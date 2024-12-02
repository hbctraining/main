# Training Development Guidelines

This is a guide to help create continuity across our training materials. It is a living document and will try to be maintained to the best of our ability.

# Format

## The YAML
The top of the page should have a YAML

```
---
title: "Title that will appear over the DNA image"
author: "List of contributing authors"
date: "Date"
---
```

## Additional documentation

Next add a list of contributing authors and the approximate time the lesson should take to complete. It might be a good idea to leave the approximate time blank initially until you get an idea of how your want the lesson to look. When someone reviews the materials, it can be a good idea for them to update that approximate time if need be.

```
Contributors: List of contributing authors

Approximate time: XX minutes
```

## Backward Design

"Traditional" course design is often regarded as a process through which the instructor develops materials and then uses the principles from those materials to create an assessment. The "downfall" of this strategy is that it can result in teaching things that aren't assessed and can sometimes feel a bit meandering in the learning. 

Backward Design principles are a set of principles for course design when focus on how students will be assessed and then work to develop materials that align with those assessment goals. When we apply backward design principles in our course development it should follow these steps:

1. Identify what goal we want participants to accomplish
2. Create an assessment that will certify that the goal was obtained
3. Develop materials aimed at ensuring that students will be successful at the assessment

When you are planning a workshop or a lesson it can be really helpful to develop, even if it is very rudimentary (you can always come back to this) what exercies you want the participants to do first. This will tremendously help guide your development process, because you will be developing *toward* an assessment.

Vanderbilt has a nice [webpage](https://cft.vanderbilt.edu/guides-sub-pages/understanding-by-design/) on Backward Design.

## Learning Objectives

The next section we need to add is arguably one of the most important sections in our layout, the Learning Objectives. It is critical that learning objectives are:

- *Measurable* - This is really important that you can, and we should try when developing the lesson, assess whether a learning objective has been achieved. 
- *Specific* - Focus on what we are specifically aiming for participants to get out of the lesson
- *Achievable* - Partipcants can accomplish the learning objective given the resources in the lesson

You will likely find that this might be one of the more difficult parts of the lesson to develop, but it can be a great guide for how you develop the lesson. 



## Identifying a dataset

This *can* be one of the most time-consuming parts of development. When designing our workshops, we want to be using publically availible data. People outside of Harvard oftentimes use our resources and they need to be able to access the data set via SRA/GEO. If we have toy datasets we should host them on Dropbox or GitHub (**Meeta we should make a verdict on this** Personally, I like having everything on GitHub, but sometimes there are file size issues with GitHub. Sometimes I get e-mails about access issue with people getting odds and even from Dropbox and that is annoying. I sort of feel like the policy should be GitHub if we can, but if File Size constricts us, then Dropbox?). 

We also want to avoid to much unnecessary complexity to the data. What is the minimum number of samples we can trim the data down to and still be within best practices? Perhaps the experiment had multiple conditions, can we narrow the dataset to just case and control conditions. We don't want the complexity of the dataset to take away from the learning of the concepts. 

## Pictures Picture Pictures

## Equations

Sometimes we people have a habit of writing out equations in words like: 

"The gravitational force is gravitational constant times the mass of first object times the mass of the second object divided by the distance between the centre of two bodies squared"

Perhaps some may find this useful, but it can be a lot more clear to provide equations ***AND*** define the elements of the equation. [Codecogs]()https://editor.codecogs.com/ provides a nice way to embed equations as images in our GitHub documents

If possible, providing toy examples and tables to help make the outcomes of the equations more intuitive. For example, instead of the gravitational example above, we could do:

<p align="center">
<img src="https://latex.codecogs.com/svg.image?F_{gravity}=\frac{G&space;M_{1}M_{2}}{D^{2}}" width=250>
</p>




Boston College has a nice [webpage](https://cteresources.bc.edu/documentation/learning-objectives/) on learning objectives.
