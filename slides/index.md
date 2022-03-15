# Reproducibility on the HPC

## Twin Karmakharm

---
<!-- .slide: data-background="assets/img/rse-logo.svg" -->
<!-- .slide: data-background-opacity="0.2" -->

### Research Software Engineering Sheffield

* Increasing research impact through software
* Support and consultancy in research software and systems development and maintenance
    * Grant support
* Software optimisation, GPU and HPC
* Training, outreach and education activities
* Led by Dr. Paul Richmond
* Visit us at [https://rse.shef.ac.uk](https://rse.shef.ac.uk)

---

## Contents

* High Performance Computing Overview
* Building a reproducibility workflow
* Reproducibility best practices



---

## High Performance Computing Overview

---

### What is HPC?

High Performance Computing (HPC) refers to a network (cluster) of connected computers (nodes).

---

### HPC Hardware: Desktop and HPC Node comparison

It's like your PC but bigger!

<object type="image/svg+xml" data="assets/img/desktop-hpc.svg" style="height: auto;">
<param id="layer2" class="fragment" />
<param id="layer3" class="fragment" />
<param id="layer4" class="fragment" />
</object>

---

### HPC Hardware: An example HPC cluster

<object type="image/svg+xml" data="assets/img/hpc-overview.svg" style="width: 70%;height: auto;">
<param id="layer2" class="fragment fade-in-then-out" data-fragment-index="1"/>
<param id="layer3" class="fragment fade-in-then-out" data-fragment-index="2"/>
<param id="layer4" class="fragment fade-in-then-out" data-fragment-index="3"/>
<param id="layer5" class="fragment fade-in-then-out" data-fragment-index="4"/>
<param id="layer6" class="fragment fade-in-then-out" data-fragment-index="5"/>
</object>

---

### HPC Software

* Majority runs on a distribution of Linux <!-- .element: class="fragment" data-fragment-index="1" -->
* Command Line interface (GUI available on some programs e.g. Matlab) <!-- .element: class="fragment" data-fragment-index="2" -->
* Has a job scheduler to enforce fair usage <!-- .element: class="fragment" data-fragment-index="3" -->

<object type="image/svg+xml" data="assets/img/hpc-software.svg" style="width: 70%;height: auto;">
<param id="layer1" class="fragment" data-fragment-index="1"/>
<param id="layer2" class="fragment" data-fragment-index="2"/>
<param id="layer3" class="fragment" data-fragment-index="3"/>
</object>


---
### HPC Scheduler: Submitting a job

You can run code interactively (using `srun` on SLURM) when:
* Installing software
* Testing/developing your code

But for long running tasks, you'll need to submit a job.

---

### HPC Scheduler: Submitting a job

<object type="image/svg+xml" data="assets/img/scheduler-cycle.svg" style="width: 70%;height: auto;">
<param id="layer2" class="fragment" />
<param id="layer3" class="fragment" />
<param id="layer4" class="fragment" />
<param id="layer5" class="fragment" />
</object>


---
