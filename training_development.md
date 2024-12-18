# Training Development Guidelines

This is a guide to help create continuity across our training materials. It is a living document and will try to be maintained to the best of our ability.

# Course Design Philosophy

## Backward Design

"Traditional" course design is often regarded as a process through which the instructor develops materials and then uses the principles from those materials to create an assessment. The "downfall" of this strategy is that it can result in teaching things that aren't assessed and can sometimes feel a bit meandering in the learning. 

Backward Design principles are a set of principles for course design which focus on how students will be assessed and then work to develop materials that align with those assessment goals. When we apply backward design principles in our course development it should follow these steps:

1. Identify what goal we want participants to accomplish
2. Create an assessment that will certify that the goal was obtained
3. Develop materials aimed at ensuring that students will be successful at the assessment

When you are planning a workshop or a lesson it can be really helpful to develop, even if it is very rudimentary (you can always come back to this) what exercises you want the participants to do first. This will tremendously help guide your development process, because you will be developing *toward* an assessment.

Vanderbilt has a nice [webpage](https://cft.vanderbilt.edu/guides-sub-pages/understanding-by-design/) on Backward Design.

## Work as a team

When working on developing course materials, if can be helpful to work as a team. This has a few advantages over solo course development:

1. Spreads the course development workload
2. Gives you a sounding board for ideas
3. Helps keep the development on track with someone else holding you accountable
4. Gives a different perspective on material
5. More fun to be doing it with someone else

What we have found when people work alone on material development is that it can be isolating and daunting. Also, when you are working alone, you oftentimes lack someone to hold you accountable and you sometimes will develop too much materials on one area and not enough in other areas.

When we work as a team on materials development, we need to:

1. Explicitly lay out an overarching timeline for the project at the beginning with ample cushion time built in
2. Create sub-timelines for each week or two weeks of development
3. Create time budgets for certain tasks so that everyone has clear expectations on the expected timeframe is and there can be a discussion if more time is needed and why
4. Assess and give feedback on the prgress made since the last meeting
5. **Try to avoid spending more than ~5 hours on development without getting at least some feedback on it.** It can be very easy to spend too much time and go too far down a rabbit hole and bill too much time for development.

## Phases of design

When we are creating a course and we have an idea for each lesson, it is a good idea to work within this framework:

1. Identify your Learning Objectives or atleast a draft or what you want them to be
2. Draft a rough idea of your assessments for those Learning Objectives
3. Create a framework of the lesson. This framework should be very minimalistic in content but still contain:
   - Learning objectives
   - YAML
   - Headings
   - Subheadings
   - Psuedocode of what the participants for the workshop will be doing (don't worry about the exact code or parameters at this point unless you are just copy-and-pasting them from somewhere, but something like `bwa align to mm10 reference` is fine
   - Drafts of exercies/assessments, these don't need to be final and it could be something like `have participants run FASTQC on sample 2`
   - Text where image will go describing it like `image showing pseudobulk process`. If you know this image exists and we already have developed it somewhere, feel free to embed it but don't create any images at this point
   - Navigation buttons, but don't link them to any pages yet as names will likely change
   - Footer
5. Get approval from your collaborator on the framework before proceeding
6. Flesh out draft materials by learning objective
7. After completing a learning objective, show it to your colloborator for feedback
8. Incorporate your collaborator's feedback and design initial drafts for any figures/GIFs/apps (guidelines below on these) that will be embedded in the materials
9. Repeat steps 5-8 for each learning objective in a lesson
10. Have a third-party review your materials and provide feedback. The thrid-party should recognize that this is still in a draft state. Fixing typos, etc. are not the goal here but rather, does the flow make sense to them, is the lesson clear, etc.
11. Incorporate third-party's feedback into the lesson
12. First pass at polish on the lesson. Try tidying the lesson up, fixing typos, checking links, making sure things are rendering correctly in the HTML
13. Third-party polish. This is the final polish for a lesson, the final polisher must:
    - Run all of the code to ensure it works
    - Work from the HTML page to ensure renderings are correct
    - Address any typos they see
    - Check each link to ensure they work

# Identifying a dataset

This *can* be one of the most time-consuming parts of development. When designing our workshops, we want to be using publically availible data. People outside of Harvard oftentimes use our resources and they need to be able to access the data set via SRA/GEO. If we have toy datasets we should host them on Dropbox or GitHub (**Meeta we should make a verdict on this** Personally, I like having everything on GitHub, but sometimes there are file size issues with GitHub. Sometimes I get e-mails about access issue with people getting odds and even from Dropbox and that is annoying. I sort of feel like the policy should be GitHub if we can, but if File Size constricts us, then Dropbox?). 

We also want to avoid to much unnecessary complexity to the data. What is the minimum number of samples we can trim the data down to and still be within best practices? Perhaps the experiment had multiple conditions, can we narrow the dataset to just case and control conditions. We don't want the complexity of the dataset to take away from the learning of the concepts. 

# Format

The general format of the page should be:

1. YAML
2. Additional documentation
3. Learning Objectives
4. Brief introduction including the step in workflow image
5. Content
6. Navigation buttons to the "Next Lesson" and "Back to Schedule"
7. License Footer


## YAML
The top of the page should have a YAML

```
---
title: "Title that will appear over the DNA image"
author: "List of contributing authors"
date: "Date"
---
```

## Additional documentation

Next add a list of contributing authors and the approximate time the lesson should take to complete. It may feel difficult to estimate a time when starting, but even estimating a time can help give you a framework to try to work within. When someone reviews the materials, it can be a good idea for them to update that approximate time if need be.

```
Contributors: List of contributing authors

Approximate time: XX minutes
```

## Learning Objectives

The next section we need to add is arguably one of the most important sections in our layout, the Learning Objectives. It is critical that learning objectives are:

- *Measurable* - This is really important that you can assess whether a learning objective has been achieved.
- *Specific* - Focus on what we are specifically aiming for participants to get out of the lesson
- *Achievable* - Partipcants can accomplish the learning objective given the resources in the lesson

You will likely find that this might be one of the more difficult parts of the lesson to develop, but it can be a great guide for how you develop the lesson. Whe you are developing learning objectives, being considering where on Bloom's Taxonomy (see below) you are aiming for workshop participants to be reaching. Not all learning objectives for the lesson need to be at the higher levels of Bloom's taxonomy. A variety can be beneficial and also is probably an accurate reflection of the level our materials should be taught at. For example, we likely won't ask participants to "Construct a read alignment algorithm", but being able to "Paraphrase or identify key steps in the read alignment process" is likely a more reasonable expectation.

<p align="center">
<img src="img/blooms_taxonomy.png" width="600">
</p>

*Image from https://tigerlearn.fhsu.edu/the-revised-blooms-taxonomy-as-a-framework-for-writing-learning-objectives/*

Create creating a Learning Objective, try to pick a verb that is going to pair well with the level in Bloom's Taxonomy you are hoping particiapnts will reach AND with your assessment. For example, if your Learning Objective is "Identify the key steps in bwa's read alignment algorithm" then the assessment should be something like "Which of these steps are part of bwa's read alignment algorithm" and not something like "Compare bwa and HISAT2's read alignment algorithms". 

Picking the right verb for your learning objective can be really helpful for creating your assessment of that learning objective. Below is a great table of more verbs associated with each level of Bloom's Taxonomy.

<p align="center">
<img src="img/Blooms-Taxonomy-Verbs.png" width="600">
</p>

*Image from https://www.learningeverest.com/blooms-taxonomy-decoded/*

## Content

### Text

Text is important for conveying ideas, but long paragraphs and text-heavy lessons can be diificult for retaining participants' attention. Major deas should be stated in text, but they can also be supplmented by:

- Images
- GIFs
- Equations
- Dropdowns
- Apps

You can also break-up paragraphs by using bullet points when you are listing anything. This creates a more diversive set of visuals for the reader and also it oftentimes more difficult to teach material that is in paragraph form as opposed to other mediums. A good rule of thumb (but not a hard rule) is to try to avoid more than 2 consecutive paragraphs of text. 

### Images

Images are an integral part of conveying information in conjunction with text. Considerations for images:

**Does the perfect figure already exist somewhere else?**

Sometimes people have created excellent figures in papers and there is no need to re-invent the wheel. If you go down this route, be sure to provide appropriate attribution underneath the figure.

**Creating our down figures**

Figures that we create should follow some guidelines:

- *High-resolution* - Others in our group or elsewhere may recycle this figure and we would like the figure to be clear at different size scaling than we present. By providing high-resolution images, we can try to future proof this.

- *Clarity* - 

### GIFs

### Dropdowns

### Linking out

### Equations

Sometimes we people have a habit of writing out equations in words like: 

"The gravitational force is gravitational constant times the mass of first object times the mass of the second object divided by the distance between the centre of two bodies squared"

Perhaps some may find this useful, but it can be a lot more clear to provide equations ***AND*** define the elements of the equation. [Codecogs]()https://editor.codecogs.com/ provides a nice way to embed equations as images in our GitHub documents

If possible, providing toy examples and tables to help make the outcomes of the equations more intuitive. For example, instead of the gravitational example above, we could do:

<p align="center">
<img src="https://latex.codecogs.com/svg.image?F_{gravity}=\frac{G&space;M_{1}M_{2}}{D^{2}}" width=250>
</p>

### Shiny Apps

## Footer

All of the pages need to have the following footer:

*These materials have been developed by members of the teaching team at the [Harvard Chan Bioinformatics Core (HBC)](http://bioinformatics.sph.harvard.edu/). These are open access materials distributed under the terms of the [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0), which permits unrestricted use, distribution, and reproduction in any medium, provided the original author and source are credited.*

- Include RRID


Boston College has a nice [webpage](https://cteresources.bc.edu/documentation/learning-objectives/) on learning objectives.
