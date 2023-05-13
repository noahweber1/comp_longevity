# Chapter 3 - Hallmarks and aging clocks


Contents of this chapter are:

* Hallmarks of aging and how tackle them computationally.
* New hallmarks of aging and how tackle them computationally.
* Aging clocks, causality and the future of evaluating biological age.


![](https://nintil.com/images/2020-01-05-longevity/image-20200117094655213.png)

Inspired by the seminal paper in cancer research, the [hallmarks of cancer](https://www.cell.com/fulltext/S0092-8674(11)00127-9), there has been a similiar attempt for aging.

 [Seminal paper](https://pubmed.ncbi.nlm.nih.gov/23746838/) defined the nine (then extended to 10) main “causes” of our decline. The question then becomes:

> *Can we frame these problems/horsemen computationally in terms of machine learning and then try to solve them?*



1. **Genomic instability**: DNA replication is not always perfect. Errors in gene expression are typically caught and corrected, but sometimes they are not. These errors can accumulate over time, causing the body to deteriorate and leading to a limit on lifespan. This genetic instability can result in damage and can manifest as diseases such as cancer, muscular dystrophy, and ALS. In this way, genetic instability can be thought of as a faulty copying machine that produces harmful results rather than unreadable pages. **Data?** [HumCFS](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5330-5): a database of fragile sites in human chromosomes. **What could you do with it?** Identify other fragile chromosomes sites AND link them to other diseases based on atom/chemical level properties.


2. **Telomere Attrition**: At the center of a cell, DNA is packaged into thread-like structures called chromosomes. Telomeres, which can be thought of as protective caps on chromosomes, act to protect the core of the chromosome. However, as DNA replicates, telomeres become shorter. When telomeres reach a critical length, the cell can no longer divide and we become more susceptible to disease and death. It has been shown that manipulating the shrinkage of telomeres in mice can affect longevity. **Data?** [Telomerase Database](http://telomerase.asu.edu/) **What could you do with it?** [Telomerase can be used as a target in anti-cancer therapy](https://pubmed.ncbi.nlm.nih.gov/28218725/). What this essentially means is one can find computationally (in-silico) inhibitors that hinder the shrinkage of telomerase. Doing this which we know has positive side effects for longevity.

3. **Epigenetic Alterations**: The environment can influence gene expression. Throughout a person's lifetime, exposure to environmental toxins can alter gene expression in negative ways. For example, exposure to carcinogens can silence the gene that suppresses tumor growth. On the other hand, it is also possible to silence the gene that is responsible for cancer. **Data?** [dbEM](https://www.nature.com/articles/srep19340) and [GenAge](https://genomics.senescence.info/genes/index.html): A database of epigenetic modifiers curated from cancerous and normal genomes. **What could you do with it?** Epigenetic proteins are important targets in cancer research. This database provides not only information on epigenetic proteins, but also genomic information related to mutational status, copy number variation, and expression levels of these proteins in tumor samples. This allows for the exploration of proteins that were not previously classified as epigenetic based on their genomic information. **How to utilise GenAge?** There are tools and companies out there that allow for a complete measurement of one genes. ML models could be built that recommend actions based on certain gene structure.

4. **Loss of Proteostasis**: Inside a cell, proteins perform a variety of functions including transportation, signaling, regulation of processes, and providing structural support. However, proteins can become less effective over time and the body has mechanisms to recycle them. As we age, this ability can decline, leading to a buildup of toxic proteins that can contribute to diseases such as Alzheimer's. **Data?** [AlphaFold](https://alphafold.ebi.ac.uk/): Protein Structure Database. **What could you do with it?** Proteins that have become terminally misfolded or are no longer functional must be degraded to prevent harmful effects from their continued presence. Predicting the shape of these proteins, even if they are unknown, can be essential in targeting their degradation.

5. **Nutrient Sensing Goes Awry**: The human body requires a diverse range of nutrients to maintain good health. In order for everything to function properly, cells must be able to recognize and process these nutrients. However, this ability can deteriorate with age. For example, one reason people may gain weight as they age is that their cells can no longer effectively metabolize fats and carbohydrates. This can also impact the insulin and IGF-1 pathway and contribute to the development of diabetes. Ultimately, this decline in cellular function can lead to death. **Data?** [Nutrient Sensing Mechanisms and Pathways](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4313349/). **What could you do with it?** [GenDR Database of Dietary Restriction-Related Genes](https://genomics.senescence.info/diet/). Not a direct ML approach but utilising [advancements in wearables and mobile sensors](https://pubs.acs.org/doi/10.1021/acssensors.1c00553) to obtain detailed and personalized data on nutrition intake based on an individual's current metabolic state could have significant impact. For example, measurements of nutrient sensing in different types of cells (such as cancer cells) could be used to adjust nutrient intake in order to achieve a desired effect on those cells, such as cell death. The GenDR Database of Dietary Restriction-Related Genes could also be used in this context to consider the role of genes in this process.

6. **Mitochondrial Dysfunction**: Mitochondria are the powerhouses of the cell, converting oxygen and food into energy to fuel cellular processes. However, their performance can decline with age. This can lead to the production of free radicals, a damaging form of oxygen that can damage DNA and proteins and contribute to the development of chronic illnesses associated with aging. **Data?** [MSeqDR](https://mseqdr.org/mitobox.php) Mitochondrial Genomic Tools and Databases **What could you do with it?** This curated list of databases could be used to combine measurements of oxygen consumption ratio (OCR), maximal oxygen consumption, and mitochondrial reserve capacity with information on the proteins involved in these processes. Beeing especially interested [in proteins that are targets in certain diseases](https://academic.oup.com/nar/article/47/D1/D1225/5162470?login=false), one could then have clear indicator with wearables or other measurement devices wether some disease is going to be triggered.

7. **Cellular Senescence**: When cells are subjected to stress, they may become "senescent" and lose their ability to divide and become resistant to death. These "zombie cells" cannot be removed from the body and can accumulate over time, infecting neighboring cells and ultimately leading to a state of chronic inflammation and debilitation. **Data?** [CellAge](https://genomics.senescence.info/cells/) Database of Cell Senescence Genes **What could you do with it?** Based on an individual's genetic makeup, a model could be developed to recommend altering genes associated with cellular senescence. Alternatively, further analysis could be performed to determine the appropriate action to take with regard to the genes involved in senescence. This approach has been explored in previous [research](https://pubmed.ncbi.nlm.nih.gov/32264951/)

8. **Stem Cell Exhaustion**: As we age, our supply of stem cells decreases significantly in some cases. Additionally, the remaining stem cells become less active, resulting in a loss of the body's ability to repair tissues and organs. While stem cell therapies exist, it is possible that AI could be used to improve their effectiveness. **Data?** [Stemformatics](https://academic.oup.com/nar/advance-articles?login=false): visualize and download curated stem cell data **What could you do with it?** A curated list of potenital AI applications in stem cell research can be found [here](https://www.eurekaselect.com/article/110522). A crucial challenge in designing stem cell therapies for central nervous system (CNS) diseases is the differentiation of neural stem cells (NSCs) into neurons. This process is complex and not yet fully understood, particularly at the early stages of development. Novel [nature](https://www.nature.com/articles/s41467-021-22758-0) publication shows that deep learning could extract minutiae from large-scale datasets, and present a deep neural network model for predictable reliable identification of NSCs fate.

8. **Altered Inter Cellular Communication**: Effective communication between cells is essential for the body to function properly. This communication occurs through various systems including the bloodstream, immune system, and endocrine system. Over time, however, signals can become disrupted and cells can become unresponsive or produce inflammation. This inflammation can block further communication, preventing the immune system from identifying and responding to pathogens. **Data?** [PanglaoDB](https://panglaodb.se/): is a database for the scientific community interested in exploration of single cell RNA sequencing experiments from mouse and human. **What could you do with it?** A machine learning tool that can quantitatively infer and analyze intercellular communication could be useful in detecting changes in the organism and informing appropriate actions. A recent publication in the journal Nature describes the development of such a tool. [CellChats](https://www.nature.com/articles/s41467-021-21246-9).

10. **Protein crosslinking [extended hallmark]**: Glycation is a phenomenon in which multiple proteins become bonded together by a sugar molecule. Depending on where this occurs, it can be associated with various signs of aging such as wrinkles, arteriosclerosis, cataracts, and kidney failure.
**Data?** [ProXL](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4977572/) (Protein Cross-Linking Database): A Platform for Analysis, Visualization, and Sharing Protein Cross-Linking Mass Spectrometry Data. **What could you do with it?** Developing an ML to identify where this bondage/linkage occurs and what kind of damage it will cause. If labeled data is hard to obtain, clustering techniques can be used to analyze already known bonding regions and try to abstract from there.

> **But they are not enough**

[JPM argues](https://pubmed.ncbi.nlm.nih.gov/34271186/), that the proposed hallmarks are not causative and explanatory enough of the true complexity of the underlying processes.

> *"In this context, the scheme is 
akin to a folding screen bearing a hallmarks of aging diagram that blocks 
the view of the true state of undress of the field. Shivering behind the 
screen is the ailing damage maintenance paradigm. We argue that as a 
field we must look and move beyond the hallmarks to understand the 
process of aging. Only by doing so can paradigms be formulated that 
possess sufficient explanatory power to enable treatments for human 
aging to be developed."*


It comes back to one of the fallacy I outlined: **Oversimplification of biology.**

So what can be done? Taking the table underneath as insight, one could quantify every possible biomarker. Determine which are statistically significant and try to map novel theory (hallmark) that could causative explanation of this multifactorial complex process we call aging.

The American Federation for Aging Research (AFAR) recommends the following criteria for biomarkers of aging:

1) It must predict a person’s physiological, cognitive, and physical function in an age-related way, independently of chronological age.

2) It must be testable and not harmful to test subjects (for example a blood test or an imaging technique); it must also be technically simple to perform, and it must be accurate and reproducibly without the need for specialized equipment or techniques.

3) It should work in laboratory animals as well as humans since preliminary testing is always done in nonhuman subjects.

Check [here](https://link.springer.com/article/10.1007/s11912-020-00977-w/tables/2) for additional details: 

![](https://i.postimg.cc/Yq4CNqVz/hallmark.jpg)

Another important reference for the biomarkers of aging is the [following](https://www.frontiersin.org/articles/10.3389/fgene.2021.686320/full). The rc-score displays how often a potential biomarker was referred to in reviews, based on the above-described NCBI-PubMed queries. 

Then effort score was added for each potential biomarker. Following values were considered:

• A low e-score (-) describes a potential biomarker which is easy to sample, to handle and to process (usually automated fast and reliable measurements are available from known sources). For example, blood counts from venous blood qualify, since such blood can be sampled easily, the plasma/serum can be stored at room temperature (up to 3 h for many analytes) or in a standard freezer (≥3 month for most analytes) and be processed by equipment that is regularly available in a standard diagnostic/clinical unit or research laboratory. The costs are low to moderate (≤10 €).

• A moderate e-score (–) is assigned if one step (sampling, handling, or processing) is associated with substantial extra effort for routine laboratories. This includes sampling under special conditions, a requirement for prompt sample handling, or the need for elaborate validation.

• A high e-score (—) implies elaborate sampling (e.g., biopsy, lumbar puncture, etc.), handling (e.g., storage in liquid nitrogen) and/or processing (e.g., non-routine nucleotide or protein sequencing). The financial costs are usually high.

![](https://www.frontiersin.org/files/Articles/686320/fgene-12-686320-HTML/image_m/fgene-12-686320-t001.jpg)

Again the relevance of these biomarkers is that they could be utilized not only to elucidate new theories and hallmarks computationally but also construct [aging clocks](https://www.technologyreview.com/2022/04/15/1050019/aging-clocks/).



## New hallmarks of aging

As the research progresses new theories started to emerge that aim to extend the current hallmarks.

### Extracellular matrix (ECM) and its connection to longevity

The extracellular matrix (ECM) is a network of proteins and other molecules that support, surround, and give structure to cells and tissues in the body. The ECM helps cells attach to and communicate with nearby cells, and plays an important role in cell growth, movement, and other functions. This three-dimensional network provides physical structure to the body and serves as a substrate for cells to live and grow. Cells often modify the components of the ECM, such as osteoclasts and osteoblasts, which degrade and lay down bone ECM, respectively.

Changes to the ECM are often overlooked as a cause of aging, but they can drastically impact cell behavior. Studies have shown that ECM characteristics such as stiffness and chemical composition can affect cell behaviors including proliferation rate, secretome, differentiation, and cellular maintenance. There is growing consensus that ECM-related changes, particularly matrix stiffening, should be considered on a similar level to the other hallmarks of aging.

"Accumulation of damage to the ECM drives cellular aging and disease progression. Collagen fragmentation, collagen glycation, collagen crosslinking, and aggregation of proteins in the extracellular space affect ECM integrity to accelerate agin." From [The Matrisome during Aging and Longevity](https://www.karger.com/Article/FullText/504295)

![](https://www.researchgate.net/profile/Abdelaziz-Ghanemi/publication/340352699/figure/fig1/AS:875550012895237@1585758798873/Example-of-extracellular-matrix-ECM-implications-The-extracellular-matrix-is-involved.png)

What questions can be answered computationally? One example would be age-related changes in gene expression of the ECM from publicly available [datasets](https://pubmed.ncbi.nlm.nih.gov/18757743/) of controls & reprogramming experiments.


## New hallmarks of ageing: a 2022 Copenhagen ageing meeting summary

After almost a decade, we have gotten a [formal update](https://www.aging-us.com/article/204248/text) on potential novel hallmarks of aging. Here is the list:

1. Autophagy
2. Inflammation
3. Microbiome disturbance
4. Altered mechanical properties
5. Splicing dysregulation

![](https://www.aging-us.com/article/204248/figure/f1/hero)

*Now our goal is same as for the original hallmarks. We want to describe them briefly, comment the data for them and then pose some question that can be answered computationally.*


### 1. Autophagy 

![](https://images.theconversation.com/files/436311/original/file-20211208-188518-1fyp5pw.png?ixlib=rb-1.1.0&q=45&auto=format&w=754&h=448&fit=crop&dpr=1)

Senescence and autophagy are essential cellular processes that play a role in aging. Senescent cells are damaged cells that stop dividing and secrete cytokines and chemokines that can cause inflammation in neighboring cells. This can lead to tissue damage and promote cancer. Autophagy, on the other hand, is the process by which cells break down and recycle damaged components. This can help repair and prevent damage to cells. Interventions that target pathways involved in aging often upregulate autophagy. Some drugs can also promote autophagy, which can help alleviate the hallmarks of aging.

**What are some interesting computational research questions concerning autophagy?**

If we accept that the molecular damage is confounding variable in aging process, then getting rid of damaged objects would aid in tackling the problem.

**Autophagy measuring and prediction through biomarkers:**

- Tsuboyama, Kotaro, et al. "The ATG conjugation systems are important for degradation of the inner autophagosomal membrane.„ - **gives evidence of a direct correlation between LC3-II and p62 and autophagy level**
- Bobillo Lobato, Joaquin, Maria Jiménez Hidalgo, and Luis M. Jiménez Jiménez. "Biomarkers in lysosomal storage diseases.“ --- **links potential biomarkers.**


Both together give the ability to model the autophagy (flux) levels insilico.

So the approach would look something like this:

<a href="https://ibb.co/h20my03"><img src="https://i.ibb.co/6DQWmQj/autophagy.jpg" alt="autophagy" border="0"></a>

And the potential input features, that were quantified when taking biomarkers, would be:

- Globotriaosylceramide (Gb3)
- Glucosylceramide
- Galactosylceramide
- Dermatan sulfate
- Heparan sulfate
- Hyaluronic acid
- Glycogen
- Free cholesterol
- Calbindin D
- Myostatin
- Chitotriosidase
- HbA1c
- Glucose level
- Lipofuscin [Molecular damage in aging Gladyshev et.al]
- Acidification [Molecular damage in aging Gladyshev et.al]
- enzymatic activity  [Molecular damage in aging Gladyshev et.al]
- Lysosomal-associated membrane protein expression [Molecular damage in aging Gladyshev et.al]


Alternative computational question for autophagy would be: 

> What are some drugs that exhibit the same [mode of action](https://www.emcdda.europa.eu/document-library/computer-aided-silico-approaches-mode-action-analysis-and-safety-assessment-ostarine-and-4-methylamphetamine_en) as example underneath.

Screening huge libraries of compounds, like [ZINC](https://paperswithcode.com/dataset/zinc) and after finding the same mode of action, perform [lead optimization](https://medium.com/@medicilon2004/effective-use-of-in-silico-tools-in-lead-optimization-62fd2cd3de55) might produce interesting candidates.

![](https://nintil.com/images/2020-01-05-longevity/image-20200116074340112.png)

### 2. Inflammation

![](https://www.mypathologyreport.ca/wp-content/uploads/2021/12/inflammatory-cells.jpg)

Inflammation is a response to perceived threats in the body, such as pathogens or tissue damage. While this response is beneficial in the short term, chronic inflammation, or "inflammaging," can cause tissue damage and increase the risk of developing diseases such as cancer. This type of inflammation can be triggered by factors such as the accumulation of senescent cells and unhealthy lifestyles, such as overeating.

Cellular senescence is a state in which cells stop dividing and enter a state of arrested growth. This is a natural protective mechanism that prevents damaged or potentially harmful cells from reproducing and potentially becoming cancerous. However, when a large number of senescent cells accumulate in the body, they can release harmful factors known as the senescence-associated secretory phenotype (SASP) that **can lead to chronic inflammation** and tissue damage.

**What can we potentially do computationally?** Given that [regulation of inflammation could be considered an anti-aging intervention](https://febs.onlinelibrary.wiley.com/doi/full/10.1111/febs.15061)
Finding novel targes based on the modulation of inflammatory pathways might be a viable direction.

### 3. Microbiome disturbance

![](https://newbrainnutrition.com/wp-content/uploads/2020/04/1.2.1-Dictionary-microbiome2.png)

Next-generation sequencing technologies have facilitated the identification of significant changes in the gut microbiome with [age](https://pubmed.ncbi.nlm.nih.gov/33619379/#:~:text=The%20identified%20microbiome%20pattern%20of,4%2Dyear%20follow%2Dup.). *"Our analysis identifies increasing compositional uniqueness of the gut microbiome as a component of healthy ageing, which is characterized by distinct microbial metabolic outputs in the blood."*

This includes shifts in microbial populations and reduced species diversity. These changes, combined with the age-related loss of structural integrity in the gut and other barrier tissues (e.g. the blood-brain barrier), can contribute to the development of inflammation.

### 4. Altered mechanical properties

The altered mechanical properties of cells and their extracellular environment can have significant impacts on cellular processes. For example, fibroblast senescence is accompanied by a shift from a mobile pool of actin that can be easily polymerized and depolymerized during cell motility, to stable stress fibers of f-actin anchored through focal adhesions to the substrate. This change is particularly pronounced in cells from patients with premature aging syndromes and is likely to affect cell motility and cell-cell communication. Changes in motility are particularly relevant to the aging of the innate immune system, where neutrophils from older donors can cause significant tissue damage during migration to sites of inflammation. Modification of the small G protein signaling pathways that regulate such cytoskeletal motility through treatment with statins has been shown to improve the function of older neutrophils in vitro and to result in a significant increase in 6-month mortality in older adults admitted to the ICU with pneumonia.

The nucleoskeleton also undergoes changes during aging, with the nuclear lamina becoming destabilized and chromatin being extruded into the cytoplasm as chromatin-containing bodies (CCFs) that trigger the senescence-associated secretory phenotype (SASP). Importantly, the nuclear lamina is highly defective in Hutchison-Gilford progeria, and clinical trials of farnesyl transferase inhibitors that restore nuclear envelope integrity have been shown to increase patient lifespan. One example falling into this would be the ECM we touched upon previously.

### 5. Splicing regulation

**Splicing regulatory elements (SREs)** are cis-acting sequences in pre-messenger RNA (pre-mRNA) that regulate the splicing of introns. SREs can either enhance or suppress splicing, and they act by recruiting trans-acting splicing factors that either activate or suppress the recognition of splice sites or the assembly of the spliceosome. The context-dependence of SREs can be categorized into two groups: (a) location-dependent activity, where the activity of SREs varies depending on their relative positions within pre-mRNA, and (b) gene-dependent activity, where the activity of SREs varies depending on the gene in which they are located.

Studies have shown that dysregulation of RNA processing is common in aging human populations [Holly AC, et. al. *Changes in splicing factor expression are associated with advancing age in man*] and interventions that reverse senescent phenotypes often act by restoring youthful patterns of splicing factor expression [Latorre E, et.al. *Small molecule modulation of splicing factor expression is associated with rescue from cellular senescence*]. These changes in RNA processing add to the known changes in genome integrity, transcriptional efficacy, and epigenetic regulation that occur during the aging process. So what can we investigate computationally? Having a [database of regulatory factors](https://www.encodeproject.org/software/regulatory-elements-database/), and then investigating whether they regulate the mRNA was one of the efforts [here](https://scholarworks.iupui.edu/bitstream/handle/1805/13762/Lin_iupui_0104D_10200.pdf?sequence=1). Replicating the study with newer regulatory factors and more sophisticated insilico methods is a viable option.

Final interesting research question, that one could pursue, is elucidating the combined effect of most of these hallmarks. Askin the questions of the type

## Aging clocks, causality and the future of evaluating biological age.

![](https://sbpdiscovery.org/sites/default/files/styles/720x375/public/2017-04/aging%20clock_res.jpg?itok=u4BRm2N6)

**Aging clocks** can estimate an organism's biological age, which is the age of its cells, tissues and systems. The reason why this is such an interesting question is because we need really good proxies to know wether some pertrubation worked or not. The default of administrating something and waiting for it to work, in a human model or not, is simply not feasible for longevity related studies. Aging clocks can provide valuable tools to assess health states and evaluate the effectiveness of anti-aging interventions.

There are three broad categories of the aging clocks:

* Molecular/Omics based (i.e. omics + molecules based)
* Phenotype based (i.e. retina or face based)
* Functional based (i.e. hematology)

Examples of computational research in this direction:

Deep neural networks (DNNs) can be utilized to extract valuable features from large sets of biomarkers obtained through typical blood testing. For instance, Putin et al. (2016) trained a consortium of DNNs on biochemical parameters from 62,419 individuals and obtained impressive performance in the prediction of chronological age (R2 = 0.8). Furthermore, this method allowed for feature extraction and identified albumin, glucose, alkaline phosphatase, urea, and erythrocytes as the most promising markers for predicting human chronological age (Putin et al., 2016). This exercise highlights the data mining capabilities of these modern techniques, even in extensively studied fields such as biomarkers.

Feature selection is a crucial and actionable area when considering the potential application of -omics sciences. While large-scale omics data are indispensable for providing insights into the aging phenotype, a specific number of actionable elements must be identified in order to enable intervention strategies. Galkin et al. (2020) also used deep learning (DL) to predict chronological age, but trained their algorithms on the taxonomic profiling of human gut microbiomes. This is a strategic decision, considering the increasing significance of the microbiota and, subsequently, nutrition for wellbeing and health.

The most important aspect is the input data/biomarkers that are informative in infering the biological information. Here are some different types of aging clocks, based on their input data:

* [The Epigenetic Clock](https://www.nature.com/articles/s43587-021-00134-3)
* [DeepMAge: A Methylation Aging Clock Developed with Deep Learning](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8279523/)
* [Deep Aging Clocks](https://www.cell.com/trends/pharmacological-sciences/fulltext/S0165-6147(19)30114-2)
* [Multi-omics Clocks](https://www.sciencedirect.com/science/article/abs/pii/S0047637419301976)
* [Deep learning hematological clocks](https://www.researchgate.net/figure/Deep-learning-based-hematological-clocks-demonstrated-accelerated-aging-rates-in-smokers_fig2_330398845)
* [Facial features clocks](https://www.nature.com/articles/cr201536)
* etc

It still remains to be seen wether this will be enough to infer goodness of a certain intervention. It would be great if this could be used as a clinical target proxy to pass the FDA trials. Time will tell.

Important future topic for this sort of inference is causality. Having [causal biomarkers](https://www.biorxiv.org/content/10.1101/2022.10.07.511382v1) that actually contribute to the true biological age would not only allow insight in terms of longevity, but also allow to discover novel biology as well.