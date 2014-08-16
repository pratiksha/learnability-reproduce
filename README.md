learnability-reproduce
======================

Generic instructions for reproducing results:

Prerequisites
C++11 compiler, git, libprotobuf-dev, protoc-compiler
Steps

1.
    ```
    tar zxvf ns-allinone-2.35.tar.gz 
    ```
2.    
    ```
    cd ns-allinone-2.35 
    ```
3.    
    ```
    rm -rf ns-2.35 
    ```
    to get rid of the original version of ns-2.35

4.    
    ```
    git clone https://github.com/hbatmit/ns2.35
    ```
    to checkout our modified version of ns-2.35

5.    
    ```
    git checkout <SHA-1-hash>
    ```
    where <SHA-1-hash> is the commit ID mentioned in each figure. 

6.    
    ```
    ./install 
    ```
    to install ns-2.35 with all its components.

7.    
    ```
    cd tcl/ex/decomposability/congctrl/sim_scripts
    ```
8. Run appropriate Python script to generate a Makefile for that experiment.
The Makefile has one target for each distinct ns-2 run required for that
experiment. Running with make -j N -k limits the number of parallel simulation
runs to N and "-k" allows the simulations to continue even if a few simulations
fail for some reason.

9. Next, run the appropriate analysis script to summarize the results.

