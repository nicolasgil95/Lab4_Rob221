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
<a href="https://imgbb.com/"><img src="https://i.ibb.co/qmg3Xvg/Whats-App-Image-2022-06-29-at-8-45-16-PM.jpg" alt="Whats-App-Image-2022-06-29-at-8-45-16-PM" border="0"></a>
## Robot Studio Simulation

To achive the goal of this lab we generated the set of points on an horizontal plane and each letter has a size of 100 x 50 mm. The movements between the points of each letter are _MoveL_ instructions with a _speed_ of 100 and a _zone_ of 10. Any other movement was made with _MoveJ_ isntructions. The curve in J letter is made by joining together two _MoveJ_ instructions into a _MoveC_ instruction. 

After checking the trajectory generated for the horizntal plane, we generated another _WorkObject_ which described the 30° rotated plane. In this new _WorkObject_ the previusly defined points were copied from the previous _WorkObject_ and the new trajectory was generated using the same parameters.

In this _[link](https://youtu.be/7uJFcwLbrFM)_ you will find the video of the paths simulated in RS. There is possible to see how the TCP travels around the world and draws the desired letters.

Sadly we couldn't make a real use of the robot due to the low available time to use them.

## Description of the proposed solution.
Firstly, the real robot tool has been calibrated, which has been given the option to insert 4 points on the flexpendant with different tool orientation.in this case, the end effector of the tool always had to arrive at the same position. On the other hand, in the same panel, a point was inserted where the tool is perpendicular to the xy plane of the deck, and the tip of the tool has the same position as the previous points.




## Conclusions
 - The horizontal board where the robot writes has slopes, which means that the lines are not as we want.
 - Calibrating the real robot tool is more complicated than the simulated one, since, with a minimum error when data is taken, it can be converted into several millimeters of error.




