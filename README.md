# dlib_puppeteering
A ros based dlib package for puppeteering is currently in progressive development

## Errors and fixes
Unable to open /home/wesagn/catkin_ws/src/dlib_puppeteering/src/shape_predictor_68_face_landmarks.dat for reading.
[dlib_puppeteering_node-3] process has died [pid 5800, exit code -6, cmd /home/wessi/catkin_ws/devel/lib/dlib_puppeteering/dlib_puppeteering_node __name:=dlib_puppeteering_node __log:=/home/wessi/.ros/log/746c1e46-20b2-11e6-96af-94de80604b3b/dlib_puppeteering_node-3.log].
log file: /home/wessi/.ros/log/746c1e46-20b2-11e6-96af-94de80604b3b/dlib_puppeteering_node-3*.log

you have to change the location of `shape_predictor_68_face_landmarks.dat`


# Install and run
```
#1: open new terminal
cd catkin_ws
catkin_make
source devel/setup.bash
cd src
pip3 install -t ../devel/lib/python2.7/dist-packages/ ./blender_api_msgs
cd blender api
goto:#2
blender -y Sophia.blend -P autostart.py

#2: open new terminal and 
roslaunch facial_puppetry facial_puppetry.launch
```

# NOTE: do the following in ../blender_api/rigControl/commands.py

# 16 - Face shapekeys controlled by PAU
self.pauAnimationMode = 16
# If 1 current shapekeys are controlled directly by PAU, otherwise by default drivers
self.shapekeysControl = 1

# Exit
```
close blender
quit facial_puppetry
```

Dependency cycle detected:
  deform depends on control through Child Of.
  control depends on deform through Locked Track.

No Command Sources found
`
cd src
pip3 install -t ../devel/lib/python2.7/dist-packages/ ./blender_api_msgs
source devel/setup.bash
cd src
`