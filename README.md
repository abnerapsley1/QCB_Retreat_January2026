# UIUC's STC QCB Retreat - January 26, 2026 #
<figure>
  <img src="Images/FULL_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model">

  <figcaption>
    <strong>Figure 1:</strong> The Whole-Cell Model
  </figcaption>
</figure>

## The Whole-Cell Model: A Unifying Framework for Quantitative Cell Biology ##
The purpose of this GitHub repository is to help researchers affiliated with the QCB know how to make meaningful contributions toward the generation of whole-cell models. As such, the majority of this repository details the various aspects of whole-cell modeling and how experimental, computational, and theoretical labs can contribute to each of these areas. First, the overall aims of whole-cell modeling are described as well as each of the individual components of a whole-cell model. Next, each component of the whole-cell modeling process is broken up into subcomponents which can serve as areas of focus for individual labs or teams. It is assumed that readers of this repository already understand the importance of whole-cell modeling as this topic will not be explored here. Rather, this repository serves as a guide for researchers and professionals who desire to contribute to the creation of whole-cell models.

## Overall Aims of the Whole-Cell Model ##
The overall aim of a whole-cell model is to provide a comprehensive description of the cell state across a defined period of time, often the length of the cell cycle (see Figure 1). The whole-cell model is comprised of a description of the cell state, its initial conditions, and the computational procedures that define how the cell state evolves over time. After being constructed, whole-cell models must be realized (or simulated) through the use of a combination of hardware, software, and computational pipelines. After whole-cell models have been simulated and results have been generated, this data can be used to perform statistical analyses, answer biological questions, visualize output, and compare output with experimental results.

## The Cell State and Initialization ##
All whole-cell models require both a definition of the cell state and initial conditions for the cell state (see Figure 2). The cell state can be thought of as a snapshot of the cell at a distinct moment in time. The cell state contains information about all aspects of the cell and it is the cell state that evolves over time in simulations of whole-cell models. A critical part of constructing a whole-cell model is defining the cell state by determining its hierarchical levels of organization, laws of emergence that relate levels of organization of the cell state to other levels, and a dictionary of all fundamental units within each level of organization. After the cell state has been defined, it also must be initialized. Each of these requirements are explained in the following subsections.  

<figure>
  <img src="Images/ONE_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model: The Cell State and Initialization">

  <figcaption>
    <strong>Figure 2:</strong> The Cell State and Initialization
  </figcaption>
</figure>

### Hierarchical Levels of Organization ###
Defining the cell state is accomplished first by defining hierarchical levels of organization. These levels can vary across whole-cell models, but should encompass the most fine-grained level of organization (can be atoms or "effective" atoms) through the most coarse-grained level (usualy the cell itself). Not only do hierarchical levels of organization need to be defined, but so do the "laws" or computational procedures that define how fundamental units at one level of organization emerge from lower level fundamental units. In general, these laws are well defined for lower levels of organization such as how atoms make up molecules, but they are less well defined for higher levels of organization such as how a group of individual molecules constitute a subcellular organelle.

Individual labs and teams can contribute to this aspect of whole-cell modeling by developing theoretical models of how higher levels of organization emerge from lower levels of organization. For example, what are the computational procedures that can be used to convert information about the numbers and locations of specific molecules in a cell into information about the state of the subcellular organelles? Likewise, how can information about the organelles and molecules in a cell be used to define the cell type being studied or simulated?

### Dictionary of Fundamental Units ###
Each hierarchical level of organization within a whole-cell model contains "fundamental units". These are the individual objects within the specified level and correspond to physical entities within the cell. For example, at the organizational level of "Molecules", fundamental units may include various metabolites, proteins, genes, RNA molecules, etc. Additionally, at the level of "Organelles", examples of fundamental units may be the plasma membrane, nucleus, mitochondria, etc. Each fundamental unit at each level of organization should have a "type" to distinguish itself from other fundamental units. Each type of fundamental unit can then be assigned an arbitrary amount of defining information such as atomic radius, charge, mass, amino acid sequence, standardized nomenclature, etc.

A critical component of defining the cell state in a whole-cell model is a dictionary of fundamental units. This dictionary contains all the information about each fundamental unit type across all hierarchical levels of organization. In essence, it is a large lookup table with which the properties of any individual fundamental unit can be accessed. 

Individual labs and teams can contribute to this aspect of whole-cell modeling in a variety of ways. For example, all molecular species and molecular complexes within a whole-cell model need to be documented. If a lab is studying specific biological pathways or reactions, the lab can gather information about molecular species included in these reactions. Such information may include DNA-protein binding partners, stoichiometric ratios of protein complexes, or the identity of various RNA or protein isoforms. Similarly, if a lab is focused on the study of subcellular organelles, information about the organelle sizes, molecular compositions, or functions can be used in the dictionary of fundamental units. 

