# QCB Retreat - Whole-Cell Models

## 1. Why Build Whole-Cell Models?

Reasons for building whole-cell models are abundant. Below is a non-comprehensive list of various academic reasons for constructing whole-cell models:

- Provide a framework for understanding how biology emerges from physics and chemistry.
- Building a unified representation of our current biological knowledge of an organism through the integration of heterogeneous biological data.
- Create a framework for the integration of fundamental molecular pathways to build large-scale molecular networks that can be used to predict emergent cellular behaviors and phenotypes.
- Illuminating what biological processes are poorly understood and where experimental and theoretical efforts may be most productively focused.
- Establishing a logical framework from which to make quantitative biological predictions and design novel biological systems.

## 2. What is Needed to Build a Whole-Cell Model?

In general, the experimental and theoretical information that is necessary to construct whole-cell models can be divided into two categories:
1. Information about model initial conditions
2. Information about how these initial conditions evolve with time

### 2.1 Initial Conditions

Whole-cell models require information from a variety of categories to specify initial model conditions. These categories include:

#### 2.1.1 Cellular Architectures

Whole-cell models require an initial configuration for what we term the "cellular architecture". This term includes quantities such as:

**Cell shape**
- What is the morphology of the cell? Can it be approximated as a sphere, spheroid, etc.?
- What are the typical length scales?

**Cellular organelles**
- What subcellular organelles are present?
- How large are they and what are their morphologies?
- How are they distributed within the cell?

**Molecular coordinates**
- Are there certain molecules whose spatial locations are important?
  - DNA
  - Ribosomes
  - Membrane proteins
- Are these molecules found within specific organelles?

#### 2.1.2 Molecular Species List

Whole-cell models require a comprehensive list of the molecular species found within the cell. These can be divided into different categories:

**DNA**
- Genes
- Regulatory regions
- Topologically significant regions
- Replication origins

**RNA**
- mRNA
- tRNA
- rRNA
- lncRNA
- snRNA
- snoRNA

**Proteins**
- Isoforms
- PTMs

**Metabolites**

**Molecular complexes**
- DNA-DNA
- DNA-RNA
- DNA-Protein
- ...

#### 2.1.3 Molecular Species Abundances and Locations

Whole-cell modeling requires both the initial abundance and location of each molecular species to be known. Abundances can often be estimated from multiomic measurements such as:

- Whole-genome sequencing
- Transcriptomics (RNA-seq)
- Proteomics (Mass spectrometry)
- Metabolomics (Mass spectrometry, NMR, etc.)

Locations of molecular species can be determined by use of techniques such as

## 3. What Types of Biological Questions Can Whole-Cell Models Answer?

How do individual molecular networks interact to generate emergent biological phenotypes?

- Cell growth rates
- Energy utilization
- Influence of external conditions on cell behaviors
- Absolute abundances of individual molecules across the length of the cell cycle
