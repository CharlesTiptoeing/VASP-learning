## What is density of state (DOS)

**One sentence defination**: The density of state (DOS) is the number of different states at a particular energy level that electrons are allowed to occupied(the number of electron states per unit volume per unit energy). **Application**: paramagnetic susceptibility, tranport phenomena of solids depend on this function, and determining the spacing between energy bands in semi-conductors.

### Denisty of state for wave
![The diagram for the desnity of state for wave](Picture1.png)

### Density of Electrons
![The diagram for the desnity of state for wave](DosAndEnergyDistribution.png)

### Procedure of running DOS calculation on VASP
1. Perform a static self consistent calculation (NSW = 0, IBRION = -1) for the DOS.

2. Make a DOS caculation by changing INCAR (ISTART = 1, ICHARG = 11, NEDOS = 1000, LORBIT = 11)
  >**ISTART=1** read from the old plane wave, and reload a new one into the WAVECAR file.
  >**ICHARG=11** To obtain the DOS for a given charge density read from CHGCAR. The selfconsistent CHGCAR file must be determined beforehand doing by a fully self-consistent calculation with a k-point grid spanning the entire Brillouin zone.
  >**LORBIT=11** 

3. Draw DOS graph


### References

[1]Density of States. (2021, September 8). https://eng.libretexts.org/@go/page/312 
