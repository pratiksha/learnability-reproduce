## Instructions ##
First, check out the appropriate commits in "Code" below.

### Generating the results ###
In the folder ns-2.35/tcl/ex/decomposability, run
   ```
   python sim_scripts/agilitysweep.py > Makefile
   ```
The Makefile generated has one target for each distinct ns-2 run required for 
this
experiment. Run
   ```         
   make -j N -k
   ```
to limit the number of parallel simulation runs to N; "-k" allows the 
simulations to continue even if a few simulations fail for some reason.


### Summarizing the results ###


## Code ##

### ns-2.35 commit ###

https://github.com/hbatmit/ns2.35/commit/9cbc214a4b04ce9ed40f341ffa20f97efcc9406e

### Simulation results ###

http://web.mit.edu/remy/learnability/resultsoptimal.tar.gz

### RemyCC commit ###

150 ms alone: 150-alone.dna.2 https://github.com/keithw/remy/commit/1d4df5bd73707cdbe38c40846560e61065320be0
