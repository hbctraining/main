# Quarto Reference

This document outlines options that we use in our Quarto documentation.

# YAML

The YAML at the top of the lesson should look like:

```
---
title: "Lesson Title"
description: |
  Write a description of the lesson here. 
author:
  - author_1
  - author_2
date: "YYYY-MM-DD"
categories: 
  - category_1
  - catagory_2
  - catagory_3
  - catagory_4
keywords:
  - keyword_1
  - keyword_2
  - keyword_3
  - keyword_4
  - keyword_5
  - keyword_6
license: "CC-BY-4.0"
editor_options: 
  markdown: 
    wrap: 72
---
```

The important components of our YAML that you will need to modfiy are:

- **title** - This is the title of the lesson. It should be in quotes.
- **description** - This is a description of the lesson and can very important in search engine optimization. This is preceeded by a pipe character but the text doesn't need to be in quotes.
- **date** - Date in YYYY-MM-DD format. It should be in quotes.
- **categories** - Broad ideas of the lesson. It can marginally help with search engine optimization.
- **keywords** - Tags for functions and ideas discussed in the lesson. It can marginally help with search engine optimization.

# Code Blocks

When embedding a code block, the format should look like:

<pre>
```{r}
#| label: code_block_label
```
</pre>

All blocks should have:

- `{r}` - The language to interpret the block with.
-  `#| label: ` - A label for the code block that is unique to the lesson

## Additional Code Block Options

You may want your code block to have additional options, such as:

- `#| eval: false` - The code block will not be evaluated if set to `false`
- `#| echo: false` - The code block will not be printed if set to `false`. This can be nice when trying to run code in the background like loading a dataset that workshop participants will already have in the background.

# Notes

If you want to provide a note in a callout block, you can use this syntax:

```
:::{.callout-note}
Text of the note.
:::
```

If you'd like to make the note collapsible, use this format:

```
::: {collapse="true" title="Click here to see <extra_information>"}
Text of the note.
:::
```

# Exercises

When making an exercise, it should look like:

```
:::{.callout-tip}
# [**Exercise <number>**](<name_of_lesson>_Answer-key.qmd#exercise-<number>)
Text of the exercise.
:::
```

All exercises should link out to an answer key that is tied to the lesson with the same name as the lesson, but with `_Answer-key.qmd` instead of `.qmd` appended to the end. The answer keys will use `# Exercise <number>` for each of the headings.