### Initial Conditions ###
The hierarchical levels of organization and dictionary of fundamental units is required to defined the "cell state". The cell state is the overall description of the cell at every hierarchical level of organization, and as such, is composed of a list of all fundamental units present in the cell within each level. Each instance of a fundamental unit can also be supplied with information about its type, relationship with other fundamental units, and time-dependent properties. 

The status of the cell state at the beginning of the simulation (initial conditions of the cell state) must be defined before the simulation of the whole-cell model can take place. This requires information about both the abundances and locations of each type of fundamental unit.

Individual labs and teams can contribute to this aspect of whole-cell modeling in a variety of ways. First, labs that work with high-dimensional -omics data can perform experiments to determine the abundances (absolute or relative) of a wide variety of molecules within the cell. Next, labs which perform microscopy experiments can help determine initial locations of molecules and subcellular organelles. Microscopy labs can also help determine the architecture or geometries of both organelles and of the cell as a whole. This information can be used to set the initial conditions of the cell state.

## Cellular Processes ##
Once the cell state has been defined and initialized, computational procedures for the time evolution of the cell state are needed (see Figure 3). Here, we will refer to these procedures as "cellular processes". Essentially, cellular processes are computational algorithms that use various aspects of the most recent cell state as input and predict cell state variables at a specified time in the future. Cellular processes can be as fine- or coarse-grained as needed. Cellular processes may also receive input and produce output from multiple levels of organization of the cell state. Although not necessary, cellular processes often correspond to specific biological processes such as molecular diffusion, DNA replication, transcription, translation, signal transduction, cell profileration, etc.

<figure>
  <img src="Images/TWO_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model: Cellular Processes">

  <figcaption>
    <strong>Figure 3:</strong> Cellular Processes
  </figcaption>
</figure>

### Molecular Dynamics ###
An important time-dependent property of the cell state is the location of each atom or molecule within the cell. Therefore, it is important to understand how these atomic and molecular locations change with time. A well-established variety of molecular dynamics methods can be used for such cellular processes. Not all molecules or processes within a whole-cell model require this level of granularity, but for the processes that are highly dependent on molecular locations, molecular dynamics methods offer a useful solution.

Molecular dynamics simulations have varying levels of granularity in their fundamental units. Some simulations such as "all-atom" simulations track the location of individual atoms within molecules while other simulations use coarse-grained "beads" which represent multiple atoms as their fundamental units.

Using molecular dynamics simulations in whole-cell models is an active field of research with some difficulties arising due to the discrepancy of timescales for molecular and cellular simulations. Molecular simulations require a large amount of computational power and therefore can only be performed across small timescales. However, in order to perform simulations of whole-cell models, timescales corresponding to hours are often needed. 

Another benifit of molecular dynamics simulations is their ability to estimate diffusion coefficients and association/disassociation rates of molecules and molecular complexes. These simulations can be performed completely separate from a simulation of a whole-cell model, and their results can be used in creating a dictionary of the types and properties of fundamental units, as described above.

Labs and teams that have expertise in molecular dynamics can contribute to the construction of whole-cell models by developing methods for integrating molecular dynamics simulations with whole-cell model simulations. In addition, these labs and teams may contribute by determining rate constants and diffusion coefficients for specific association reactions and molecules, respectively.


### Chemical Kinetics or Chemical Reaction Dynamics ###
Another time-dependent property of the cell state is the abundance of each molecule within the cell. The evolution of molecular abundances is governed by the kinetics of chemical reactions, where molecules of one type are converted into molecules of a different type. 

Defining how molecules can be interconverted requires a variety of steps. First, researchers must construct a reaction network that defines all the possible reactions that can take place within the cell. Although much progress has been made in determining metabolic reaction networks, much work is still needed to define and refine reaction networks for the processes of DNA replication, gene regulation, transcription, translation, post-transcriptional and post-translational modifications, signal transduction, and molecular complex formation. Adding further complication to this process is the fact that many cell types have unique reaction networks, or reaction networks that are slightly different from other cell types. This is true both within and across species. Second, kinetic parameters that define the rates of these reactions must be determined. This is often done experimentally and can be both time- and labor-intensive. Other methods for determining kinetic parameters for chemical reactions include using specialized reactive force fields such as ReaxFF, quantum mechanics/molecular mechanics methods, or machine-learning methods. Third, the computational procedure for simulating chemical reactions needs to be determined. To date, there have been various methods used in whole-cell models to simulate the time evolution of chemical abundances including flux balance analysis (FBA), systems of ordinary differential equations (ODEs), the chemical master equation (CME) coupled with the Gillespie algorithm, the reaction-diffusion master equation (RDME) coupled with extensions of the Gillespie algorithm, Markov models, etc. Often, whole-cell models will use multiple methods within the same model to simulate different processes involving chemical kinetics. In these cases, a reaction network in which each reaction has a specified simulation method must be constructed.

