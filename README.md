# ROS2_Humble_Visual_System
ROS2 Humble Visual System. This use your build in Camera or external camera. It has a build in detecter which is not 100% complete and still in development.
OS: Ubuntu 22.04 (Jammy Jellyfish)

The file is large so it is compressed to a zip file

Extract ws2.zip as ws2 folder in Home folder or in any location

# INSTALL ROS2 HUMBLE FROM HERE

https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html

# Terminal 1
cd ~/ws2

source /opt/ros/humble/setup.bash

colcon build

source install/setup.bash

chmod +x ~/ws2/src/aed/aed/camera.py ~/ws2/src/aed/aed/viewer.py ~/ws2/src/aed/aed/detector.py

head -n 1 ~/ws2/src/aed/aed/camera.py

head -n 1 ~/ws2/src/aed/aed/viewer.py

head -n 1 ~/ws2/src/aed/aed/detector.py




# For all three files, the absolute first line must be exactly this:

#!/usr/bin/env python3

cd ~/ws2

rm -rf build install log

source /opt/ros/humble/setup.bash

colcon build

source install/setup.bash




# It should cleanly output all three scripts:

aed camera_pub

aed camera_sub

aed detector

ros2 run aed camera_pub



# Terminal 1 Continuation 

cd ~/ws2

source install/setup.bash

ros2 run aed camera.py




USE CTRL+SHIFT+T in Ubuntu 22.04

No need to colcon build in terminal 2 and 3

# Terminal 2

cd ~/ws2

source install/setup.bash

ros2 run aed detector.py



USE CTRL+SHIFT+T to open a new terminal

# Terminal 3
cd ~/ws2

source install/setup.bash

ros2 run aed viewer.py




# INSTALLATION REQUIREMENTS

pip3 install ultralytics

pip3 install "numpy<2"
