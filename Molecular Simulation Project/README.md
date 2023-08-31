# Gibbs Ensemble Monte Carlo Simulations (constant NPT version)
using MCCCS Towhee (https://towhee.sourceforge.net/)

## System: CO2, Methane (united atom), ZSM-5 (zeolite)
## Force field:
– Methane force field by Dubbeldam et al. (2004)
(see https://towhee.sourceforge.net/forcefields/dubb2004.html)
– Zeolite and CO2 force field from DOI: 10.1088/0965-0393/24/4/045002

## Project Idea: 
Carry out Gibbs ensemble Monte Carlo (GEMC) simulations of the adsorption of a binary mixture of carbon dioxide (CO2) and methane
(united atom) on a zeolite(ZSM-5). Place the zeolite structure (without any gas
molecules) in one box initially and a binary mixture of CO2 and united atom
methane in the other box. Use 100 molecules of CO2 and 200 molecules of methane
initially. Assume the zeolite framework to be rigid and carry out the moves only
on the gas atoms and molecules (not on the zeolite framework). Note that the
entire zeolite framework is treated as a single molecule during the simulation.

## Objective
At 
Temperature :300 K and 
Following pressure values (in kPa): 1, 10, 50, 100, 500, 1000, 2000. 
Carry out 5000 cycles of GEMC
simulation at each pressure value. At each pressure, consider the average amount
of gas adsorbed during the last 2500 cycles of GEMC simulation (using the block
averaging feature in Towhee) to obtain the adsorption isotherm

## Results to Generate:
– Plot of the adsorption isotherms of CO2 and methane on ZSM-5 at 300 K
(i.e., plot of moles of gas adsorbed per kg of adsorbent vs pressure)
– Plot of the selectivity of CO2 over methane against the pressure at 300 K.
Selectivity of component B over component A is defined as αB/A =(xB/xA)/(yB/yA)
where xi and yi represent the mole fractions of component i in the adsorbed
and gas phases respectively
