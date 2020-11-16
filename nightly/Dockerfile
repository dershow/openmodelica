FROM accetto/xubuntu-vnc-novnc

#FROM consol/ubuntu-xfce-vnc:1.4.0
#Was :latest  now just try default
USER root
RUN apt-get update && apt-get install -y sudo lsb-core && rm -rf /var/lib/apt/lists/*

RUN for deb in deb deb-src; do echo "$deb http://build.openmodelica.org/apt `lsb_release -cs` nightly"; done | sudo tee /etc/apt/sources.list.d/openmodelica.list
RUN wget -q http://build.openmodelica.org/apt/openmodelica.asc -O- | sudo apt-key add -

# Update index (again) and install OpenModelica 
RUN apt-get update && apt-get install -y openmodelica omlib-modelica-3.2.3 omlib-modelicareference \
&& rm -rf /var/lib/apt/lists/*

#RUN apt install omlib-.* # Installs optional Modelica libraries (most have not been tested with OpenModelica)

USER 1000

