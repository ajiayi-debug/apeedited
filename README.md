##Overview:
This project involved revamping the APE codebase to integrate the Alpaca-7B model, resulting in cost reductions and increased efficiency. The effort was inspired by the study “Large Language Models Are Human-Level Prompt Engineers.”

##Key Achievements:

 • Successfully replaced OpenAI’s GPT-3 with Alpaca-7B in a Linux environment, optimizing resource utilization.
 • Innovated data transformation by converting CSV datasets to LaTeX tables using few-shot prompting, surpassing traditional zero-shot methods in prompt generation efficiency.
 • Applied principles from “Improving Few-Shot Prompts with Relevant Static Analysis Products” to fine-tune the APE-generated prompts, enhancing the quality and effectiveness of the output.
 • Developed an optimization for APE that incorporates semantic facts into the data, significantly improving the accuracy of the generated prompts.
 • Conducted a comparative analysis that confirmed the inclusion of semantic facts leads to a substantial increase in the accuracy of data to LaTeX table conversion.

##Conclusion:
The project demonstrates the potential of few-shot prompting combined with semantic facts to automate and improve data generation processes.

##Instructions:
#Automatic Prompt Engineer (APE) to convert CSV data to LaTeX format

This repo contains edited code from the paper "Large Language Models Are Human-Level Prompt Engineers" from [ArXiv](https://arxiv.org/abs/2211.01910)

#Abstract

With the emergence of large language models (LLMs) comes the need for large amounts of data to train these LLMs. However, creating such data is tedious and requires lots of human effort. The project goal was to create realistic data for LLM training through automated methods in the form of LaTeX data. One such method is to use prompt engineering to create data. However, this still requires human effort to create prompts. 
Existing research has shown that the algorithm Automatic Prompt Engineer (APE) can automate the prompt engineering process, reducing the need for human efforts. 
In my method, the APE reads in a dataset of input-output pairs and generates a set of instructions using an LLM and a generation template. This set of instructions is then put back into the LLM with an evaluation template and the output generated is used to calculate the score of the instruction generating the deesired output. (generated output vs desired output). The score is then used to score the generated instructions and the best ranking one is the best generated instruction.


##Installation

To install APE, simply run:

```bash
pip install -e .
```

Please refer to the paper "Large Language Models Are Human-Level Prmpt Engineers" from [ArXiv](https://arxiv.org/abs/2211.01910) and their github page for more information

To install Alpaca-7B, refer to the website [circulus/alpaca-7b](https://huggingface.co/circulus/alpaca-7b)

##Using APE

With reference to [automatic_prompt_engineer](https://github.com/keirp/automatic_prompt_engineer/blob/main/README.md#using-ape), to run the APE with semantic facts, refer to comments at the top of the file in llm.py


You can ignore all openaikey parts as OPENAIAPI was not used in this version of APE.
