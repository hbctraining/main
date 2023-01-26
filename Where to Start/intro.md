## This page is for people who are feeling overwhelmed and lost

* Are you keen on data analysis but not really sure where to start?
* Does the idea of writing your own code seem exciting yet daunting?
* Do you have a general idea of what is involved with high throughput sequencing data, but eager to learn more?


### If this fits you then you are on the right page! 

Let's start by trying to understand some important concepts. 

**A bit hestitant to describe/focus all 'omics' since we don't really teach all of them.**

## What is Big data?

A paragraph on data types, data formats, standards, metadata and data management strategies (of course, I had to try and get this in here ;) ).


## What kind of data do we see in biomedical research?

A commonly encountered type of big data in biomedical research is genomic and transcriptomics data. 

* genOMICS - The study of the complete set of **DNA** in an organism, sigle cells, or group of cells.
* transcriptOMICS - The study of the complete set of **RNA** in an organism, sigle cells, or group of cells.

The most common way to interrogate the transcritptome and genome is using **high throughput sequencing**. 

## What is High Throughput Sequencing (HTS)?

Genomes and transcriptomes, etc are massive data sets containing hundreds of millions or billions of [base pairs](https://en.wikipedia.org/wiki/Base_pair) (A,T,G,C). For a comparison, an average length book might have about 375,000 characters. Reading those bases one at a time will take too long even for a fast machine. **H**igh **T**hroughput **S**equencing (HTS) is when multiple DNA or RNA moleculars are sequenced in parallel (i.e., at the same time). This leads to hundreds of millions of molecules being sequenced at one time. Because only DNA and RNA are sequenced, HTS is used for genomics and transcriptomics. However, newer methodologies allow information about chromatin and proteins to be incorporated with this data.

## What is a high performance cluster (HPC) environment?

Define a cluster ---
Let's take a quick look at the basic architecture of a cluster environment and some cluster-specific jargon.

<p align="center">
<img src="img/cluster.png" width="500">
</p>

The above image reflects the many computers that make up a **"cluster"** of computers. Each individual computer in the cluster is usually a lot more powerful than any laptop or desktop computer we are used to working with, and is referred to as a **"node"** (instead of computer). Each node has a designated role, either for logging in or for performing computational analysis/work. **A given cluster will usually have a few login nodes and several compute nodes.** Each individual node in an HPC environment is a lot **more powerful** than any laptop or desktop computer we are used to working with. What we mean by *powerful* here is that each of these nodes have:

  * a lot more memory (temporary storage)
  * many more, faster CPUs
  * each of those CPUs has many more cores

## Do I need a HPC for analyses, when I have a pretty good laptop?

Let's return to our book example. If one book is 375,000 characters then 3.2 billion characters (the size of the human genome) translates to 8,533 books! While we might keep tens or even hundreds of books at our house, most people will never have thousands. 

<p align="center">
<img src="img/library.jpg" width="500">
</p>
<p align = "center">
Can you imagine dusting this?
</p>


It's the same with our local computer.  While we might keep small data files on our laptop, we don't want to clutter it up with huge data files. And this is just thinking about storage! Books or data sets need to be organized and kept track of as well. You might be able to alphabetize or organize a hundred books on your own but working with >8,000 books would be overwhelming! The same goes for our computer. To organize billions of basepairs and make sense of our sequencing data we simply need more power. Your "pretty good" laptop might have 16 cores. In comparison, a high perfomance computing (HPC) cluster might have hundreds of cores. That is a lot more power for the big computational work we want to do!

E.g. A cluster “Node” that has eight “quad"-core CPUs, means that node has 32 cores (ability to process 32 computations at a time).


### Why use the cluster or an HPC environment?

1. A lot of software is designed to work with the resources on an HPC environment and is either unavailable for, or unusable on, a personal computer.
2. If you are performing analysis on large data files (e.g. high-throughput sequencing data), you should work on the cluster to avoid issues with memory and to get the analysis done a lot faster with the superior processing capacity. Essentially, a cluster has:
    * 100s of cores for processing!
    * 100s of Gigabytes or Petabytes of storage!
    * 100s of Gigabytes of memory!



## What is shell and how does it relate to clusters?

So how might you actually use a cluster? Unfortunately you can't just walk up to where the cluster is stored and start using it. Clusters are accessed remotely, that means that you connect to the cluster from your own computer. You will do this from the **command line** or a text based user interface. We are used to a point and click environment on our laptops. We are comfortable using our mouse to click on applications we want to use and selecting various commands from dropdown menus. Unfortunately, our mouse is pretty useless when working on the command -line.

<p align="center">
<img src="img/fasRC.jpeg" width="650">
</p>
<p align = "center">
The FAS-RC Cluster
</p>

Any task that you want a cluster to do has to be communicated through text. If you have never taken a computer science course or worked with clusters before this will all be brand new to you. 

The **shell** is what runs in these programs to interpret your commands. These programs all use [Bash](https://en.wikipedia.org/wiki/Bash_Unix_shell), a command language. As you get into HTS and computational work you will encounter a lot of languages such as python, perl, fortran, R, c++, java and more. You can think of these as being akin to human languages; French and English sound very different and have different syntax (the order of words) but can be used to convey the same message. At HBC training we recommend that you become familiar (or fluent) in bash and R.  

## What is R and what can it do?

<INSERT AN R IMAGE HERE>

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

Hopefully you now feel like you have a grasp on some of these terms. If you want to start getting your hands wet, we recommend that you take a look at our training program. <INCLUDE LINK TO THE MAIN_DRAFT PAGE HERE?>
 
 Happy Computing!




