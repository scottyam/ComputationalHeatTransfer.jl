# Using initialize_ohpsys
initialize_ohpsys

# Using 

# Source code changes for fill ratio
File we are editing: Preprocessing.jl

Changed this source code:
function initialize_ohpsys(sys,p_fluid,power;boil_waiting_time=1.0,Rn_boil=3e-6,inertia_f=1.3,tube_d=1e-3,tubeshape="square",g_angle=(3/2)*π,Nu=3.6,slugnum=30,film_fraction=0.3,g = 0*9.81,ηplus=0.6,ηminus=0.0,nucleatenum = 250,L_newbubble = 6e-3)

To this:
function initialize_ohpsys(sys,p_fluid,power;chargeratio=0.46, boil_waiting_time=1.0,Rn_boil=3e-6,inertia_f=1.3,tube_d=1e-3,tubeshape="square",g_angle=(3/2)*π,Nu=3.6,slugnum=30,film_fraction=0.3,g = 0*9.81,ηplus=0.6,ηminus=0.0,nucleatenum = 250,L_newbubble = 6e-3)

Changed this source code:
X0,realratio = randomXp(tube,numofslugs=slugnum)

To this: 
X0,realratio = randomXp(tube,numofslugs=slugnum, chargeratio=chargeratio)

Changes are implemented in this version
