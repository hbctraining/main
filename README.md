# Training program description:

The training team at the Harvard Chan Bioinformatics Core provides bioinformatics training through both shorter workshops and longer in-depth courses. Our current workshops and courses are designed to help biologists become comfortable with using tools to analyse high-throughput data. We are slowly beginning to expand this repertoire to include training for researchers with more advanced bioinformatics skills. See our current workshop schedule on our [training website](http://bioinformatics.sph.harvard.edu/training/).

**We are excited to announce the launch of HBC's new training program for 2019!**

This semester *we are piloting a new learning model* that replaces the 3-day workshops we have previously offered for **eligible researchers**. 

While all of the content will remain the same as past workshops, we are changing the format to be *more modular*. We have divided our training content into the two categories listed below. Any participants wanting to take an [advanced workshop](#advanced-topics-analysis-of-high-throughput-sequencing-ngs-data) will have to have taken certain [basic workshop(s)](#basic-data-skills) within the past 6 months. 

* [Basic Data Skills](#basic-data-skills) - No prior programming knowledge needed (no prerequisites)
* [Advanced Topics: Analysis of high-throughput sequencing (NGS) data](#advanced-topics-analysis-of-high-throughput-sequencing-ngs-data) - Certain "Basic" workshops required as prerequisites.

We are structuring the training schedule such that it gives interested researchers several opportunities to take the basic workshops. 

| Topic | Category | Duration | Prerequisites |
| :----: | :----: | :----: | :----: |
| Introduction to the command-line interface (shell) | Basic | 1 day | None |
| Introduction to R | Basic | 1.5 days | None |
| [Introduction to the command-line interface (shell)](https://wiki.harvard.edu/confluence/pages/viewpage.action?pageId=233092746) | Basic | 1 day | None |
| Bulk RNA-seq analysis| Advanced | 2 days | Intro to shell |
| Differential gene expression analysis (bulk RNA-seq) | Advanced | 2 days | Intro to R |
| ChIP-seq analysis | Advanced | 2 days | Intro to R **&** shell |
| Single-cell RNA-seq analysis | Advanced | 2 days | Intro to R **&** shell **&** Differential gene expression |

***

## Basic Data Skills

These are short 1-1.5 day workshops that provide an introduction to computational skills required for someone to get started with analyzing high-throughput sequencing data independently. These have no prerequisites and do not require any prior experience with programming. 

We will alternate between two basic topics in the schedule, with at least one basic offering every month. *The completion of one or more of these workshops is required in order to register for the [workshops on advanced topics](#advanced-topics-analysis-of-high-throughput-sequencing-ngs-data).*

### Introduction to command-line interface (Unix/shell/Linux/bash)

In this 1-day hands-on workshop, participants will learn basic commands for navigating the file system, exploring file contents, and performing basic operations, such as moving, copying, and renaming files/folders. In addition, participants will get an introduction to high-performance computing (HPC).

### Introduction to R
This 1.5-day workshop will introduce participants to the basics of using R and RStudio, a simple programming environment that enables the effective handling of data, while providing excellent graphical support.

Participants will learn how to use R for:
* exploring basic data structures
* inspecting and wrangling data
* installing & working with data analysis packages
* making publication-quality plots with the ggplot2 package

***

## Advanced Topics: Analysis of high-throughput sequencing (NGS) data

These are 2-day intensive workshops that instruct participants on how to efficiently manage and analyze data, with a focus
on the workflow for a specific type of next-generation sequencing data (i.e RNA-seq, ChIP-seq). *These workshops require participants to have taken one or more of the [Basic Data Skills workshops](#basic-data-skills) as listed in the table below.*

| Topic | Prerequisites |
| :----: | :----: |
| [Introduction to (bulk) RNA-seq using High-Performance Computing](#rna-seq-analysis-from-raw-data-to-gene-expression-counts) |  Introduction to shell |
| [Introduction to Differential Gene Expression Analysis](#differential-gene-expression-analysis-using-gene-expression-counts-from-the-above-workshop)  |  Introduction to R  |
| [Introduction to ChIP-seq Analysis](#chip-seq-analysis) |  Introduction to R & shell |
| [Introduction to single cell RNA-seq Analysis](#single-cell-rna-seq) | Introduction to R & shell |

### RNA-seq Analysis (from raw data to gene expression counts)
This 2-day hands-on workshop will cover the basics of bulk RNA-seq analysis; from designing a good experiment to performing QC on sequencing data to obtaining gene expression matrices. All the analysis will be performed on HMS-RC's O2 cluster.

### Differential Gene Expression Analysis (using gene expression counts from the above workshop)
This 2-day hands-on workshop will cover the statistical considerations when using RNA-seq data for differential gene expression analysis, followed by using DESeq2 to obtain lists of differentially expressed (DE) genes. In addition, this workshop will cover tools that will enable broader functional analysis on the DE gene lists. All the analysis will be performed using R (RStudio).

### ChIP-seq analysis
This 2-day hands-on workshop will cover the basics of ChIP-seq analysis; from designing a good experiment to peak calling and performing a multitude of QC steps. This workshop requires participants to have a working knowledge of both R and shell, since we will be using HMS-RC's O2 cluster for some of the work and doing other analyses locally.

### Single cell RNA-seq
This workshop will be either 2 or 3 days long. This workshop also requires participants to have a working knowledge of both R and shell. *More details coming soon!*

### Current topics in bioinformatics series:

These short workshops (half-day or less) are designed to allow researchers, who have some familiarity with R or bash, to learn new tools and methods. For the short workshops topics please [click here](https://hbctraining.github.io/Training-modules/).


### In-Depth Next Generation Sequencing Analysis Course

[This intensive course](https://hbctraining.github.io/In-depth-NGS-Data-Analysis-Course/) runs for between **8 to 12 days** and is aimed at bench biologists interested in learning how to **independently** perform NGS data analyses using *best practices*. Topics include:

  * High-performance computing
  * Best practice workflows for NGS data analysis (RNA-seq, ChIP-seq, Variant calling)
  * R for statistical analysis and data visualization
  * Functional analysis with gene lists
  * Additional skils and tools for better reproducibility like reports with RMarkdown, version control with Git/Github, etc.

## Contact us:

**Email:** [hbctraining@hsph.harvard.edu](mailto:hbctraining@hsph.harvard.edu)

**Webpage:** [http://bioinformatics.sph.harvard.edu](http://bioinformatics.sph.harvard.edu)

**Twitter:** [@bioinfocore](http://twitter.com/bioinfocore)
