
### Prepare system ###
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade

"""
Additionally thesepackages are must be installed if not there already in system:

build-essential
sqlite3
ffmpeg
"""

### Pre-installations ###
pip2 install rpi_ws281x==4.3.4
pip2 install Adafruit-GPIO==1.0.3
pip2 install Adafruit-PureIO==1.0.1
pip2 install Adafruit-BBIO==1.0.9
pip2 install Adafruit-ADS1x15==1.0.2
pip2 install board==1.0
pip2 install smbus==1.1.post2
pip2 install smbus2==0.4.1
pip2 install spidev==3.5
pip2 install gTTS==2.2.3
pip2 install psutil==5.9.0

### Creating ROS DIR and Sourcing from CDL - MINT git Repo ###
mkdir -p catkin_ws_niryo_ned/src
cd catkin_ws_niryo_ned
git clone https://github.com/cdl-mint/ned_ros_master src

### ROS Melodic Installation ###
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt install curl 

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

sudo apt update

sudo apt install ros-melodic-desktop-full

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc

source ~/.bashrc

source /opt/ros/melodic/setup.bash

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update

### Install additional packages ### 
sudo apt install catkin
sudo apt install python-catkin-pkg
sudo apt install python-pymodbus
sudo apt install python-rosdistro
sudo apt install python-rospkg
sudo apt install python-rosdep-modules
sudo apt install python-rosinstall python rosinstall-generator 
sudo apt install python-wstool

### Install Melodic packages ###
sudo apt install ros-melodic-moveit
sudo apt install ros-melodic-control
sudo apt install ros-melodic-controllers
sudo apt install ros-melodic-tf2-web-republisher
sudo apt install ros-melodic-rosbridge-server
sudo apt install ros-melodic-joint-state-publisher-gui

### Setup Ros Env ### 
catkin_make

source devel/setup.bash

echo "source $(pwd)/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc