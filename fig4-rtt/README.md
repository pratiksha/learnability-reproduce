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
In the folder ns-2.35/tcl/ex/decomposability, run
   ```
   python sim_scripts/agilityanalysis.py
   ```

## Code ##

### ns-2.35 commit ###

https://github.com/pratiksha/ns2.35/commit/910ccefb0863fcd56a7e8a560549d805f0a09dac

### Simulation results ###

http://web.mit.edu/remy/learnability/results-rttvar.tar.gz

### RemyCC commits ###

150 ms alone: 150-alone.dna.2 https://github.com/keithw/remy/commit/1d4df5bd73707cdbe38c40846560e61065320be0 

145--155 ms : 145--155.dna.4  https://github.com/keithw/remy/commit/c143a61649fbcc12df53c78a7de49bd915fc95cf 

140--160 ms : 140-160.dna.5   https://github.com/keithw/remy/commit/30909e99a803a4770a325fb47ef271416d0a211b 

110--200 ms : rtt_10x.dna.3   https://github.com/keithw/remy/commit/40f97eed4a73f09d87bb14057ac06e6fed201f9a 

50--250 ms  : rtt_20x.dna.4   https://github.com/keithw/remy/commit/5015e4709326c95b70add7720ab26b0e57bc85ec

30--280 ms  : rtt_30x.dna.2   https://github.com/keithw/remy/commit/6e4f2cffa2dfb47d26b8776b3a63c6663da6ca0a
