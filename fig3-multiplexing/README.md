## Instructions ##
First, check out the appropriate commits in "Code" below.

### Generating the results ###
In the folder ns-2.35/tc/ex/decomposability, run
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

https://github.com/hbatmit/ns2.35/commit/8518585265803bba0f78c62eb28af930b9f1b6d1

### Simulation results ###

http://web.mit.edu/remy/learnability/ns2resultssendersweep-5BDP.tar.gz (5 BDP buffer)
http://web.mit.edu/remy/learnability/ns2resultssendersweep-infBDP.tar.gz (unbounded buffer)

### RemyCC commits ###

1--2 senders:   muxing2.dna.2          https://github.com/keithw/remy/commit/19a226e9c442f8300ed1f0364aec566b17aceaf2

1--10 senders:  muxing10-resume.dna.3  https://github.com/keithw/remy/commit/57addc0041ddf9b4ea03b504c2dba0c9cad81fd1

1--20 senders:  muxing20-resume.dna.5  https://github.com/keithw/remy/commit/59107622979e793410d395f0d6092e358ed58a4f

1--50 senders:  muxing50-resume.dna.1  https://github.com/keithw/remy/commit/494acb88cd47dd53db9837e97ce60fc786c9c93c

1--100 senders: muxing100-resume.dna.0 https://github.com/keithw/remy/commit/2c21e20e599bb7fd5a22f9be1d0e2d2042998233  
