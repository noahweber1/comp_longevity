***
>*Important notes*:
* Goal of this project is to be a community *WIKI* for computational longevity topics.
* This means that corrections and/or additions that are substantial will be rewarded with 1000$ worth of ETH. Submit a PR here with the instruction how in README: https://github.com/noahweber1/Computational_Longevity
* This is a rolling set of writings, meaning information will be added in perpetuity.
* You can navigate to the desired (sub-)chapters using the dropdown on the right.
* To cite this work use the following format: *Weber, Noah (2023). Computational Longevity. https://noahweber1.github.io/Computational_Longevity/Chapter%201%20-%20Motivation.html*
***

# Chapter 1 - Motivation and brief overview

## Contents of this book:

1. *Motivation for writing this book:*
    > a) Analogy based learning between longevity and the computer science.

    > b) Future horizont of some of the breakthroughs and advances relevant to longevity.

2. *Biology basics, measurements, databases and computational approaches towards elucidating longevity:*
    > a) Basics of (longevity) biology.

    > b) Quantifying biological research in longevity.

    > c) Tools for measuring the data.

    > d) Data sources specifically dedicated to aging.

    > e) Network and omics approach to research aging.

3. *Hallmarks and biomarkers of aging. How can we computationally explore them:*
    > a) Hallmarks of aging and how tackle them computationally.

    > b) New hallmarks of aging and how tackle them computationally.

    > c) Aging clocks, causality and the future of evaluating biological age.

4. *Longevity interventions and animal models to test these interventions:.*
    > a) Molecular pathways involved in the aging process.

    > b) Chemical basis for longevity.

    > c) Environmental basis for longevity.
    
    > d) Alternative (less known and researched) longevity interventions .

    > e) Model organisms of aging and its alternatives.


# Chapter 1 - Motivation

