# rospractice
basic informations about ros_turtlesim
rostopic pub -r 5 /turtle1/cmd_vel geometry_msgs/Twist  '{linear:   {x: 0.1, y: 0.0, z: 0.0},   angular:  {x: 0.0, y: 0.0, z: 0.0}}' 
rosrun turtlesim turtlesim_node
rosrun turtlesim turtle_teleop_key
What is the first command you must run in ROS?
roscore 
What is the command to run the Turtlesim simulator?
rosrun turtlesim turtlesim_node 
What is the command to find the list of all ROS nodes?
rosnode list  
What is the command to find the list of all ROS topics?
rostopic list  
What is the topic that tells about the position of the turtle?
/turtle1/pose 
What is the topic that sends command to the turtle to make it move?
turtle1/cmd_vel 
What is the command that tells you information about the topic about velocity?
rostopic info /turtle1/cmd_vel 
What is the node used to publish velocity commands to the turtle?
turtle_teleop_key
What is the node used to subscribe to velocity commands to the turtle?
turtlesim 
What is the command that allows to see the type of message for velocity topic?
rostopic info /turtle1/cmd_vel
What is the content of the velocity message? Explain its content.
rosmsg show geometry_msgs/Twist

  
geometry_msgs/Vector3 linear

  
  float64 x

  
  float64 y

  
  float64 z

  
geometry_msgs/Vector3 angular

  
  float64 x

  
  float64 y

  
  float64 z

  
 
we use x
y for linear velocity and z for angular velocity
What is the content of the position message? Explain its content
rosmsg show turtlesim/Pose

  
float32 x

  
float32 y

  
float32 theta

  
float32 linear_velocity

  float32 angular_velocity
rosservice list
rosservice info /spawn
rossrv info turtlesim/Spawn
rosservice call /spawn 7 0 0 turtle2 	//for create another turtle
rosservice call /kill turtle2 //for kill the turtle
