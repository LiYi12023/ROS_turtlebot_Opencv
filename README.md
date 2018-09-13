# ROS_turtlebot_Opencv
此程式用於開啟一新視窗，讀取realsens 攝影機在現實世界中，或turtlebot在模擬環境中的攝影機畫面。  
This project is used to create new windows to catch the vision of the turtlebot in the simulation world and the real world.  
## 使用方法 Usage
**1. 下載 Download**  
在終端機中首先移動至想存取的工作環境中，接著下載檔案：  
Moves to the work space and then clone the project.  
`$ git clone https://github.com/LiYi12023/ROS_turtlebot_Opencv.git`

**2. 編輯及建立程式 Edit and build**  
在終端機中輸入以下資料，以更新並建立程式  
Add the environment variables and build the program.  
` $ source devel/setup.bash`  
` $ catkin_make`  

**3. 更改程式  Setting the code**  
可以藉由更改image_converter.cpp 中繼承的Ros主題，選擇顯示realsens 攝影機畫面，或模擬環境中的攝影機畫面。  
By changing the Subscriber in the image_converter.cpp, you can choose to see the real world vision or the simulation vision.
## 測試 Test
**1. 模擬環境 Simulation world**  
`$ roslaunch turtlebot_gazebo turtlebot_world.launch`  
`$ rosrun ROS_turtlebot_Opencv image_converter`  
![image](https://raw.githubusercontent.com/LiYi12023/ROS_turtlebot_Opencv/master/In_turtlebot_world.jpg)  

**2. 真實環境 Real world**  
`$ roslaunch roslaunch realsense2_camera rs_rgbd.launch`  
`$ rosrun ROS_turtlebot_Opencv image_converter`  
![image](https://raw.githubusercontent.com/LiYi12023/ROS_turtlebot_Opencv/master/In_real_world.png)  

## LICENSE
請查看資料夾中LICENSE檔案，以獲得更多相關資訊。  
Please see the LICENSE file for more information.
