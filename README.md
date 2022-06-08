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
