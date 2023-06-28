## Framework for development of a longer workshop on applications of NGS/HTS

* Determine pre-req, if applicable
* Introduction to the application
  * Presentation given by an external expert speaker or someone from tt if they have expertise
* Introduction to the dataset with the big picture biological picture in mind (why someone might choose to use this specific application of NGS/HTS)
  * Workflow diagram to explain
  * Explain how (if needed) the dataset was subsetted
* Directory organization with a focus on data management
* Run the workflow steps in R or interactively on HPC (fastqc, alignment, other QC, filtering).
  * Emphasize the biological context of each step
  * Explain statistical or algorithmic elements in some depth and provide links for more in-depth study
  * These lessons/sections are to describe tools, parameters and parameter choices. Essentially the "Whys and "Hows".
* For HPC based workshops create a shell-based (or nf-core based?) pipeline for full analysis
  * Pipeline should have usage at the top
  * Any hard coded variables should be clearly marked
  * Should be parallelizable for all samples/samplegroups with job arrays or similar
* Downstream analysis lessons should focus on biological significance and visualization of results
  * If adding other tools, make sure to include a description of tools, parameters and parameter choices and very importantly the interpretation and connection to the biological context (tie it back to the first lesson on dataset description)
