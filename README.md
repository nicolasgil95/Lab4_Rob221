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
## RAPID code of the module used for the development of the practice.

you can go to the Rapid Program folder where the code is located.

## Video containing the simulation in Robotstudio.

https://youtu.be/7uJFcwLbrFM

## Description of the proposed solution.
Firstly, the real robot tool has been calibrated, which has been given the option to insert 4 points on the flexpendant with different tool orientation.in this case, the end effector of the tool always had to arrive at the same position. On the other hand, in the same panel, a point was inserted where the tool is perpendicular to the xy plane of the deck, and the tip of the tool has the same position as the previous points.




## Conclusions
 - The horizontal board where the robot writes has slopes, which means that the lines are not as we want.
 - Calibrating the real robot tool is more complicated than the simulated one, since, with a minimum error when data is taken, it can be converted into several millimeters of error.




