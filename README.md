# CPS_Paper

## Running Physical Twin:

#### Requirements:
- Niryo Ned Robot
- Conveyor Belt
- Gripping Tool
- Physical Twin scripts from `physical_twin`

#### Steps:
- Install required packages [https://docs.niryo.com/dev/ros/v3.2.0/en/source/overview.html](https://docs.niryo.com/dev/ros/v3.2.0/en/source/overview.html)
- Make the physical connections according to the architecture
- Run the script form `Physical_Twin`

## Running Digital Twin:

#### Requirements:
- Niryo Ned Robot
- Conveyor Belt
- Gripping Tool
- Physical Twin scripts from `Physical_Twin`

#### Steps:
- Install required packages [https://docs.niryo.com/dev/ros/v3.2.0/en/source/overview.html](https://docs.niryo.com/dev/ros/v3.2.0/en/source/overview.html)
- Make the physical connections according to the architecture
- Run the script form `physical_twin`


## Running Digital Twin
### Requirements:
- Webots 2023a https://github.com/cyberbotics/webots/releases/tag/R2023a
- URDF model of Niryo Ned robot
- urdf and .py under `Digital_Twin_File/` folder

### Steps:
1. Open Webots and load the `Niryo_Ned.wbt` file or else create new Niryo Ned robot and load the `Niryo_Ned.urdf` file.
2. Load the `Digital_Twin_Niryo.py` under `Digital_Twin`.
3. And run the `Digital_Twin_Niryo.py` file.
