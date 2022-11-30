## This is for people who are feeling overwhelmed and lost


* Are the words 'omics, HTS, R programming, shell, and computer cluster new for you?
* Are you unsure how to start getting comfortable with large data sets?
* Have you never written a single line of code?


### If this fits you then you are on the right page! 

Let's start by trying to understand what 'omics data, HTS, computer clusters, shell, and R are and who might need to use them.


## What the heck is 'omics?

New sequencing technologies (often abbreviated **NGS for next generation sequencing**) now allow us to look at the entirety of a certain type of data in an organsim. To put it another way, scientists used to be limited to studying one gene, one protein etc. 'omics data encompasses the entirety genes, proteins, etc in a cell or organism. We can break 'omics down into specific categories

* genOMICS - The study of the complete set of **DNA** in an organism, sigle cells, or group of cells
* transcriptOMICS - The study of the complete set of **RNA** in an organism, sigle cells, or group of cells
* proteOMICS - The study of the complete set of **Proteins** in an organism, sigle cells, or group of cells
* metabolOMICS - The study of the complete set of **Metabolites** in an organism, sigle cells, or group of cells


## How does High Throughput Sequencing relate to 'omics?

**H**igh **T**hroughput **S**equencing (HTS) is when multiple DNA or RNA moleculars are sequenced in parallel (i.e., at the same time). This leads to hundreds of millions of molecules being sequenced at one time. Because only DNA and RNA are sequenced HTS is used for genomics and transcriptomics. However, newer methodologies allow information about chromatin and proteins to be incorporated with this data.

## How do clusters relate to HTS?
Data too big! need cluster! See below for more info on clusters.

## What is shell and how does it relate to clusters
Need shell to run cluster!


## What is R and what can it do?

What R is and why it is the best


## More on clusters


Let's take a quick look at the basic architecture of a cluster environment and some cluster-specific jargon.

<p align="center">
<img src="img/cluster.png" width="500">
</p>

The above image reflects the many computers that make up a **"cluster"** of computers. Each individual computer in the cluster is usually a lot more powerful than any laptop or desktop computer we are used to working with, and is referred to as a **"node"** (instead of computer). Each node has a designated role, either for logging in or for performing computational analysis/work. **A given cluster will usually have a few login nodes and several compute nodes.**

The data on a cluster is also stored differently than what we are used to with our laptops and desktops, in that it is not computer- or node-specific storage, but all of the data is available to all the nodes in a cluster. This ensures that you don't have to worry about which node is working on your analysis.


The above image shows us the many nodes (or computers) that make up a **"cluster"** of computers. Each individual node in an HPC environment is a lot **more powerful** than any laptop or desktop computer we are used to working with. What we mean by *powerful* here is that each of these nodes have:

  * a lot more memory (temporary storage)
  * many more, faster CPUs
  * each of those CPUs has many more cores

E.g. A cluster “Node” that has eight “quad"-core CPUs, means that node has 32 cores (ability to process 32 computations at a time).

**A note about data on the cluster:** One thing that each of these powerful cluster nodes **do not have** is **large amounts of data storage** capability. Instead, all the data on a cluster is stored in a set of **shared disks** connected to all the nodes on the cluster. The data storage disks and nodes usually have very high-speed connectivity between them to avoid any data access lags. 

### Why use the cluster or an HPC environment?

1. A lot of software is designed to work with the resources on an HPC environment and is either unavailable for, or unusable on, a personal computer.
2. If you are performing analysis on large data files (e.g. high-throughput sequencing data), you should work on the cluster to avoid issues with memory and to get the analysis done a lot faster with the superior processing capacity. Essentially, a cluster has:
    * 100s of cores for processing!
    * 100s of Gigabytes or Petabytes of storage!
    * 100s of Gigabytes of memory!

### Parallelization

Point #2 in the last section brings us to the idea of **parallelization** or parallel computing that enables us to efficiently use the resources available on the cluster.

#### One input file

Let's start with the most basic idea of processing 1 input file to generate 1 output (result) file. On a personal computer this would happen with a single core in the CPU. 

<p align="center">
<img src="img/serial_hpc_crop.png" width="50">
</p>

On a cluster we have access to many cores on a single node, so in theory we could split up the analysis of a single file into multiple distinct processes and use as many cores to speed up the generation of an output file. This is called **multithreading**, i.e. using multiple threads or cores. As you can imagine, multithreading can speed up how fast the analysis is performed! In the example below, the input file is analyzed using 8 cores, likely resulting in an 8 fold speed up!

<p align="center">
<img src="img/multithreaded_hpc.png" width="450">
</p>

> **Note:** Multithreading is done internally by analysis tools being employed, and **not** by manually splitting the input (except in very unusual circumstances).

#### Three input files

Now, what if we had 3 input files? Well, we could process these files **in serial**, i.e. use the same core(s) over and over again, as shown in the image below.

<p align="center">
<img src="img/serial_hpc_3samples.png" width="450">
</p>

This is great, but it is not as efficient as multithreading each analysis, and using a set of 8 cores for each of the three input samples. This is actually considered to be true parallelization.

<p align="center">
<img src="img/multithreaded_hpc_3samples.png" width="650">
</p>

With parallelization, several samples can be analysed at the same time!

