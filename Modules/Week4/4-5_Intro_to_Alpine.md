# Intro to Alpine

Today, we will start to learn about **High-Performance Computing** or HPC. HPC is a means of performing large computational tasks on supercomputers or compute clusters in a way that takes advantage of their ability to perform multiple tasks simultaneously.

**Supercomputers** in the crudest terms are basically what happens if you glued 100's or 1000's of individual computers together. You end up making a giant computer with more functionality.

The supercomputer we'll be using is **ALPINE** and it lives on CU Boulder campus. [ALPINE](https://www.colorado.edu/rc/alpine) is a joint venture between Colorado State University and CU Boulder and is sponsored by those institutes and by a grant from the National Science Foundation. **ALPINE** is shared between CU Boulder, Colorado State University, CU Anschutz, and RMACC (Rocky Mountain Advanced Computing Consortium, a network of >20 other academic institutions in Colorado, Arizona, Idaho, Montana, and New Mexico).

There is a list of the [Top 500 biggest supercomputers](https://www.top500.org/lists/top500/list/2023/06/) on the planet (as of June 2023). According to this list, the largest supercomputer is **FRONTIER** located at Oak Ridge National Labs in Tennessee and run by the DOE (US Department of Energy).

How do these supercomputer systems compare to our laptops?

| Typical laptop | Alpine Supercomputer	| FRONTIER Supercomputer |
| -------------- | -------------------- | ---------------------- |
| 0.1 - 10 teraFLOPS | 450 teraFLOPS |	1,102,000 teraFLOPS |
| 1 - 4 cores organized onto 1 node |	11,300 cores on 485 nodes	| 8,730,112 cores |

- **FLOPS** is a measure of how many floating point operations a computer can do per second. So it's a measure of calculations a second
- **Cores** relates to how many CPUs (Central Processing Units) the computer has

**!!! NOTE:** *All 500* of the top 500 Supercomputer systems run LINUX or LINUX-based operating systems!

### What are the benefits and drawbacks of using a supercomputer?

#### Benefits

power, efficiency, and speed!!!
team of professionals to help set up the system and provide user support
allows for collaboration with other users

#### Drawbacks

There is a learning curve
Multi-user platform requires job-sharing - there is usually a queue to execute your code
May not have architecture specialized for your task.

