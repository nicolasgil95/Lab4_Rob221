# Lab4_Rob221
# Industrial robotics

By: Jhon Brandol Muñoz Romero, Nicolas Gil Rojas and 
Jorge Luis Reina Jara

Generate the necessary paths to represent the initial letters of the names of each member by group.
The following restrictions must be taken into account:
- The trajectories to be developed must be carried out in a speed range between 100 and 1000
- The maximum tolerable error zone must be z10.
- El movimiento debe partir de una posición home especificada (puede ser el home del robot) y realizar la trayectoria de cada letra con un trazo continuo, el movimiento debe finalizar en la misma posición de home en la que se inició.
- The trajectories must lie in the positive quadrant of xy.
- Las letras deben estar separadas.


## Tool design.
The tool has been designed to be manufactured with addictive manufacturing. Therefore,  there is a spring inside that will be responsible for pushing the marker.


<a href="https://imgbb.com/"><img src="https://i.ibb.co/qmg3Xvg/Whats-App-Image-2022-06-29-at-8-45-16-PM.jpg" alt="Whats-App-Image-2022-06-29-at-8-45-16-PM" border="0"></a>

<a href="https://ibb.co/MZw5gHh"><img src="https://i.ibb.co/8Nv4mwB/Whats-App-Image-2022-06-29-at-11-18-47-PM.jpg" alt="Whats-App-Image-2022-06-29-at-11-18-47-PM" border="0"></a>

## Robot Studio Simulation

To achive the goal of this lab we generated the set of points on an horizontal plane and each letter has a size of 100 x 50 mm. The movements between the points of each letter are _MoveL_ instructions with a _speed_ of 100 and a _zone_ of 10. Any other movement was made with _MoveJ_ isntructions. The curve in J letter is made by joining together two _MoveJ_ instructions into a _MoveC_ instruction. 

After checking the trajectory generated for the horizntal plane, we generated another _WorkObject_ which described the 30° rotated plane. In this new _WorkObject_ the previusly defined points were copied from the previous _WorkObject_ and the new trajectory was generated using the same parameters.

In this [link](https://youtu.be/7uJFcwLbrFM) you will find the video of the paths simulated in RS. There is possible to see how the TCP travels around the world and draws the desired letters.

Sadly we couldn't make a real use of the robot due to the low available time to use them.

On 30/06/2022 we were able to use the robot on LabSir. [Here](https://youtube.com/shorts/5zYbWFITxb0) you will find the results of these work. In practice we only had to adjust the height of the points to reach the actual height of the boards installed.

## Description of the proposed solution.
The letters that have been chosen with the initial of our names are `LJN`

Firstly, the real robot tool has been calibrated, which has been given the option to insert 4 points on the flexpendant with different tool orientation.in this case, the end effector of the tool always had to arrive at the same position. On the other hand, in the same panel, a point was inserted where the tool is perpendicular to the xy plane of the deck, and the tip of the tool has the same position as the previous points.This module has been named as follows, and you can find it with the other files.


`TCPZ_tool_jnj1.MOD`

<a href="https://ibb.co/Kr4vLxD"><img src="https://i.ibb.co/mcZWX50/Screenshot-from-2022-06-29-21-11-17.png" alt="Screenshot-from-2022-06-29-21-11-17" border="0"></a>

## Conclusions
 - The horizontal board where the robot writes has slopes, which means that the lines are not as we want.
 - When replicating the horizontal plane trajectory in the inclined plane, it is mandatory to identify some "special" points, or more precisely, poses in where the multiplicity of solutions could make some troubles. It is then the robotist's job to clearly specify the more convenient set of joint configurations that prevent any undesired robot behaviour.
 - Calibrating the real robot tool is more complicated than the simulated one, since, with a minimum error when data is taken, it can be converted into several millimeters of error.
 - It turns to be very important the use of the concept of _WorkObject_ in many robot applications. It is not only an elegant way to define every pose relative to it, but it is also immensely useful when a repetitive task, but in another orientation, is required.




