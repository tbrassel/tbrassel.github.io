---
layout: post
title: What can the gene network interactions of VKORC1 tell me about Warfarin metabolism?
subtitle:  VKORC1 Gene Ontology Enrichment Network Analysis with Cytoscape, an open source software platform for visualizing complex networks and integrating these with any type of attribute data.
--- 
## Cytoscape Citation
- Shannon P, Markiel A, Ozier O, Baliga NS, Wang JT, Ramage D, Amin N, Schwikowski B, Ideker T. 
Cytoscape: a software environment for integrated models of biomolecular interaction networks. Genome Research 2003 Nov; 13(11):2498-504 

# What is [Cytoscape](https://cytoscape.org/)?

![Visual Mapping for Microarray Data](https://cytoscape.org/images/screenshots/visualMapping1.png)

**Cytoscape supports many use cases in molecular and systems biology, genomics, and proteomics:**
- Load molecular and genetic interaction data sets in many standards formats
- Project and integrate global datasets and functional annotations
- Establish powerful visual mappings across these data
- Perform advanced analysis and modeling using Cytoscape Apps
- Visualize and analyze human-curated pathway datasets such as WikiPathways, Reactome, and KEGG.

***

![Twitter Social Network Visualization](https://cytoscape.org/images/screenshots/twitterVisualization1.png)

**Cytoscape is used by social scientists to:**
- Visualize and analyze large social networks of interpersonal relationships
- Assemble social networks from tables and forms
- Gather social interactions from the web by variety of web service APIs with scripting languages and save it in standard data file formats. Cytoscape supports most of the standard file formats .
- Calculate network statistics using Apps
- Use with other tools, such as R with sna/ igraph package or NetworkX, for more advanced analysis

# VKORC1 Analysis

## Load Libraries
```R
library(dplyr) 
library(tidyr) 
library(readr)
```

## **Preliminary data analysis**
##### The two tables share the *Gene* column in common.

```R
galExpData <- read_csv(file='galExpData.csv')
galFiltered_edge <- read_csv(file='galFiltered_edge.csv')
```

## **Gene Network: VKORC1**

![VKORC1 Interaction Network](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/VKORC1_String.png?raw=true)


### **Discussion**

- *VKORC1* encodes the vitamin K epoxide reductase enzyme, which is responsible for converting vitamin K epoxide to vitamin K as part of the clot signalling pathway in humans. Polymorphisms in *VKORC1* are shown too be significant contributors to Warfarin dose variance, a common anticoagulant prescribed for a variety of conditions. As one can see from the Gene Network, the neighboring gene *CYP2D6* (Cytochrome P450 2D6), which is responsible for the metabolism of many drugs and environmental chemicals according to STRING, interacts significantly with *VKORC1*. The other genes are associated with the vitamin K metabolism pathway. I mainly gather from this network the significance of looking at more than one gene than *VKORC1* when using genetic assays to predict dosage of Warfarin. A complicated enzymatic ballet drives the metabolism of Warfarin.

## **Gene Ontology Enrichment Network**

![VKORC1 GO Network](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/VKORC1_GO.png?raw=rue)


## **Gene Ontology Enrichment Table**

![VKORC1 GO Table (directly from the STRING website)](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/GO_table.png?raw=true)


### **Discussion**

- In discussion of the GO network, the BINGO app did not include every detail that STRING had on their website, however it is not wrong. It is a little difficult to read, but the terms "drug transmembrane transporter activity", "xenobiotic transporter activity", and "xenobiotic-transporting ATPase activity" show up as significantly enriched. This is consistent with the described roles of each enzyme included on the STRING website. The STRING GO table includes more detail, including "omega-hydroxylase P450 pathway" and "drug metabolism", which more accurately describes the role of *VKORC1* and associated genes. From these interactions I can postulate that metabolism of Warfarin involves membrane transport in and out of cells as well as oxidation by various Cytochrome enzymes.

