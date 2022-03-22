---
layout: post
title: VKORC1 Gene Ontology Enrichment Network Analysis with [Cytoscape](https://cytoscape.org/), an open source software platform for visualizing complex networks and integrating these with any type of attribute data.
subtitle: What can the gene network interactions of VKORC1 tell me about Warfarin metabolism?
--- 

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

![VKORC1 Interaction Network](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/VKORC1_String.png)


### **Discussion**

- *VKORC1* encodes the vitamin K epoxide reductase enzyme, which is responsible for converting vitamin K epoxide to vitamin K as part of the clot signalling pathway in humans. Polymorphisms in *VKORC1* are shown too be significant contributors to Warfarin dose variance, a common anticoagulant prescribed for a variety of conditions. As one can see from the Gene Network, the neighboring gene *CYP2D6* (Cytochrome P450 2D6), which is responsible for the metabolism of many drugs and environmental chemicals according to STRING, interacts significantly with *VKORC1*. The other genes are associated with the vitamin K metabolism pathway. I mainly gather from this network the significance of looking at more than one gene than *VKORC1* when using genetic assays to predict dosage of Warfarin. It is clear to me now in a way that it was not during Project 1 that a complicated enzymatic ballet drives the metabolism of Warfarin.

## **Gene Ontology Enrichment Network**

![VKORC1 GO Network](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/VKORC1_GO.png)


## **Gene Ontology Enrichment Table**

![VKORC1 GO Table (directly from the STRING website)](https://github.com/tbrassel/tbrassel.github.io/blob/master/assets/img/GO_table.png)


### **Discussion**

- In discussion of the GO network, the BINGO app did not include every detail that STRING had on their website, however it is not wrong. It is a little difficult to read, but the terms "drug transmembrane transporter activity", "xenobiotic transporter activity", and "xenobiotic-transporting ATPase activity" show up as significantly enriched. This is consistent with the described roles of each enzyme included on the STRING website. The STRING GO table includes more detail, including "omega-hydroxylase P450 pathway" and "drug metabolism", which more accurately describes the role of *VKORC1* and associated genes. From these interactions I can postulate that metabolism of Warfarin involves membrane transport in and out of cells as well as oxidation by various Cytochrome enzymes.

