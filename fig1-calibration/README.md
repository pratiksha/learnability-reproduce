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


## Code ##

### ns-2.35 commit ###

https://github.com/pratiksha/ns2.35/commit/d9e230ec5b95a50921ad3db61e2c1a76fc1c0bf2

### Simulation results ###

http://web.mit.edu/remy/learnability/resultsoptimal.tar.gz

### RemyCC commit ###

150 ms alone: 150-alone.dna.2 https://github.com/keithw/remy/commit/1d4df5bd73707cdbe38c40846560e61065320be0