![](https://www.genengnews.com/wp-content/uploads/2019/07/205397_web.jpg)

Learning a new discipline is easier if we can apply [analogy-based learning](https://link.springer.com/referenceworkentry/10.1007/978-1-4419-1428-6_11#:~:text=Learning%20by%20analogy%20is%20a,linguistic%20competence%2C%20divergent%20thinking).
Coming from a computational background and trying to decipher research papers of the form: ["Metformin treatment of diverse Caenorhabditis species reveals the importance of genetic background in longevity"](https://onlinelibrary.wiley.com/doi/10.1111/acel.13488) has proven to be hard.

What is Metformin? What is Caenorhabditis? Is the optimal model? What is a model in the first place? What is the genetic role in longevity? etc.
To navigate this space, one needs to start from [first principles](https://en.wikipedia.org/wiki/First_principle#:~:text=A%20first%20principle%20is%20a,to%20as%20postulates%20by%20Kantians.) of biology.

Biology is complex. So are computers. Can we find a mapping between software and biology related terms? 

Example of what this analogy comparison would look like is this:

 Biology | Software | 
------- | -------- | 
[gene](https://en.wikipedia.org/wiki/Gene)  ->   | [library](https://en.wikipedia.org/wiki/Library_(computing)) ||
[genome](https://en.wikipedia.org/wiki/Genome)  ->   | [bytecode](https://en.wikipedia.org/wiki/Bytecode) |
[translation](https://en.wikipedia.org/wiki/Translation_(biology))  ->   | [disassembly](https://en.wikipedia.org/wiki/Disassembler) |
[protein](https://en.wikipedia.org/wiki/Protein)  ->   | [function](https://en.wikipedia.org/wiki/Function_(computer_science)) |
[protein secondary structure](https://en.wikipedia.org/wiki/Protein_secondary_structure)  ->   | [basic blocks](https://en.wikipedia.org/wiki/Basic_block) |
[quaternary structure](https://en.wikipedia.org/wiki/Protein_quaternary_structure)  ->   | [compiled function with inlining](https://en.wikipedia.org/wiki/Inline_expansion) ||
[protein structure prediction](https://en.wikipedia.org/wiki/Protein_structure_prediction)  ->   | [library identification](https://www.hex-rays.com/products/ida/tech/flirt/in_depth/)
[genome analysis](https://en.wikipedia.org/wiki/Genomics#Genome_analysis)  ->   | [static analysis](https://en.wikipedia.org/wiki/Static_program_analysis) |
[molecular dynamics](https://en.wikipedia.org/wiki/Molecular_dynamics)  ->   | [dynamic analysis](https://en.wikipedia.org/wiki/Dynamic_program_analysis) |
[nucleotide](https://en.wikipedia.org/wiki/Nucleotide)  ->   | [byte](https://en.wikipedia.org/wiki/Byte)

While not a perfect mapping it serves a purpose: 
> All of the problems that are going to be faced in biology domain could be tackled with already proposed solutions in software domain.

But why care?

## Biology is just an iteration cycle

We care because solving aging entails solving biology. And solving biology means finding a better iteration cycle: 

![biology_iterations](https://i.ibb.co/PWmtWWp/biology-debugging.jpg")

1. **Observe Phenotype** means observing the effect of the intervention on everything that can be measured. Besides the external changes of the organism, internal measuraments such as [biomarkers](https://en.wikipedia.org/wiki/Biomarker) are also relevent. 
2. **Update the model** means using the observational information to enhance your (computational) understanding of the particular biological part. One example for that can be a computer simulation of particular molecular pathway. Other one could be using animal models that are most similiar to what we are trying to tackle in humans. Using this model we can then make educated therapeutic suggestions.
3. **Suggest therapeutic intervention** means utilizing the previous information in order to make an intervention that will hopefully result in more favorable observations in step 1.

Problem is, biological iteration cycles take a lot of time. As I am writting this, the formatted Markdown text is being rendered on adjecent window. The ("software") iteration cycle is fast, since I can observe all the changes in almost real time. Hence I can adjust accordingly in timely fashion. 

*We need an biological alternative of real time rendering.*




## What gets measured gets simulated

In order to achieve the biological alternative of real time rendering, we face complications on several levels:

1. **Oversimplification of biology.** Example: [Apoptosis pathway](https://en.wikipedia.org/wiki/Apoptosis). Left is the oversimplified understanding. Right is the actual one. Hope is that the data will give us insight in unexplored biological mechanisms.
<a href="https://ibb.co/W0yX9R0"><img src="https://i.ibb.co/cwF95sw/biology-complexity.png" alt="biology-complexity" border="0"></a>
2. **Capturing data.** In order to simulate biology we need to comprehensively capture the information on each cellular level. 
3. **Interpeting data.** In order to analyse this data, there needs to be appropriate [tools](https://omicstutorials.com/bioinformatics-tools-softwares-programmes/) operating on them.
4. **Accurate models.** Both in terms of animal and computational models we are only approximating of what should happen in humans. Translational issues are a huge problem.
5. **Causality.** Just because we have identified some patterns does not mean that these patterns are causative, i.e. explain the biological process in a mechanistical manner. This is very important, because if we can not use the computational modelling to actually derive biological theories, then it is all just a black box.
6. And many others...


## Why longevity?

Ever heard of a 25 year old with Alzheimers? Me neither. Longevity is arguably root cause for majority of diseases. If we could solve longevity we could potentially solve majority of diseases.

> *But what is the exact problem definition?*

**Prolonged health span, not only life span.**

I like to think of the longevity problem as a multi-objective optimization.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/J5Vx6DF/longevity-mo.jpg" alt="longevity-mo" border="0"></a>

We have two variables. X is the the health span and Y is the life span.
Usually our health span peaks around 50 (or even sooner depending on the definition) and we proceed with life (span). What the actuall goal with longevity should be (or maybe not if you read some research papers) is to first optimize for the X variable as we are optimizing for the Y. Not the other way around. With this objective in mind we can aim for long, healthy life span. Not necesseraly solely life span for the sake of it. 


Given that we have been trying to [solve this problem](https://www.amazon.com/dp/B00SHPD0N4/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1) for thousands of years, and still fail, is there a reasonable argument we could tackle longevity successfully now?

We need some breakthroughs to argue for the **future horizon of longevity**. What are the developments coming from biology and chemistry and how can we supplement them computationally?

# Future Horizon of Longevity
One of the key challenges to understanding complex systems is the fallacy of assuming that correlation implies causation. For instance, the telomere shortening theory is widely regarded as a key factor in longevity. Telomeres are repetitive nucleotide sequences found at the ends of our chromosomes that are associated with proteins. The theory is that the length of telomeres directly impacts longevity. Scientists observed that mice with shorter telomeres tend to have shorter lifespans, and vice versa. However, when the theory was tested in humans, the results were less clear. In some cases, excess telomerase was linked to cancer. This raises the question of whether the length of telomeres is a cause of longevity, or if it is an effect. More data is needed to determine the answer.

So we need some new breakthroughs that could potentially elucidate more insight based on data and underlying biology.

Here are some of the examples, many of which we will extend upon in the upcoming chapters:

## The genetic engineering breakthrough.

The Human Genome Project, which was completed in 2003, successfully sequenced (almost) the entire human genome. This means we now have an (almost) complete map of all 25,000 individual genes. This information allows us to predict many hereditary diseases, the likelihood of developing cancer, and other unknowns where the cause and effect relationship is still not well understood. However, given that our genes do not change much from birth, what other implications does gene sequencing have? Our epigenome, which is the system of chemical modifications around our genes that determines how they are expressed, does change. Furthermore, according to longevity scientists, the biological age of our epigenome, rather than our actual age, appears to be far more significant.

**Why is this important for machine learning?** Biological age measuring solutions, such as Horvath clocks, enable us to measure the "aging score" and effectively measure the chemical activity within the epigenome. This allows us to simulate longevity experiments and observe the effects on a human cell long before that person dies. [Deep learning can be used to improve the Horvath clock accuracy](https://epigenie.com/the-epigenetic-clock-from-deep-space-to-deep-learning/). In addition, the cost of genome sequencing has decreased significantly, making it more affordable to analyze the enormous amounts of data produced. One genome contains three billion nucleotide base pairs, and even a small change in just one letter (one nucleotide) in the genome can have severe side effects.

One example of using our understanding of the genome and the effects of genes is gene therapy. This approach focuses on genetic modifications of cells to produce a therapeutic effect. For instance, CAR T-cell therapy is a cancer treatment that is based on gene therapy. In this approach, a patient's own immune system T cells are modified to fight specific types of cancer. Machine learning can be used to [improve the manufacturing process of CAR T-cells](https://www.isct-cytotherapy.org/article/S1465-3249(19)30527-4/fulltext).


## The regenerative medicine breakthrough.

As we age, our bodily systems and functions begin to deteriorate. Longevity is not just about living longer, but also about making the most of the years we have. To achieve this, we need technologies that can repair these functions. One such technology is stem cell therapy. This field has been a topic of discussion for many years, but what has been emerging and further advancing it is, as you might have guessed, artificial intelligence (AI). AI can aid in many aspects of stem cell technology, with a formal overview of how AI can be used to tackle different parts of stem cell technology available [here](https://www.eurekaselect.com/186710/article).


## The health-care hardware breakthrough.

Of all the potential breakthroughs, this one holds the most potential. Every year, 60 million lives are lost, and more than half of those deaths are due to reversible diseases if caught early. The problem is that we are not monitoring frequently and granularly enough to react in time. Our current approach is "reactive" rather than "proactive." If we can get this data early and accurately enough, we will be able to diagnose the condition at hand. This brings us to one of the fundamental principles of AI: it's the data that makes the difference, not the machine learning algorithms. If you have high-quality (labeled) data, the algorithms that operate on that data are not as important. And yes, current wearables are very limited in their capabilities. However, this is changing quickly, as this recent [Nature](https://www.nature.com/articles/s41591-021-01652-8) publication shows. We can now measure deep tissue processes without invasive surgery. He who owns the data owns the AI.


## The health data intelligence breakthrough.
The amount and quality of data coming from wearable devices is a key factor driving the longevity revolution. Another important aspect is the practice of precision medicine, which involves customizing health diagnostics to individual characteristics. We are getting more and more publicly available data for this, such as [here](https://www.biorxiv.org/content/10.1101/2022.05.01.489928v2). However, privacy issues can be a problem when it comes to using machine learning algorithms on this data. Sending the data to a server for diagnostic computation can be problematic.

There are two potential solutions to this problem: on-edge machine learning and differential privacy. The first solution leverages the fact that our current devices (not just phones) have become incredibly powerful. They can now perform computations that were previously only possible on personal computers or clusters. The computer used to send the first man to the moon is now weaker than most modern phones. This means that expensive machine learning calculations can be performed on phones and smaller medical devices, avoiding the need to send sensitive data to servers. The second paradigm is that of differential privacy, which involves injecting carefully controlled noise into the data to mask it, while still allowing the algorithms to extract patterns and make diagnoses. This is not a new concept, and is what companies like Google and Apple claim to use when processing our private data.

**NOTE**: Privacy and its solutions will become even more critical as we move towards the internet of bodies (IoB), where all the sensors that measure our data are connected to each other and to other people's data. Collective intelligence is more powerful than individual intelligence, so this step is essential for improving AI. However, it will also introduce new security challenges that will need to be addressed using solutions like those discussed above.

The abundance of data is closely linked to better diagnostics. Novel, non-invasive, cheap, and highly effective diagnostic methods include:

1. **Liquid biopsy**, which allows examination of bodily fluids like urine, saliva, spinal fluid, or blood to find traces of diseases, examine DNA or RNA, and more. This is non-invasive and cheap, and the fact that we can extract a lot of information from a single drop of blood opens many doors for diagnosis. As we understand and analyze blood data, for example, we can improve our machine learning algorithms. Some companies are already doing this, building diagnostic recommender systems based on personal blood information. **Data**? [liqDB](https://academic.oup.com/nar/article/47/D1/D113/5144140?login=false) is a small-RNAseq knowledge discovery database for liquid biopsy studies. **What could you do with it?** With this and other liquid biopsy databases, labels indicate different diseases based purely on bodily fluid measurements. There is potential to expand this to other, unlabeled diseases and see if accurate inference can be performed.


2. **Genetic diagnostics** is a rapidly growing area of research and development in the healthcare industry. Advances in machine learning algorithms have enabled companies to create personalized diet plans based on an individual's genetic makeup. However, the real challenge in this field is not the development of ML algorithms, but rather the creation of data to support accurate inferences. A comprehensive overview of the applications and databases in the field can be found [here](https://genomemedicine.biomedcentral.com/articles/10.1186/s13073-019-0689-8).

3. **Epigenome diagnostics** is a promising area for early disease detection. Changes in the chemical compounds and processes that regulate gene expression, known as epigenetic changes, can be used to detect diseases earlier and more accurately than traditional genetic approaches. A wide range of applications, from supervised learning to unsupervised learning to reinforcement learning, are possible in this field. For example, unsupervised learning has been used to profile high-resolution comparative genomic hybridization and RNA sequencing data in order to analyze chromosomal alterations and dysregulated gene expression in tumor samples of patients with fibrolamellar hepatocellular carcinoma. This application illustrates the importance of a multidisciplinary approach to using AI in epigenome diagnostics. [Epigenetic Tools and Databases](https://epigenie.com/epigenetic-tools-and-databases) can be used as a starting point for research in this field.

4. **The human microbiome**, consisting of the microorganisms that inhabit the digestive tract, is closely linked to health and longevity. However, the unique combination of microorganisms in each individual makes it difficult to analyze this data and make accurate inferences. To overcome this challenge, domain knowledge from clinical experts must be combined with curated datasets and AI algorithms to accurately predict diseases based on the microbiome. The [Human Microbiome Project Database](https://commonfund.nih.gov/hmp/databases) is a valuable resource for researchers in this field. A review of methods for applying AI to microbiome data, including the use of deep learning networks to predict antibiotic resistance genes, can be found [here](https://www.frontiersin.org/articles/10.3389/fmicb.2021.634511/full)."


If one peels through the layers of aging problems and rephrase these challenges in terms of information and data, one can see that aging can be tackled computationally with AI.

But for now lets stick to biology basics and introduce some definitions.