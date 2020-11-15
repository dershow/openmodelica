# openmodelica

Docker files for running OpenModelica with a desktop and novnc.
Therea are two versions:
stable and nightly
dersh/om_desktop-stable
dersh/om_

These dockerfiles are based on: accetto/xubuntu-vnc-novnc
The default password is: headless
To run this image:
docker run -d -p 25901:5901 -p 26901:6901 dersh/om-desktop-stable
or 
docker run -d -p 25901:5901 -p 26901:6901 dersh/om-desktop-nightly

Then connect with a browser to locahost (or another host where you have run docker):

For example:
http://localhost:26901/vnc.html?password=headless

