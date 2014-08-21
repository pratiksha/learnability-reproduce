## Instructions ##
First, check out the appropriate commits in "Code" below.

### Generating the results ###
In the folder ns-2.35/tcl/ex/decomposability, run
   ```
   python sim_scripts/multilink.py > Makefile
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
   python sim_scripts/multilinkanalysis.py
   ```

## Code ##

### ns-2.35 commit ###

https://github.com/pratiksha/ns2.35/commit/7f47db6ec09a93e7a699960237cc3f7333d9d520

### Simulation results ###

http://web.mit.edu/remy/learnability/resultsmultilink.tar.gz

### RemyCC commits ###

2-bottleneck topology: multilink-take2.dna.2 https://github.com/keithw/remy/commit/c984263a7a06028b8e7c824d29c49fd9737acdb4

1-bottleneck topology: bigbertha-10x.dna.4   https://github.com/keithw/remy/commit/8faf8844bfa1182c7a93b7f207a472c21baf519f  
