# Two-D-Motion-Simulator
The classes in this repository can be used to simulate two-dimensional motion in two different formats. Both used Open Source 
Physics packages for the visual components of the simulaion. All projects in this class involves the ParticleDM class, which encodes all of the normal characteristic and functions associated with a two-d particle (e.g., velocity, x and y position, etc.)

The first project is to simulate the motion of a ball that is subject to both gravity and air resistance. Specifically, it is
initialized to simulate the conditions of the Green Monster wall in Fenway park for the purpose of finding the optimal angle 
and smallest velocity necessary to hit a homerun over the wall. First, the program initializes an array of baseballs (about a 
hundred of them) with a initial velocity that is too large. They are then all shot towards the wall at their varying angles. 
After they all land, velocity is decreased and the range of angles of the new set of balls that is restricted to the range of 
angles of those that made it over previously. This process is repeated iteratively forever. After a couple of minutes, a pretty exact estimate of the optimal angle for the baseball to travel over the wall is achieved. For each set of balls launched, the minimum of the set's angle rnage is printed on the screen. Because the range gets smaller as the rounds go on, the minimum angle eventually approaches the optimal angle. BaseballDM is the class specific to this task.

A second, more extensive project is also included in this repository: a simulation of ideal gas molecules in a box. The goal of the project was to find the distribution of air particles when subject to gravity. This question came from my curiousity about the way in which air particles distribute when subject to gravity, knowing that we can breathe without noticing a difference when at sea level as when 20 feet above sea level. I recognized that there was an opposing force at play: kinetic energy. While gravity pulls particles down, the total energy of a batch of particles (if not lost to other forms that were
not kinetic or potential) would keep the gas molecules occupying a certain volume. So I developed the CollisionDM, an object that performs calculations and stores data relating to specific collisions between particles, and
