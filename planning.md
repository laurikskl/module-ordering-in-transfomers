PAPER

Introduction

The introduction is a crucial part of any paper. A compelling introduction immediately captures the reader’s interest and answers the question: “Why should I read this?" Here is the structure I use for my paper introductions. Feel free to adapt it to your needs or develop your own structure.
* 1-2 sentences to give context about the work - LLMs have quadratic scaling for context length, infini-attention promises infinite context length in a finite compressive memory.
* Introduce the “problem" you will be solving. - how does this compressive memory scale.
* List the highlights of approaches that try to solve this problem. - they do benchmarks like needle in a haystack etc. They say it has a 114x compressive ratio
* Identify the gap in the literature - They don't play around with compressive memory size
* State how are you going to address this gap? - I am going to train new models that change the embedding dimension size or may be key dimension size of the model.
* Give some details about your proposed approach
* Report your main findings
* Indicates the implications of your findings
* Wrap up this section by clearly listing your main contributions, it can be a new technique, a new dataset, a tool, an empirical study with new findings, etc.

**The Problem**
- LLMs are really nice to use for summarizing long texts or giving them documentation that they have not been trained on
- Increasing context length makes the costs scale quadratically
- Infini-attention promises infinite context length for a finite cost.
- They propose a compressive memory,  but can it really hold infinite information?

**Existing Approaches**
- They do benchmarks like needle in a haystack 
- they find a compressive ratio of 114x

**The Gap**
- How does the compressive memory scale depending on its size?


2 BACKGROUND AND RELATED WORK
To ensure a comprehensive understanding and position your work in the broader landscape context, it is essential to familiarize yourself with recent advancements in the domain. Search for recent work that addresses your specific problem. Moreover, research studies that use your proposed model/method and summarise them. In the interest of time, you can focus on studies and solutions proposed since 2020 (but you are welcome to cover more). Use platforms like Google Scholar or DBLP for your search. Prioritize contributions from top software engineering conferences such as ICSE, ESEC/FSE, ASE, and MSR and well-known journals like TSE, TOSEM, and EMSE (in our case; AI-focused venues may be more appropriate)
In my opinion: your introduction should be relatively short; and you can include all necessary supplementary material for someone not as familiar with your topic in this section. I.e. extensively describe existing approaches, where they succeed and fail, how this highlights a gap in the research, and additional studies you draw on to motivate this paper.

They use associative binding from 

**Background and prior work**
(The idea is to look at the old papers and see how scaling could work)
- we parameterize the memory with an associative matrix (Schlag et al., 2020). 
(LEARNING ASSOCIATIVE INFERENCE USING FAST WEIGHT MEMORY Imanol Schlag)

- This approach further allows us to cast the memory update and retrieval process as linear attention mechanism (Shen et al., 2018)
(Zhuoran Shen, Mingyuan Zhang, Haiyu Zhao, Shuai Yi, and Hongsheng Li. Efficient attention: Attention with linear complexities.)

- adopt the update rule and retrieval mechanism by Katharopoulos et al. (2020)
(Transformers are RNNs: Fast Autoregressive Transformers with Linear Attention Angelos Katharopoulos)


3 APPROACH
Tip: I recommend that you create and use a nice figure to depict the approach. This is where you motivate, and conceptually/mathematically describe the gap you seek to investigate.
E.g. in my last paper, I changed the transformer architecture to integrate additional modalities. First I motivate this change by highlighting the contextual integration abilities of transformer models. Then, I conceptually highlight existing methods to address this gap, their strengths and drawbacks. Finally, I describe (both with figures and math) what changes I hypothesise will improve performance.


4 EXPERIMENTS SETUP
Define the research questions clearly. Discuss the specific configurations you have settled on, and elaborate on the data sets you have utilized. Document the evaluation setup and define the metrics.
4.1 Research Questions
4.2 Dataset
4.3 Models
4.4 Evaluation Setting and Metrics.
Evaluation Metrics: You should mention the components of the BabyLM evaluation pipeline; but can defer explaining each (fine-tune) task in detail to the BLiMP/GLUE/SuperGLUE papers. However, you should describe the process each of these components uses to return a score (i.e. how is the final score computed?)
Evaluation Settings: hardware.
4.5 Configuration and Implementation Details

5 RESULTS
Results per research question. These are the numbers you got (ob-
jective).

6 DISCUSSION
Here discuss your interpretation of the results (subjective), what are their implications, how can they be improved, what are potential reasons for good or bad performance, and suggest future work. Finally, wrap up by reflecting on the threats to the validity of your study. there are different types of threats, i.e., construct, internal, external, etc. Make sure to read up on them and identify relevant threats to your work.
6.1 Implications
6.2 Threats to the Validity: Split into internal, external, and construct validity (more info)
6.3 Future Work
7 RESPONSIBLE RESEARCH
Explain how you:
Ensured transparency and reproducibility in your research by sharing data, methods, and findings openly. 
Adhered to principles of scientific integrity, avoiding data manipulation, fabrication, and plagiarism.
Addressed ethical considerations, disclosed conflicts of interest, and followed guidelines for ethical conduct
Incorporated principles and practices from chapters 2 and 3 of the Netherlands Code of Conduct for Research Integrity
8 CONCLUSION
Summarise the main goal and findings of the work.

REFERENCES
Make sure all references are provided in the Title Case. Check that \cite or \citet (if you have ‘according to’, a clever package) also provides a link to the reference. Try to include a doi wherever possible.


