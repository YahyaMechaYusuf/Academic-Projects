The main goal of the project is to add an extra line of defense to the bomb disposal squad by providing a mobile robot that is used in operations of searching, detecting, and handling explosive materials.

1- Provide remote monitoring by a live camera streaming and controlling application for analysis of a suspicious bomb.
2- Allow the user to manipulate the bomb using the robotic arm.
3- provide visual feedback from the site of the bomb.
4- provide a very user-friendly control application


Methodology:
The Robot uses a control application, at the user end to
control the robot remotely using Wireless technology. The bomb technician
controls the robot using a joystick. Input from the user is transmitted serially
over an RF link to the Robot, where it is received, identified, and relayed to the desired position.


Robot steering:
It is a system that allows a tank, or other continuous track vehicles, to turn. Because the tracks cannot be angled relative to the hull (in any operational design), the steering must be accomplished by speeding one track up, slowing the other down (or reversing it), or a combination of both. The tank engine rotates one or more steel sprockets, which move a track made up of hundreds of metal links. The tank's wheels ride along the moving track, just like the wheels in a car run along the road.
Inspired by the tank’s steering theory & Taking into account that some of the road environments in which both the robot and the tank operate are common, we decided to drive our robot to mimic a simple tank’s movement behavior.
This is applied firstly by choosing steel sprockets to lead the roller chains derived by a motor on each side of the robot, which will then be controlled to drive the robot forward, backward, right & left.

Controlling the robot’s movement using the Dual motor vnh5019 shield was very simple to code, it only needs a speed value & a direction (+ve or -ve).
For forward movement: we desire that both roller chains rotate in the same direction (forward) i.e., in our case: directed to the robotic arm. This is implemented by giving the 2 motors the same speed but in the opposite direction because the 2 motors are reversed” compared to each other”.

For backward movement: we desire that both roller chains rotate in the same direction (backward) i.e., in our case: directed to the other side of the robotic arm. This is implemented by giving the 2 motors the same speed but in the opposite direction because the 2 motors are reversed” compared to each other”. Just inverting the forward directions.

The aim of steering the robot is to manipulate it in order to take a turn in a curve form, not an instantaneous turn, this is implemented by driving both the roller chains in the same direction but with speed variation.
For Turning the Robot Right: The left roller chain should rotate faster than the Right one.
For Turning the Robot Left: The Right roller chain should rotate faster than the Left one.

The difference in the speeds should decide how bigger or smaller the curve will be done by the robot. So, The speed variation is inversely proportional to the curve size.
