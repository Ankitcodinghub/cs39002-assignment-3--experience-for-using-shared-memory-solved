# cs39002-assignment-3--experience-for-using-shared-memory-solved
**TO GET THIS SOLUTION VISIT:** [CS39002 Assignment 3- Experience for using shared-memory  Solved](https://www.ankitcodinghub.com/product/cs39002-assignment-3-experience-for-using-shared-memory-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100364&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS39002 Assignment 3- Experience for using shared-memory&nbsp; Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="section">
<div class="layoutArea">
<div class="column">
Hands-on experience for using shared-memory

In this assignment you will learn how to use shared memory to communicate between processes and in turn make your computation faster by dividing compuations. There are two tasks in this assignment.

Task 1: [15 marks]

</div>
</div>
<div class="layoutArea">
<div class="column">
a)

</div>
<div class="column">
For this assignment, you will be writing a program for matrix-multiplication. Let A and B be two input matrices of sizes 𝑟1 * 𝑐1

and 𝑟2 * 𝑐2respectively, where 𝑐1 = 𝑟2. You will be implementing the naïve matrix multiplication algorithm, where each element of the result

matrix C of size 𝑟1 * 𝑐2can be computed independently from one

another. The overall scheme for implementation is:

<ul>
<li>Create a function void *mult(void *arg): which multiplies a row
of matrix A with a column of matrix B, and stores the result in the appropriate cell of preallocated matrix C, all in shared memory.
</li>
<li>The argument arg is a structure of type ProcessData, which stores the input and output parameters for the function shown below. Note that the actual matrix data is stored in the shared memory and is accessible to all.</li>
<li>In the main program, create child processes to compute all the elements of the matrix C.
The structure for passing parameters can be:
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
compute A[i,:] * B[:,j] and store in

</div>
</div>
<div class="layoutArea">
<div class="column">
//

C[i,j] typedef struct _process_data {

</div>
</div>
<div class="layoutArea">
<div class="column">
double **A; double **B; double **C;

int veclen, i, j;

} ProcessData;

<ul>
<li>// &nbsp;veclen: 𝑐1/𝑟2</li>
<li>// &nbsp;i, j: cell to compute
In this part you should simply create 𝑟1 * 𝑐2 child processes each for computing each element. Note that no mutual exclusion is needed as all
</li>
</ul>
</div>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="section">
<div class="layoutArea">
<div class="column">
the output entries are created independently and all the inputs are already available.

b) The problem with the above implementation is that you have to allocate memory for 𝑟1 * 𝑐2 processes and input arguments. However, in most

practical systems you will not have enough cores to execute all the processes concurrently. Keeping this in mind, what is the maximum size of matrix that you can multiply(in terms of 𝑟1 * 𝑐2). Show your

reasoning/calculation. Include this in a report (See submission guidelines).

Task 2: [35 marks](30+5)

Implement a producer / worker system using shared memory, which can

multiply a sequence of matrices block-wise:

<ol>
<li>a) &nbsp;Your program will first read the values of NP (number of producers) and NW (number of workers), and create the required number of producer and worker processes. It will also take the total number of matrices to multiply as an input.</li>
<li>b) &nbsp;Create a shared memory segment SHM, which is shared among all the producer and consumer processes spawned by your code. The shared memory segment will contain a standard queue of finite size (say, can hold 8 elements). It will also create a job_created counter (integer) in the shared memory, which will store the number of matrices already generated.</li>
<li>c) &nbsp;Each producer process should generate a computing job, wait for a random interval of time between 0 and 3 seconds, and insert the computing job in the shared memory queue SHM. After insertion, the producer will repeat the process. Each computing job is represented by a structure which contains the following elements at a minimum:
<ol>
<li>i) &nbsp;producer number</li>
<li>ii) &nbsp;status of the matrix multiplication</li>
<li>iii) &nbsp;a matrix of size NxN; N=1000</li>
<li>iv) &nbsp;a matrix id</li>
</ol>
The matrix id is a random integer between 1 and 100000, elements of the matrix should be randomly between -9 and +9. The producer generates each of these three numbers randomly while creating a job. The status can be set according to your needs.
</li>
<li>d) &nbsp;While insertion, if the queue has no empty space, the producer waits until more space becomes available. It will also print the producer number, pid</li>
</ol>
</div>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
and details of the job generated. Then the producer will increase the jobs_created counter by 1.

<ol start="5">
<li>e) &nbsp;Each worker process waits for a random interval of time between 0 and 3 seconds, retrieves two blocks of the first two matrices in the queue, and updates the status as required. The block-wise multiplication is described below:
Let M = N/2. Break the matrices into M × M blocks. We want to multiply C = A* B

A = |A00 A01| |A10 A11|

B = |B00 B01| |B10 B11|

C = |C00 C01| |C10 C11|

For each I, J, K ∈ {0,1}, define the block product DIJK = AIK * BKJ For each I, J ∈ {0,1}, we then have CIJ = DIJ0 +DIJ1

Each worker process will calculate a DIJK in its local memory, and then copy/add it to a new element in the SHM queue to store CIJ. Thus to multiply two matrices you need 8 worker processes working on it.

When the first worker starts to access the blocks, add a new memory segment to store the resultant matrix at the back of the queue.

After the 8 workers have accessed all the blocks, remove the first two memory segments from the SHM queue.

If a worker finds that all 8 blocks of the first two memory segments have been accessed, it does nothing and waits for the next job.

The process which first accesses the block CIJ copies its local block product to CIJ. The second process to access CIJ adds its local block product to CIJ. The status variable can be used to map out which blocks of matrices have been processed already, and which are remaining.

Whenever a worker fetches or writes a block, print an appropriate status message stating: worker number, producer numbers, Matrix IDs, block numbers and the work done (reading/copying/adding the blocks).
</li>
<li>f) &nbsp;The parent process (i.e., your code) will wait till job_created counter reaches a specified number of jobs (e.g., 10), and only 1 element remains in the queue. Output the total time taken to run those specified number of</li>
</ol>
</div>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="section">
<div class="layoutArea">
<div class="column">
jobs, along with the sum of the elements in the principal diagonal of the final matrix and then kill the process.

g) [BONUS]: use mutex locks to prevent concurrent updation to shared variables leading to possible race conditions. [5 marks]

</div>
</div>
</div>
</div>
