## This page is for people who are feeling overwhelmed and lost


* Are the words 'omics, HTS, R programming, shell, and computer cluster new for you?
* Are you unsure how to start getting comfortable with large data sets?
* Have you never written a single line of code?


### If this fits you then you are on the right page! 

Let's start by trying to understand what 'omics data, HTS, computer clusters, shell, and R are and who might need to use them.


## What the heck is 'omics?

Using methods such as Sanger sequencing and allozymes scientists used to be able to study just a few genes at a time. However, new sequencing technologies (often abbreviated **NGS for next generation sequencing**) now allow us to look at the entirety of a certain type of data in an organsim. This data, called 'omics data, encompasses the entirety of the genes or proteins etc in a cell or organism. We can break 'omics down into 4 specific categories:

* genOMICS - The study of the complete set of **DNA** in an organism, sigle cells, or group of cells.
* transcriptOMICS - The study of the complete set of **RNA** in an organism, sigle cells, or group of cells.
* proteOMICS - The study of the complete set of **Proteins** in an organism, sigle cells, or group of cells.
* metabolOMICS - The study of the complete set of **Metabolites** in an organism, sigle cells, or group of cells.

'Omics does not put a limit on the number of biological or technical replicates. So even if you are studying the genome of a single individual it is considered 'omics data. However, we usually are looking at data from large number of biological samples (individuals, cell lines, etc).

## How does High Throughput Sequencing relate to 'omics?

Genomes and transcriptomes, etc are massive data sets containing hundreds of millions or billions of [base pairs](https://en.wikipedia.org/wiki/Base_pair) (A,T,G,C). For a comparison, an average length book might have something like 375,000 characters. Reading those bases one at a time will take too long even for a fast machine. **H**igh **T**hroughput **S**equencing (HTS) is when multiple DNA or RNA moleculars are sequenced in parallel (i.e., at the same time). This leads to hundreds of millions of molecules being sequenced at one time. Because only DNA and RNA are sequenced, HTS is used for genomics and transcriptomics. However, newer methodologies allow information about chromatin and proteins to be incorporated with this data.

## How do clusters and HPC relate to HTS?
Let's return to our book example. If one book is 375,000 characters then 3.2 billion characters (the size of the human genome) translates to 8,533 books! So while we might keep 10s or even hundreds of books at our house most people will never have thousands. 

<p align="center">
<img src="img/library.jpg" width="500">
</p>
<p align = "center">
Can you imagine dusting this?
</p>


Same with our local computer, while we might keep small data on our laptop we don't want to clutter it up with huge data files. And this is just storage! You might be able to alphabetize or organize a hundred books but >8,000 books would be every overwhelming! The same goes for our computer. To organize billions of basepairs and make sense of our sequencing data we simply need more power. The mac laptop I am writing this on has 10 cores. A high perfomance computing (HPC) cluster might have hundreds of cores! That is a lot more power for the big computational work we want to do.

Let's take a quick look at the basic architecture of a cluster environment and some cluster-specific jargon.

<p align="center">
<img src="img/cluster.png" width="500">
</p>

The above image reflects the many computers that make up a **"cluster"** of computers. Each individual computer in the cluster is usually a lot more powerful than any laptop or desktop computer we are used to working with, and is referred to as a **"node"** (instead of computer). Each node has a designated role, either for logging in or for performing computational analysis/work. **A given cluster will usually have a few login nodes and several compute nodes.** Each individual node in an HPC environment is a lot **more powerful** than any laptop or desktop computer we are used to working with. What we mean by *powerful* here is that each of these nodes have:

  * a lot more memory (temporary storage)
  * many more, faster CPUs
  * each of those CPUs has many more cores

E.g. A cluster “Node” that has eight “quad"-core CPUs, means that node has 32 cores (ability to process 32 computations at a time).

The data on a cluster is also stored differently than what we are used to with our laptops and desktops, in that it is not computer- or node-specific storage, but all of the data is available to all the nodes in a cluster. This ensures that you don't have to worry about which node is working on your analysis.

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

## What is shell and how does it relate to clusters?

So how might you actually use a cluster? Unfortunately you can't just walk up to where the cluster is stored and start using it. Clusters are accessed remotely, that means that you connect to the cluster from your own computer. You will do this from the **command line** or a text based user interface. We are used to clicking on applications we want to use and selecting various commands from dropdown menus. Clusters do not work this way. Any task that you want a cluster to do has to be communicated through text.

<p align="center">
<img src="img/fasRC.jpeg" width="650">
</p>
<p align = "center">
The FAS-RC Cluster
</p>

If you have never taken a computer science course or worked with clusters before this will all be brand new to you. But don't worry, we have [courses for that](https://hbctraining.github.io/Intro-to-shell-flipped/schedule/links-to-lessons.html)! For now let's just review the basics. To look at command line on your own computer you can open the terminal program in macs or the download the [Git BASH](https://gitforwindows.org/) or [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) program for windows. The shell what runs in these programs to interpret your commands. These programs all use [Bash](https://en.wikipedia.org/wiki/Bash_Unix_shell), a command language. As you get into HTS and computational work you will encounter a lot of languages such as python, perl, fortran, R, c++, java and more. You can think of these as akin to human languages, French and English sound very different and have different syntax (the order of words) but can be used to convey the same message. At HBC training we recommend that you become familiar (or fluent) in bash and R.  

## What is R and what can it do?

Why do we recommend R instead of other languages? According to [R-project](https://www.r-project.org/about.html) R is "R is a language and environment for statistical computing and graphics." R is also a well developed and relatively simple language that is widely used among data scientists and people in STEM. Compelling arguements for learning R include:

* It’s open-source. This means no fees or licenses are needed and you won't get any pop ups asking for money.
* It’s platform-independent. This means that R runs on all operating systems (mac, windows, unix) and R scripts written on on platform can be run on any other platform.
* People write packages for R. The R language has more than 10,000 packages stored in the CRAN repository, and that number is continuously increasing. Many packages for analyzing HTS data are written for R such as DESeq2 and Seurat among other.
* Data wrangling, i.e., turning raw data into the desired format. Data wrangling is necessary for working with any 'omics data set and R has many packages that can turn unstructured, messy data into a structured format.
* Great plotting programs. R has wonderful packages to make publication ready figures. We even have a [workshop](https://hbctraining.github.io/Training-modules/publication_perfect/) devoted to it!
* It’s great for statistics. Unlike SAS which is very costly R is free and has many different statistical packages available.
* You can use R for Machine Learning. R is ideal for machine learning operations such as regression and classification and even for artificial neural network development.
* R is growing. R has a solid support program and help with issues is widely available. New packages and features are available regularly! 

## Where do I go from here?

Hopefully you now feel like you have a grasp on some of these terms. If you want to start getting your hands wet, we recommend that you take our [Intro to R Course](https://hbctraining.github.io/Intro-to-R-flipped/schedules/links-to-lessons.html) and the appropriate shell intro for the cluster you will use, either [O2](https://hbctraining.github.io/Intro-to-shell-flipped/schedule/links-to-lessons.html) or [FAS-RC](https://hbctraining.github.io/Intro-to-shell-fasrc-flipped/schedule/links-to-lessons.html). You are free to take a workshop with us or work through the lessons yourself at your own pace. See our [main page](https://hbctraining.github.io/main/) for all course offerings. Happy Computing!




