# DocuMint: Docstring Generation for Python using Small Language Models

- [Final Presentation](https://github.com/cs540-24/docu-mint/blob/main/Final%20Presentation.pdf)
- [Final Report](https://github.com/cs540-24/docu-mint/blob/main/Final%20Report.pdf)

## Background
Large Language Models (LLMs) are having their moment right now. The latest trends in LLMs however, are Small Language Models (SLMs, generally 13B parameters or less), such as Mistral, Gemma, and Llama family of models. SLMs are significantly more cost effective in terms of latency, memory, throughput, and energy consumption. In addition, they are also small enough to fit in consumer GPUs i.e., they can be deployed locally. 

This study evaluates the effectiveness of SLMs in generating documentation of a Python file. Worldwide, software developers are estimated to spend significant time in code documentation, if this step can be effectively automated, it would have a huge impact on the software development pipeline.

## Research
Our study is to explore if we can leverage SLMs to automatically generate docstring (classes, functions in a python file). More specifically:
   - Conduct a user preference study on various open source SLMs to establish a ranking on which SLMs programmers prefer. 
   - Fine tune available SLMs on World of Code data.  
   - Study the emergent properties of SLMs on documentation generation (As the number of parameters increase, can SLMs generate better docs?). 

## Data
Extract well documented python files from World of Code. Split the data into fine-tuning and validation.
World of Code is a large dataset, so we need to mine for the information that we're looking for:
1. Look at commits (and blobs, not just files) that have “added docstring” in the commit message.
3. Look for projects that list documentation links in the README (parse the README).
3. Look at the code released by corporations (tend to have high quality documentation)

## Deliverables
1. User preference study (human ranking) on the docstring generated by various SLMs.
2. Evaluation of the “emergent behaviors" in generating docstring.
   - Do human coders prefer the documentation from larger models? i.e., does increasing the size of the model improve the quality of docstring?
4. Fine tuning vs. base model.
   - Does the fine tuning step help?
   - NOTE: This will be based on time constraints, and may not be feasible in the short-term.

## People
Shelah Ameli (@ShelahAmeli / oameli@vols.utk.edu)

Adam Cook (@ajcook247 / acook46@vols.utk.edu)

Bibek Poudel (@poudel-bibek / bpoudel3@vols.utk.edu)

Sekou Traore (@Sekou2077 /straore1@vols.utk.edu)

---
BI-weekly reports are present as issues
