# SAS_jetsonnano
 ## jetson nano jetpack SDK
 Ver 4.6.1
 ## install
 sudo apt update
sudo apt install nvidia-jetpack

For ubuntu 18.04
sudo apt-key adv --fetch-key http://repo.download.nvidia.com/jetson/jetson-ota-public.asc
run 
chmod +x ZED_SDK_Tegra_L4T32.3_v3.7.4.run 
./ZED_SDK_Tegra_L4T32.3_v3.7.4.run 


# startle
## ZED
 cd ~/catkin_ws/src
 git clone --recursive https://github.com/stereolabs/zed-ros-wrapper.git
 cd ../
 rosdep install --from-paths src --ignore-src -r -y
 catkin_make -DCMAKE_BUILD_TYPE=Release
 source ./devel/setup.bash
 
 cd ~/catkin_ws/src
 git clone https://github.com/stereolabs/zed-ros-examples.git
 cd ../
 rosdep install --from-paths src --ignore-src -r -y
 catkin_make -DCMAKE_BUILD_TYPE=Release
 source ./devel/setup.bash
## Ardupilot
https://ardupilot.org/dev/docs/using-gazebo-simulator-with-sitl.html
To solve  gazebo: symbol lookup error:
sudo apt upgrade libignition-math2
Build Gazebo9 (10 is ok need to >8)
https://classic.gazebosim.org/tutorials?tut=install_ubuntu
check
 cat /etc/apt/sources.list.d/gazebo-stable.list
 wget https://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
 instead 11
 sudo apt-get install gazebo9
 For developers that work on top of Gazebo, one extra package
sudo apt-get install libgazebo9-dev
go to ardupilot file 
ardupilot_gazebo from khancyr github
 mkdir build 
 cd build
 cmake ..
 make
 sudo make install
Add source
 gedit ~/.bashrc
 source /usr/share/gazebo/setup.sh

export GAZEBO_MODEL_PATH=~/ardupilot_ws/ardupilot_gazebo/models:${GAZEBO_MODEL_PATH}

export GAZEBO_MODEL_PATH=~/ardupilot_ws/ardupilot_gazebo/models_gazebo:${GAZEBO_MODEL_PATH}

export GAZEBO_RESOURCE_PATH=~/ardupilot_ws/ardupilot_gazebo/world:${GAZEBO_RESOURCE_PATH}
