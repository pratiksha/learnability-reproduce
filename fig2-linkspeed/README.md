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

https://github.com/pratiksha/ns2.35/commit/d943277aa5e81c47677be89285fdfc9323df2203

### Simulation results ###

http://web.mit.edu/remy/learnability/resultslogarithmic.tar.gz (10x, 100x, 1000x, cubic, cubic/sfqcodel)
http://web.mit.edu/remy/learnability/results2x.tar.gz (2x)

### RemyCC commits ###

1000x RemyCC: bigbertha2.dna.5     https://github.com/keithw/remy/commit/ad05f8a6cbedc4b4c1a74ffbc3640f02e91920d9

100x RemyCC:  bigbertha-100x.dna.5 https://github.com/keithw/remy/commit/64dc0a7216fcaba15c052a9132e2a1992460d7cc

10x RemyCC:   bigbertha-10x.dna.4  https://github.com/keithw/remy/commit/8faf8844bfa1182c7a93b7f207a472c21baf519f

2x RemyCC:    bigbertha2x.dna.5    https://github.com/keithw/remy/commit/4180b10043e8b7ff87d6a80ba4e287d201c406d3 
