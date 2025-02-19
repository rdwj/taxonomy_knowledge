# taxonomy_knowledge

**Description:**  
Reference files for the document section of `qna.yaml` to be used with InstructLab.

---

## Overview

This repository contains a collection of reference files that are used in the `document` section of the `qna.yaml` file, specifically designed for use with InstructLab. These reference files provide the content required for building an effective Q&A file.

---

## Files

The repository consists of various files for specific domains of knowledge. Markdown files may have been converted from PDF using https://https://pdf2md.morethan.io/ 

---

## Usage

To use the reference files in this repository within your `qna.yaml` configuration, follow these steps:

1. In your own `taxonomy_knowledge` repository, create or modify your `qna.yaml` file to reference the files you want to use from this repository. The format should look like this:

   ```yaml
   document:
     repo: https://github.com/rdwj/taxonomy_knowledge
     commit: <FULL_SHA_OF_FILE>
     patterns:
       - <file_name>.md
To get the full SHA for the file you want to reference:

Go to the file in this repository (e.g., taxonomy_knowledge/readme.md).
Open the file.

Click the History or Commits button on the upper right part of the window.

Click on the "Copy" button next to the short SHA (visible to the right of each commit).
Replace <FULL_SHA_OF_FILE> in the commit field with the full SHA you copied.

Once you've updated your qna.yaml, use it with InstructLab to run your Q&A pipeline.

Example:
Here’s how your qna.yaml might look if you were using this README.md file:

```yaml
document:
  repo: https://github.com/rdwj/taxonomy_knowledge
  commit: e154ac7e02d7bde248b6be35f47490d1f3cf1045
  patterns:
    - README.md
```

This configuration will pull in the README.md file from the taxonomy_knowledge repository at the specified commit SHA, and the Q&A system will use the data in this file.