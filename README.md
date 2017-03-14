An Experimental Study of the Learnability of Congestion Control
======================

This repository contains materials to reproduce the results of a 
[paper](http://web.mit.edu/keithw/www/Learnability-SIGCOMM2014.pdf), 
appearing at ACM SIGCOMM 2014,
which explores the "learnability" of congestion control protocols
through the use of an automated protocol design tool, 
[Remy](http://web.mit.edu/remy/).

## Prerequisites ##

You will need a C++11 compiler, git, an appropriate version of [Protocol Buffers](https://github.com/google/protobuf) (see step 4b below), Python 2.7, and numpy.

## Steps ##

1. Get the [base ns-2 tarball](http://web.mit.edu/anirudh/www/ns-allinone-2.35.tar.gz) and untar it.

    ```
    tar zxvf ns-allinone-2.35.tar.gz 
    ```

2.  cd into the untarred folder.

    ```
    cd ns-allinone-2.35 
    ```
3.  Replace the original version of ns-2.35 with our modified ns-2.35 repository. (We leave the remaining components as is.)

    ```
    rm -rf ns-2.35 
    git clone https://github.com/pratiksha/ns2.35 ns-2.35
    ```

4.  For each figure in the paper, this repository contains a folder with a README file, which provides the SHA-1 hash for a specific commit in ns-2.35. Check out the ns-2.35 commit for the figure you wish to reproduce using the appropriate SHA-1 hash:

    ```
    cd ns-2.35
    git checkout <SHA-1-hash>
    cd ..
    ```
4b [UPDATE] The protobuf version on most machines has been updated since we generated protobuf outputs (dna.pb.h and dna.pb.cc in the ns-2.35/tcp/remy). The versions in our ns-2.35 repo are most likely out of date relative to the protobuf version on your machine. To fix this, run the following:

    (assuming you are in the ns-2.35 folder)
    ```
    cd tcp/remy
    protoc --cpp_out=. dna.proto
    ```
    
5.  Now install ns-2.35 with all its components.

    ```
    ./install 
    ```

6.  cd to the decomposability folder in order to run the simulations.

    ```
    cd ns-2.35/tcl/ex/decomposability/
    ```

7. Follow the instructions in the README file of the appropriate figure's folder
   to run the simulations and summarize the results. The graphmaker and ellipsemaker scripts in
   ns-2.35/tcl/ex/graphing-scripts can be used to generate the ellipse figures
   from the results.

## For questions or comments, please email remy@mit.edu ##