Labs and teams can contribute to this aspect of whole-cell modeling in a variety of ways. First, labs that have the ability to delineate the subreactions that comprise biological processes can help generate detailed reaction networks. For example, labs that can uncover the order of reactions that lead to formation of protein-protein complexes can help construct realistic reaction networks that can be used to determine possible molecular transition pathways. Similarly, labs that specialize in studying gene regulation can construct detailed reaction networks that describe how transcription factors bind to DNA, histone modifications are performed, or DNA methylation markers are edited. Second, there exists an critical need for an enormous number of accurate kinetic parameters for a host of biological reactions. For example, of the ~16,000 biological reactions annotated for human cells in the Reactome database, only a very small minority of them have accurate kinetic parameters. Similarly, there exists a dearth of kinetic parameters for enzyme-catalyzed metabolic reactions for many cell types and organisms. Groups that have the ability to perform experiments or simulations that produce these missing kinetic parameters can work with groups that are building whole-cell models to determine which reactions are most critical to have accurate kinetic parameters.

### Dynamics of Subcellular Organelles ###
Whole-cell models also require information on the dynamic behaviors of subcellular organelles. Organelle geometries, locations, interactions, and molecular compositions all change as a function of time, and computational procedures that define how these processes unfold are critical for building whole-cell models. Information on organelle dynamics is important for both prokaryotic and eukaryotic cells. Although prokaryotic cells only contain a plasma membrane and cytosol, these "organelles" do change over time and these changes are vital aspects of the cell state and cellular functioning. Furthermore, understanding organelle dynamics becomes even more important when constructing eukaryotic whole-cell models because eukaryotes contain a wide array of organelles, each with its own unique functions.  

Much of the previous work on organelle dynamics has been focused on how organelles change during the process of mitosis. However, organelles also exhibit dynamic behavior within other phases of the cell cycle (i.e., G1, S, and G2). Laws governing the dynamics of organelles across the entirety of the cell cycle are needed for the generation of whole-cell models. 

Included in this category is also a description of how the overall cellular architecture evolves over time. This includes both the geometry of the plasma membrane as well as the process of cell division or proliferation. 

Individual labs and teams that study any aspect of organelle dynamics can contribute significantly to whole-cell modeling efforts. The molecular composition and geometries of membrane-bound organelles can be determined for various cell types by experimental efforts such as organelle isolation/fractionation and a combination of lipidomic and proteomic analyses. Microscopy methods are also invaluable in studying organelle geometries. Especially important are time-series experiments in which organelle information at multiple times across the cell cycle can be determined. Additionally, mathematical or computational models for the dynamic behavior of organelles and overall cellular architectures need to be established. Close collaboration between experimental and theoretical groups will hopefully lead to the development of dynamic models to predict organelle and overall cell dynamics.

## Whole-Cell Simulations ##
Once the cell state is define and initialized, and all computational procedures for the time-evolution of the cell state are in place, a whole-cell model must be realized or simulated using high-performance computing (see Figure 4). In order to perform whole-cell model simulations, hardware and infrastructure must be procured, computational software must be designed, and computational frameworks and pipelines must be established. In this area of whole-cell modeling, two main concerns are as follows: (1) reducing simulation times and costs and (2) ensuring all computational frameworks are user-friendly, reusable, and reproducible.


<figure>
  <img src="Images/THREE_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model: Whole-Cell Simulations">

  <figcaption>
    <strong>Figure 4:</strong> Whole-Cell Simulations
  </figcaption>
</figure>

### Hardware and Infrastructure ###
Computational hardware and infrastructure used for whole-cell modeling


### Computational Software ###
While previous sections described the computational procedures that predict the time-evolution of the cell state, often these procedures are realized through the implementation of specific software. Examples of this are LAMMPS or GROMACS for molecular dynamics, Lattice Microbes for chemical kinetics, and MitoTNT for tracking mitochondrial dynamics. However, presently, there are many cellular processes in whole-cell modeling that do not have dedicated software. Whole-cell modeling requires the development and maintenance of both existing and new software to efficiently perform the computations required for cellular processes. 

Labs and teams that have expertise in software development and maintanence can contribute to whole-cell modeling efforts. By working closely with groups involved in defining cellular processes, labs with software expertise can develop specialized software that is both useful and efficient. Additionally, the collaboration of labs and groups that work with either hardware or software can further optimize the software being constructed for specific hardware that will be used in whole-cell simulations.

### Computational Frameworks and Pipelines ###
After computational hardware and software have been procured and developed, whole-cell models require the creation of computational frameworks or pipelines that are both efficient and user-friendly. 

## Model Predictions and Output ##
After whole-cell simulations are complete, model output should be converted into understandable and actionable information (see Figure 5). For this to take place, model output must be statistically analyzed, visualized, and compared with experimental results. Both existing and novel methods can be used to statistically analyze the vast amount of data generated by whole-cell models. 

<figure>
  <img src="Images/FOUR_QCB_Retreat_01_26_2026.png" alt="The Whole-Cell Model: Model Predictions and Output">

  <figcaption>
    <strong>Figure 5:</strong> Model Predictions and Output
  </figcaption>
</figure>

### Statistical Analysis and Interpretations ###

### Visualization ###

### Comparison with Experimental Results ###

