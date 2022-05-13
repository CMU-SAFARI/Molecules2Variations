# From Molecules to Genomic Variations: Accelerating Genome Analysis via Intelligent Algorithms and Architectures

We describe the ongoing journey in significantly improving the performance, accuracy, and efficiency of genome analysis using intelligent algorithms and hardware architectures. We need to read, analyze, and interpret our genomes not only quickly, but also accurately and efficiently enough to scale the analysis to population level. There currently exist major computational bottlenecks and inefficiencies throughout the entire genome analysis pipeline, because state-of-the-art genome sequencing technologies are still not able to read a genome in its entirety. Our paper is the first to provide a comprehensive survey of a prominent set of algorithmic improvement and hardware acceleration efforts for the entire genome analysis pipeline.

We explain state-of-the-art algorithmic methods and hardware-based acceleration approaches for each step of the genome analysis pipeline and provide experimental evaluations. Algorithmic approaches exploit the structure of the genome as well as the structure of the underlying hardware. Hardware-based acceleration approaches exploit specialized microarchitectures or various execution paradigms (e.g., processing inside or near memory) along with algorithmic changes, leading to new hardware/software co-designed systems. We conclude with a foreshadowing of future challenges, benefits, and research directions triggered by the development of both very low cost yet highly error prone new sequencing technologies and specialized hardware chips for genomics. We hope that these efforts and the challenges we discuss provide a foundation for future work in making genome analysis more intelligent. 


![alt text](https://github.com/CMU-SAFARI/Molecules2Variations/blob/main/Figures/Molecules2GenomicVariations.png?raw=true)

## Table of Contents
The paper covers the following topics in detail with a focus on intelligent algorithms, intelligent hardware accelerators, and intelligent hardware/software co-design.

>> Computer algorithms and hardware architectures are called intelligent if they are able to efficiently satisfy three principles, 
data-centric, data-driven, and architecture/algorithm/data-aware.
>> - [x] First, we would like to process genomic data efficiently by minimizing data movement and maximizing the efficiency with which data is handled, i.e., stored, accessed, and processed. 
>> - [x] Second, we would like to take advantage of the vast amounts of genomic data and metadata to continuously improve decision making (self-optimizing decisions) for many different use cases in science, medicine, and technology. 
>> - [x] Third, we would like to orchestrate the multiple components across the entire analysis system and adapt algorithms by understanding the structure of the underlying hardware, understanding analysis algorithms, and understanding various properties (i.e., the structure of the genome, type of sequencing data, quality of sequencing data) of each piece of data.


1. Introduction
2. Obtaining Genomic Sequencing Data
    1. Generating Sequencing Data
    2. Downloading Real Sequencing Data
    3. Simulating Sequencing Data
3. Types of Genomic Sequencing Data
    1. Short Reads
    2. Ultra-long Reads
    3. Accurate Long Reads
    4. Discussion on Types of Sequencing Reads
4. Genome Analysis Using Different Types of Sequencing Reads
5. Basecalling
    1. Illumina
    2. ONT
    3. PacBio
6. Quality Control
7. Read Mapping
    1. Accelerating Indexing and Seeding
        1. Sampling Seeds
        2. Improving Data Structures for Seed Lookups
        3. Reducing Data Movement During Indexing
    2. Accelerating Pre-Alignment Filtering
        1. Pigeonhole Principle
        2. Base Counting
        3. q-gram Filtering Approach
        4. Sparse Dynamic Programming
    3. Accelerating Sequence Alignment
        1. Accurate Alignment Accelerators
        2. Alignment Accelerators with Limited Functionality
8. Variant Calling
9. Discussion and Future Opportunities


## Citing this paper

If you use this paper in your work, please cite:

> Mohammed Alser, Joel Lindegger, Can Firtina, Nour Almadhoun, Haiyu Mao, Gagandeep Singh, Juan Gomez-Luna, Onur Mutlu. 
> "From Molecules to Genomic Variations: Accelerating Genome Analysis via Intelligent Algorithms and Architectures"
> arXiv preprint **arXiv** (2022). [link](https://arxiv.org)

Below is bibtex format for citation.

```bibtex

