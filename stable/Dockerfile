FROM accetto/xubuntu-vnc-novnc

USER root
#RUN apt-get update && apt-get install -y sudo lsb-core && rm -rf /var/lib/apt/lists/*

RUN for deb in deb deb-src; do echo "$deb http://build.openmodelica.org/apt `lsb_release -cs` stable"; done | sudo tee /etc/apt/sources.list.d/openmodelica.list
RUN wget -q http://build.openmodelica.org/apt/openmodelica.asc -O- | sudo apt-key add -
#USER 1000
# Update index (again) and install OpenModelica 
RUN apt-get update && apt-get install -y openmodelica
#RUN apt install omlib-.* # Installs optional Modelica libraries (most have not been tested with OpenModelica)
RUN sudo apt-get install -y omlib-modelica-3.2.3
USER 1000

