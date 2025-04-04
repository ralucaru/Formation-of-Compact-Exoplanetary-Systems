# Formation-of-Compact-Exoplanetary-Systems

Data of simulations from "Origin of compact exoplanetary systems during disk infall"
by Raluca Rufu and Robin M. Canup

The folder includes the symba output and input files for the simulations shown in Figure 4a.
The full description of the symba code and the structure of output and input files is available at: https://www.boulder.swri.edu/~hal/swift.html .
The code requires units in which the grav. constant G is unity. Unless otherwise specified the units used are such that the mass of primary 4*pi^2 and the radius of primary is 1.

File description in each folder:
1. bin.dat - contains orbital elements of all bodies EXCEPT the central body, similar format to symba
2. discard_mass.out - contains the bodies that are added/removed from the simulation, similar format to symba.
   Format:
   **if merging occours**
   Time  2
  -1 Body1Id  Body1Mass Body1Radius
   x1  y1  z1
   Vx1  Vy1  Vz1
  -1  Body2Id  Body2Mass Body2Radius
   x2  y2  z2
   Vx2  Vy2  Vz2
   +1 MergedBodyId MergedBodyMass MergedBodyRadius
     x  y  z
   Vx  Vy  Vz
   **if escape/capture occours**
      Time  1
  -1 Body1Id  Body1Mass Body1Radius
   x1  y1  z1
   Vx1  Vy1  Vz1
3. mass.bin.dat contains the mass of all bodies INCLUDING the central body,  similar format to symba
4. runinfo.in - details about the infall and the gas disk surface density input.
5. outev - text output during the run.
6. param.in - parameterss of the run, similar format to symba
7. pl.in - initial distribution of planetesimals, similar format to symba
8. inflowvst.out - contains the infall rate and surface density at each output timestep in code units.
9. totalmassvst.out - number of bodies in simualtion and the total mass (normalized by the primary mass) each output timestep.
