# openmodelica

Docker files for running OpenModelica with a desktop and novnc.
There are two versions:
stable and nightly<p>
dersh/om-desktop-stable<p>
dersh/om-desktop-nightly

These dockerfiles are based on: accetto/xubuntu-vnc-novnc
The default password is: headless <p>
To run this image:<p>
docker run -d -p 25901:5901 -p 26901:6901 dersh/om-desktop-stable<p>
or <p>
docker run -d -p 25901:5901 -p 26901:6901 dersh/om-desktop-nightly<p>

Then connect with a browser to locahost (or another host where you have run docker):<p>

For example:<p>
http://localhost:26901/vnc.html?password=headless

