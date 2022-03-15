https://www.reprohack.org/event/14/

https://docs.google.com/presentation/d/1YzR6iq4pyXUB4NFOYjh1-CUVrd4AAsb_KEmLJ_PU3eU/edit#slide=id.p

https://annakrystalli.me/talks/r-in-repro-research-dc-srse.html#1

https://sulis-hpc.github.io

Reproducing computationally intensive paper on the HPC 

For example, I thought starting by describing what goes on when they run sth on their laptop (ie how dependencies, data inputs, code etc code together) as a reference point and then expand on how that changes when they move onto a HPC systems, and what options they have to create reproducible computational environments on the cluster (including a little on containers), get their data and code on it and run it.

FAIR (Findable Accessible Interoperable Reusable)

* HPC Overview
  * What is HPC?
  * HPC hardware
  * HPC Software
    * Linux
    * Command line
    * Scheduler 
  * Scheduler - submitting a job
* Building the reproducibility workflow
  * Workflow overview
    * Paper
    * Code/Software
    * Data
  * Code/Software
    * Software packages
      * Commercial existing software
        * LAMMPS, GROMACS, SimpleMD, PLUMED
        * OpenFoam
        * Get your IT dept or RSEs to install them for you!
          * Architecture optimisation
          * interconnect interoperability MPI (infiniband?)
          * Maths library like MKL
    * Code
      * What languages did the submissions use?
        * C++
        * Fortran
          * Quantum espresso
        * Python
          * Scipy
          * pytorch
        * Julia
      * With what build tools?
        * Make & Cmake
      * Package managers
        * apt, yum, etc.
        * conda, spack
      * Containers
        * Singularity/Apptainer
          * Open MPI with infiniband check with your local RSE
          * Linux
          * Windows WSL
  * Data
  
  



* Software

    
  
  * You're not an admin!
  * Dependencies
  * Package managers
  * Containers (Singularity/Apptainer)
    
* Data
    * Getting it on the cluster
    * Processing    
* Workflow
  * Batch script, job scripts  
  * The scheduler SLURM
    * Submitting jobs
      * things might not run live
      * Request time, memory, resources that's needed
      * Log outputs, Print useful logs in stages
      * .sh Scripts
    * Hardware
      * Filesystem - Where to put your data?
        * Spinning disk
        * Fast storage? SSD? 
        * Local storage SSD?
        * RAM
        * Consider for both input, intermediates and output
      * Specilist hardware
        * GPU
        * FPGA?
      * Interconnect
        * Infiniband?
        * MPI
    * Parallisation, job arrays
* Best practices
  * Version control your code
    * Github
      * Best practices
        * README.md
          * What the project's about
          * Dependencies
            * What OS? (Probably linux) 
            * Required software and list of their dependencies
          * Build instructions
            * Do I need to compile? or are they scripts 
          * Run instructions
            * Simple and short examples to test that the program is running and installed properly
          * Dataset
            * Explanation of key dataset
              * What's in the dataset
              * Directory, file structure, file formats
            * How to run with the software (if quite different from example)
            * What outputs should I be expecting? 
          * Jupyter notebooks etc. that shows the result or process
