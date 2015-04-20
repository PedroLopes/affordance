# affordance plus plus
The code repository for the Affordance++ project, from Patrik Jonell's repo.
See http://plopes.org/project/affordance-plus-plus/ for details about this project

## What is in the code
This code is a web editor for EMS amplitude envelopes. This assumes you are running the same (or similar hardware) than the one we developed for Affordance++ (check details in the paper). The editor is able to create user specific gestures, modulate them, etc.  

### Install instructions

1. opening up a virtual env for python (3.4)
virtualenv -p /usr/bin/python3.4 <path/to/new/virtualenv/>

2. pip install -r requirements.txt

3. git clone https://github.com/rpavlik/vrpn.git
make the main C library (cmake, make)

4. ccmake with te follwoing command:
ccmake ../ -DPYTHON_LIBRARIES=/Library/Frameworks/Python.framework/Versions/3.4/lib/libpython3.4m.dylib -DPYTHON_INCLUDE_PATH=/Library/Frameworks/Python.framework/Versions/3.4/include/python3.4m -DPYTHON_EXECUTABLE=/Library/Frameworks/Python.framework/Versions/3.4/bin/python3.4m -DPYTHON_INCLUDE_DIR=/Library/Frameworks/Python.framework/Versions/3.4/include/python3.4m
or
ccmake ../ -DPYTHON_LIBRARIES=/Library/Frameworks/Python.framework/Versions/3.4/lib/libpython3.4m.dylib -DPYTHON_INCLUDE_PATH=/Library/Frameworks/Python.framework/Versions/3.4/include/python3.4m -DPYTHON_INCLUDE_DIR=/Library/Frameworks/Python.framework/Versions/3.4/include/python3.4m

and then make



5. cd into ../python and edit GNUMakefile and uncommet #mac unversal and #python 3.4 and then make
make install
copy manually the universal(or whatever build name)/vrpn.so to your libs place, for instance venv/lib/Python/site-packages

6. install mondodb
> mongod --dbpath mongodata/

7. Install Unity

Should run.



###
use coffee -j compiled.js -cwo www/static/js www/static/coffee/ for coffee compiling
