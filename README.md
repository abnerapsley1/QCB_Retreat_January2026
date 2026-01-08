# UIUC's STC QCB Retreat - January 26, 2026 #
<figure>
  <img src="Images/FULL_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model">

  <figcaption>
    <strong>Figure 1:</strong> The Whole-Cell Model.
  </figcaption>
</figure>

## The Whole-Cell Model: A Unifying Framework for Quantitative Cell Biology ##
The purpose of this GitHub repository is to help researchers affiliated with the QCB know how to make meaningful contributions toward the generation of whole-cell models. As such, the majority of this repository details the various aspects of whole-cell modeling and how experimental, computational, and theoretical labs can contribute to each of these areas. First, the overall aims of whole-cell modeling are described as well as each of the individual components of a whole-cell model are explored. Next, each component of the whole-cell modeling process is broken up into subcomponents which can serve as areas of focus for individual labs or teams. It is assumed that readers of this repository already understand the importance of whole-cell modeling as this topic will not be explored here. Rather, this repository serves as a guide for researchers and professionals who desire to contribute to the creation of whole-cell models.

## Overall Aims of the Whole-Cell Model ##
The overall aim of a whole-cell model is to provide a comprehensive description of the cell state across a defined period of time (often the length of the cell cycle). The whole-cell model is comprised of a description of the cell state, its initial conditions, and the computational procedures that define how the cell state evolves over time. After being constructed, whole-cell models must be realized through the used of a combination of hardware, software, and computational pipelines. After whole-cell models have been realized and results have been generated, this data can be used to perform statistical analyses, answer biological questions, visualize output, and compare output with experimental results.

## The Cell State and Initialization ##
All whole-cell models require both a definition of and initial conditions for the cell state. 

<figure>
  <img src="Images/ONE_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model: The Cell State and Initialization">

  <figcaption>
    <strong>Figure 2:</strong> The Cell State and Initialization.
  </figcaption>
</figure>

### Hierarchical Levels of Organization ###
Defining the cell state is accomplished first by defining hierarchical levels of organization. These levels can vary across whole-cell models, but should encompass the most fine-grained level of organization (can be atoms or "effective" atoms) through the most coarse-grained level (usualy the cell itself). Not only do hierarchical levels of organization need to be defined, but so do the "laws" or computational procedures that define how fundamental units at one level of organization emerge from lower level fundamental units. In general, these laws are well defined for lower levels of organization such as how atoms make up molecules, but they are less well defined for higher levels of organization such as how a group of individual molecules constitute a subcellular organelle.

Individual labs and teams can contribute to this aspect of whole-cell modeling by developing theoretical models of how higher levels of organization emerge from lower levels of organization. For example, what are the computational procedures that can be used to convert information about the numbers and locations of specific molecules in a cell into information about the state of the subcellular organelles? Likewise, how can information about the organelles and molecules in a cell be used to define the cell type being studied or simulated?


### Dictionary of Fundamental Units ###
Each hierarchical level of organization within a whole-cell model contains "fundamental units". These are the individual objects within the specified level and correspond to physical entities within the cell. For example, at the organizational level of "Molecules", fundamental units may include various metabolites, proteins, genes, RNA molecules, etc. Additionally, at the level of "Organelles", examples of fundamental units may be the plasma membrane, nucleus, mitochondria, etc. Each fundamental unit at each level of organization should have a "type" to distinguish itself from other fundamental units. Each type of fundamental unit can then be assigned an arbitrary amount of defining information such as atomic radius, charge, mass, amino acid sequence, standardized nomenclature, etc.

A critical component of defining the cell state in a whole-cell model is a dictionary of fundamental units. This dictionary contains all the information about each fundamental unit type across all hierarchical levels of organization. In essence, it is a large lookup table with which the properties of any individual fundamental unit can be accessed. 

Individual labs and teams can contribute to this aspect of whole-cell modeling in a variety of ways. For example, all molecular species and molecular complexes within a whole-cell model need to be documented. If a lab is studying specific biological pathways or reactions, the lab can gather information about molecular species included in these reactions. Such information may include DNA-protein binding partners, stoichiometric ratios of protein complexes, or the identity of various RNA or protein isoforms. Similarly, if a lab is focused on the study of subcellular organelles, information about the sizes, molecular compositions, or functions can be used in the dictionary of fundamental units. 

### Initial Conditions ###


## Cellular Processes ##

### Molecular Dynamics ###

### Chemical Kinetics or Chemical Reaction Dynamics ###

### Dynamics of Subcellular Organelles ###


## Whole-Cell Simulations ##

### Hardware and Infrastructure ###

### Computational Software ###

### Computational Frameworks and Pipelines ###


## Model Predictions and Output ##

### Visualization ###

### Statistical Analysis and Interpretations ###

### Comparison with Experimental Results ###

