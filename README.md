<img src="https://raw.githubusercontent.com/anagainaru/MPI_Lectures/master/mpi_lecture.png" alt="Logo" align="right" width="400"/>

# SC3260 / SC5260
## High Performance Computing 
Spring 2020

**Instructors**<br/>
Ana Gainaru ([website](http://www.ana-gainaru.com))<br/>
Hongyang Sun ([website](https://my.vanderbilt.edu/hongyangsun/))<br/>

**Office**
Jacobs and Featheringill Hall #382

**Lectures** Featheringill Hall #134

**Prerequisites**<br/>
Basic scentific computing knowledge (e.g., matrix computations, sorting)<br/>
Basic knowledge in C/C++

**Table of contents**
- [Lectures](#lectures)
  * [Midterm](#midterm)
  * [Homeworks](#homeworks)
  * [Project](#project)
  * [Presentations](#presentations)
  * [Additional Materials](#additional-materials)
- [Grading](#grading)
  * [Grade Breakdown](#grade-breakdown)
  * [Letter Grades](#letter-grades)

## Lectures

The tentative schedule with PDF lecture notes is shown below (**refresh this page to view the lates changes**). The schedule will be updated when needed and significant changes will be announced in class.

| Lectures        | Date | Slides           | Additional material |
| --------------- |------|-----------------:| -----------:|
| Uniprocessors    | 01/06 | [Uniprocs.pdf](lectures/1_uniprocs.pdf) |  |
| Overview of HPC    | 01/08 | [HPC.pdf](lectures/1_hpc.pdf) |  |
| Introduction to parallel computing I     | 01/13 | [Parallel(I).pdf](lectures/Intro_to_parallel_computing(I).pdf) | |
| Introduction to parallel computing II     | 01/15 | [Parallel(II).pdf](lectures/Intro_to_parallel_computing(II).pdf) | |
| Introduction to C | 01/22 | [IntroC.pdf](lectures/2_cpp.pdf) | - C extensions for Python: https://cython.org/ <br/> - Code examples and documentation in the `C_code` folder |
| Submitting jobs on a cluster | 01/27 | [SLURM.pdf](lectures/2_sbatch.pdf) | ACCRE Tutorials: [Link](https://www.vanderbilt.edu/accre/getting-started/training/) |
| Shared-memory algorithms | 01/29 -- 02/10 | [Shared.pdf](lectures/Shared.pdf) | - Cilk code examples in the `Cilk_code` folder <br/> - Cilk installation guide on Brightspace with Homework 1 |
| GPU | 02/12 | [GPU.pdf](lectures/3_gpu.pdf) | Nvidia‘s CUDA parallel computation API from Python: [Link](https://mathema.tician.de/software/pycuda/) |
| GPU Performance | 02/17 | [GPU_perf.pdf](lectures/3_perf.pdf) | CUDA code examples in the `CUDA_code` folder. <br/> Short tutorial on how to run GPU programs on ACCRE can be found here: [ACCRE_guide.pdf](documentation/accre_gpu_guide.pdf)  |
| Interconect and communication | 02/19 | [Interconnect.pdf](lectures/Interconnect.pdf) | |
| Homework Review | 02/24 | | |
| MPI | 02/26, 03/09 | [MPI slides](http://ana-gainaru.com/MPI_Lectures) | MPI code examples in the `MPI_code` folder. <br/> MPI code examples used for the slides can be found [here](https://github.com/anagainaru/MPI_Lectures) |
| Distributied-memory algorithms I | 03/16 | [Distributed(I).pdf](lectures/Distributed(I).pdf) | |
| Midterm | 03/18 | | |
| Distributied-memory algorithms II | 03/23, 03/25 | [Distributed(II).pdf](lectures/Distributed(II).pdf) | |
| Parallel File System | 03/30 |  [PFS.pdf](lectures/4_pfs.pdf) | The two examples used in the slides can be found here: [PFS_example.pdf](lectures/4_pfs_example.pdf)|
| Scheduling I | 04/01 |  [BatchScheduler(I).pdf](lectures/5_scheduler.pdf) | |
| Scheduling II | 04/06 |  [BatchScheduler(II).pdf](lectures/5_scheduler2.pdf) | Batch Scheduler Simulator: [ScheduleFlow.zip](schedule_simulations/ScheduleFlow.zip)<br/> To run the examples from the slides: `cd examples`, `python generate_gif_example.py` <br/> GIF files can be found in ../draw <br/> Generating GIFs requires pdflatex and convert from ImageMagick <br/> Updates on [Github](https://github.com/anagainaru/ScheduleFlow) |
| Fault tolerance | 04/08 |  [FaultTolerance.pdf](lectures/6_fault_tolerance.pdf) | |
| Grad students presentations | 04/13 | Below |  Papers and presentations in the `research` folder |

**Grad students presentations**

| Paper        | Presenter | Slides           | Paper |
| --------------- |------|-----------------:| -----------:|
| A Three-Dimensional Approach to Parallel Matrix Multiplication | Damin Xia | [p1_slides.pdf](research/p1_slides.pdf) |  [p1_paper.pdf](research/p1_paper.pdf)  |
| Exposing Hidden Performance Opportunities in High Performance GPU Applications | Chloe Frame | [p2_slides.pdf](research/p2_slides.pdf) |  [p2_paper.pdf](research/p2_paper.pdf)  |
| GROMACS: High performance molecular simulations through multi-level parallelism from laptops to supercomputers | Quach Co | [p3_slides.pdf](research/p3_slides.pdf) |  [p3_paper.pdf](research/p3_paper.pdf)  |
| Strong scaling of general-purpose molecular dynamics simulations on GPUs | Duncan Steward | [p4_slides.pdf](research/p4_slides.pdf) |  [p4_paper.pdf](research/p4_paper.pdf)  |
| How Much Parallelism is There in Irregular Applications? | Xiaobo Liu | [p5_slides.pdf](research/p5_slides.pdf) |  [p5_paper.pdf](research/p5_paper.pdf)  |


### Midterm
The midterm material includes everything before the first MPI lecture (all the lectures including the one on 02/19). The topics include:
- Paradigms of parallel computing: data parallel, task parallel, pipelining, speed-ups
- Parallel architecture concepts: SIMD, vector machines, array processors, MIMD, uniform shared memory, nonuniform shared memory, distributed memory, distributed shared memory
- SPMD versus MIMD style programming
- Shared memory algorithms and performance models
- Concepts of GPU programming and differences between GPU and CPU
- Interconnection networks

> The crash course on C is NOT included in the midterm topics

The midterm is in written format, will include 6 questions and will last for one hour. The midterm is open notes.

Midterm date: **March 18th, 2020 (online)**


### Homeworks
All assignments are mandatory and part of the final grade. Assignments and homework should be turned in before or at the due date before midnight. When turned in late, 5% will be deducted from the project grade per day until the submission has been received, with a maximum extension of five days.

There will be 3 homeworks (equal weight in the final grade): 
* Shared memory (Cilk programming)
   * Link to homework 1: available on Brightspace
   * Deadline: *February 14th*
* Shared memory (GPU programming) 
   * Link to homework 2: available on Brightspace
   * Deadline: *March 20th*
* Distributed memory (MPI programming)
   * Link to homework 3: available on Brightspace
   * Deadline: *April 6th*

## Group Project

### Project

**The project is currently suspended due to the cancellation of all in-person classes. More details on how this will move forward will be announced later.**

**Update: The project is canceled.**

The project consists of parallelizing an algorithm (in any programming language) to solve a specific problem and analyzing the scalability and bottlenecks of the parallel code. The problem to be solved can be something from your field of study, a benchmark or one discussed in class (e.g. Sort, Marix Multiplication). If a simple problem is chosen, it will have to be implemented with multiple methods (e.g. different algorithms in shared memory CPU vs GPU, or shared vs distributed CPU) and the results will have to be compared with each other and explained. All chosen problems and algorithms must be approved.

**Groups** <br/>
This is a group project (2 or 3 students per team).

**Deadline** <br/>
Problem and algorithm choice must be sent for approval by **March 16th** with the complete list of team members.<br/>
Submission of the projects must be done before April 12th. <br/>
Each group will have to submit the codes and a small report describing the algorithm and code analysis.

**Presentations** <br/>
Presentations will be held on the last week of the class <br/>
Order of presentations will be decided by the instructors by the middle of March.

## Research paper presentations 
### Presentations
#### Only for grad students

Grad students need to choose a paper related to parallel/distributed programming, optimization, HPC, large-scale architectures/applications and present them in the last week of class. Chosen papers need to be approved. The following is a list of good candidate papers  (**email us your selections for approval before April 1st**). Feel free to chose one of these or something related to HPC from your field of study.

1) Milind Kulkarni, Martin Burtscher, Rajasekhar Inkulu, Keshav Pingali and Calin Cascaval. "How Much Parallelism is There in Irregular Applications?" Principles and Practices of Parallel Programming (PPoPP), February, 2009.

2) A.Y. Grama, A. Gupta, and V. Kumar. "Isoefficiency: Measuring the Scalability of Parallel Algorithms and Architectures," Parallel & Distributed Technology: Systems & Applications, IEEE, see also IEEE Concurrency, Volume 1, Issue 3, Aug. 1993, pp. 12-21.

3)  S. Srinivasan, R. Kettimuthu, V. Subramani and P. Sadayappan, "Characterization of backfilling strategies for parallel job scheduling", Proceedings. International Conference on Parallel Processing Workshop, 2002

4) W. Daniel Hillis and Guy L. Steele. "Data Parallel Algorithms," Communications of the ACM, December 1986, pp. 1170-1183.

5) David E. Culler, Richard M. Karp, David Patterson, Abhijit Sahay, Eunice E. Santos, Klaus Erik Schauser, Ramesh Subramonian, Thorsten von Eicken. "LogP: A Practical Model of Parallel Computation," Communications of the ACM, Volume 39, Issue 11, November 1996, pp. 78 - 85.

6) V. Nageshwara Rao and Vipin Kumar. "Superlinear Speedup in Parallel State-Space Search," Lecture Notes In Computer Science, Vol. 338, Proceedings of the Eighth Conference on Foundations of Software Technology and Theoretical Computer Science, pp. 161-174, 1988.

7) R. C. Agarwal, S. M. Balle, F. G. Gustavson, M. Joshi, and P. Palkar. "A Three-dimensional Approach to Parallel Matrix Multiplication," IBM Journal of Research and Development, Volume 39, Number 5, 1995.

8) Fabrizio Petrini, Darren J. Kerbyson, Scott Pakin. "The Case of the Missing Supercomputer Performance: Achieving Optimal Performance on the 8,192 Processors of ASCI Q," Conference on High Performance Networking and Computing, Proceedings of the 2003 ACM/IEEE Conference on Supercomputing, 2003.

9) J.T.Daly, "A higher order estimate of the optimum checkpoint interval for restart dumps", Future Generation Computer Systems, Volume 22, Issue 3, Pages 303-312, February 2006

**The submission will be done on Brightspace:** 
* Students will have to prepare slides (1-2 slides for each):
   * Describing what the paper is trying to solve
   * The current state-of-the-art related to the problem tackled by the paper
   * What is the paper bringing new compared to the state-of-the-art
   * Details on the implementation that is solving the problem
   * Results
   * Students optinion on the paper

* The slides will be uploaded on the website and will be accessible to all the other students
* Deadline: *April 13th*

## Additional Materials

The material in this section is not required for this class. The following books give a good detailed overview to multiple HPC related topics.

 * *"Software Optimization for High Performance Computing: Creating Faster Applications"* by K.R. Wadleigh and I.L. Crawford, Hewlett-Packard professional books, Prentice Hall.<br/>
 * *"The Software Optimization Cookbook"* (2nd ed.) by R. Gerber, A. Bik, K. Smith, and X. Tian, Intel Press.<br/>
 * *"Parallel Programming: Techniques and Applications using Networked Workstations and Parallel Computers"* (2nd ed.) by B. Wilkinson and M. Allen, Prentice Hall.<br/>
 * *"Parallel Scientific Computing in C++ and MPI"* by G. Karniadakis and R. Kirby II, Cambridge University Press.<br/>
 * *"Scientific Parallel Computing"* by L.R. Scott, T. Clark, and B. Bagheri, Princeton University Press.<br/>
 * *"Sourcebook of Parallel Programming"* by J. Dongara, I. Foster, G. Fox, W. Gropp, K. Kennedy, L. Torczon, and A. White (eds), Morgan Kaufmann.
 * *"Designing and Building Parallel Programs: Concepts and Tools for Parallel Software Engineering"* by I. Foster, Addison-Wesley Longman Publishing Co., Inc. <br/>
 * *"Introduction to Parallel Computing (2nd ed.)"* by A. Grama, A. Gupta, G. Karypis, V. Kumar. Addison-Wesley Professional <br/> 
 * *"Introduction to Algorithms (3rd ed.)"* by T. H. Cormen, C. E. Leiserson, R. L. Rivest, and C. Stein. MIT Press and McGraw-Hill. <br/> 
 * *"Parallel Algorithms"* by H. Casanova, A. Legrand, Y. Robert. Chapman & Hall/CRC. 


## Grading

### Grade Breakdown

**Honor Code Violations**
All exams and assignments must be completed individually, unless stated otherwise. Copying solutions is considered cheating. Submitted source code listings will be compared. Keep a copy of the listings to provide evidence of creative work. Students are expected to uphold the Honor Code. Any student involved in cheating is in violation of the Honor code. Consult the "Student Handbook" for more details on the Honor code.

| Percentage grade | Undergraduate credit	| Graduate credit |
|------------------|----------------------|-----------------|
| Midterm exam | 40% | 40% |
| Homework	| 60%	| 45% |
| Research article presentation | n/a | 15% |

### Letter Grades

| A |B|C|
|----------|-------------|------------|
| 94-100%	A+	| 76-81%	B+ |	56-61%	C+|	
| 88-93%	A |	70-75%	B | 50-55%	C	| 
| 82-87%	A- |	62-69%	B- |	42-49%	C- | 

