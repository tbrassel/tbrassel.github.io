---
layout: post
title: Comparing Bioinformatics Databases as Applied to a Gene of Interest
subtitle: How is the VKORC1 gene responsible for the large therapeutic dosage range of the anticoagulant drug Warfarin?
---

## **VKORC1 Overview**

![[The Warfarin Pathway](https://s3.pgkb.org/pathway/PA145011114.png?versionId=WPnE8UK.Ot6e_jjG2Uq2vvHnlTAiQxNX)][logo0]

[logo0]: https://s3.pgkb.org/pathway/PA145011114.png?versionId=WPnE8UK.Ot6e_jjG2Uq2vvHnlTAiQxNX "Warfarin Pathway"
> *VKORC1* encodes the vitamin K epoxide reductase enzyme, which is responsible for converting vitamin K epoxide to vitamin K as part of the clot signalling pathway. Warfarin is a lifesaving *VKORC1* inhibitory medication used to lower the risk of deadly blood clot formation in at risk patient populations, such as the 2.6 million people living with atrial fibrillation in the United States [^1]. Doctors must carefully prescribe Warfarin: too little and a patient is not treated, too much and the patient could die of internal bleeding. Their jobs are made more difficult by the two key single nucleotide polymorphisms (SNPs) that exist of the *VKORC1* gene in the human population, both which affect Warfarin’s ability to bind to the enzyme and inhibit its activity. The first, known as *VKORC1A*, is caused by a single Guanine to Adenine transversion. This SNP affects the transcription binding site, reducing *VKORC1* transcription and consequently increasing Warfarin sensitivity. The second is caused by replacing aspartic acid with tyrosine at position 36, resulting in noticeable Warfarin resistance due to the decreased ability for the enzyme to bind to the drug[^2]. This leads to doses that varying from 2mg to 10mg once per day [^3]. Locus‐Specific DataBases (LSDB), like the Leiden Open Variation Database (LOVD) and PharmGKB, store information on gene sequence variation associated with human phenotypes and are of particular importance in dosage calculation algorithms and guidelines used by physicians in determining Warfarin dose among diverse patient populations[^4].

## **Primary Database: The Leiden Open Variation Database (LOVD)**
![[The Leiden Open Variation Database, Part of the Human Variome Project](https://pbs.twimg.com/profile_images/2455207201/logo_2012-07-20_twitter_400x400.jpg)][logo1]

[logo1]: https://pbs.twimg.com/profile_images/2455207201/logo_2012-07-20_twitter_400x400.jpg "LOVD"

> **The database documentation states that the LOVD, “focuses on the collection and display of DNA sequence variants,” with extensive support for complete clinical data as well as automatic annotation of VCF files. The most recent version 3.0 was released in 2007 and data is still being updated. Full documentation for the Leiden Open Variation Database can be found [here.](https://databases.lovd.nl/shared/docs/LOVD_manual_3.0.pdf)**

### **Types of Data and Biological Questions**
> **The Leiden Open Variation Database can answer many biological questions. As well as including information on the precise chromosomal location of the gene within the human genome, it includes categorized links to the NCBI homepage corresponding to the genomic, transcript, and intron/exon reference for a particular gene. Where this database specializes is in the recording of all publically available variants of a gene from affected individuals, including graphs and statistics on what kinds of mutations occur with what genes, as well as what diseases are commonly associated with what mutations.**

### **Primary Characteristics: Data Collection**
> **The Leiden Open Variation Database is a primary database that mainly collects information on individuals, and variants of genes observed in those individuals, from registered submitters. All submitters must go through a vetting process whereby their academic credentials and institutional associations are reviewed by curators and managers of the service. A complete submission contains information on an individual, disease and phenotype information (optional), variant screening(s), and at least one found variant. There a curator reviews the data and publishes the acceptable entries on the main webpage on the behalf of the submitter. Managers oversee curators and are responsible for large scale manipulations to the database.**

### **Data Storage, Format, and Usage**
> **Since the Leiden Open Variation Database is most concerned with the collection of genomic variants, it mainly accepts VCF, or Variant Call Format files, a type of Next Generation Sequencing format. The database is divided into five categories: genes, transcripts, variants, individuals, and diseases. Searching the LOVD is extensive, with twenty-five categories under “Variants” alone. Some searchable categories include haplotype, the database ID, the genomic DNA change that causes a particular variant, and remarks made by the curator who submitted the data. While the LOVD includes many categories of information, some subcategories like “Published as” and “Frequency” seem seldom used. These and many other subcategories are sometimes left blank, providing a patchwork array of varying information that can be difficult to navigate. Well documented code extensions as well as "out of the box" design functionality work to help make the Leiden Open Variation Database accessible to as many users as possible.** 

### **Restrictions**
> **The front end web interface of the Leiden Open Variation Database is open source and freely viewable to the public. However, the contents of this LOVD database are the intellectual property of the respective curators and are protected by copyright. Hidden from public view is the data input by registered submitters which has not been published by a curator or a manager. This is either because the data has not yet been processed, the data is not yet up to the standards of the database management team, or the data is private and will never be shared publicly. Numerous security measures are in place to keep user accounts and their associated data secure, including a safe login procedure, resistance to SQL injection and cross-site scripting, as well as password protected data manipulation forms. What is visible to the public is just the tip of the iceberg in terms of what data might be stored in the database.**

### **LOVD in Literature**
> **The Leiden Open Variation Database is a lesser known yet extensively documented database. The following review article describes the LOVD's open source, "out of the box" design philosophy for easy maintenance and management: [LOVD v.2.0: the next generation in gene variant databases.](https://onlinelibrary.wiley.com/doi/full/10.1002/humu.21438)**

### **VKORC1 in LOVD**
> **A search for *VKORC1* in the LOVD returns the gene homepage, with basic information about the gene automatically curated by NCBI. Available are an informative series of [graphs](https://databases.lovd.nl/shared/genes/VKORC1/graphs) that explain the types and proportions of genetic polymorphisms for the gene. From this view it is easy to see that the database contains 187 public variant entries, with 20 unique variations, 90% of which are substitutions.**

***

## **Secondary Database: PharmGKB**
![[The PharmGKB logo](data:image/png;base64,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)][logo2]

[logo2]: data:image/png;base64,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 "PharmGKB"
***

> **The process by which clinicians determine guidelines for drugs like Warfarin is called Pharmacogenomics, the study of the relationship
between genetic variations and how the human responds to medications. PharmGKB is a secondary database that serves to curate knowledge about the impact of genetic variation on drug response, serving as a resource to both researchers and physicians alike[^5].**

### **Types of Data and Biological Questions**
> **PharmGKB works mainly to store information which supports the reasoning behind the clinical guidelines which determine the dosage requirements of various medications. In addition to listing common gene variants as in the Leiden Open Variation Database, PharmGKB works to help clinicians interconnect the abstract study of genomics with the practice of clinical medicine. For example, an oncologist may wish to understand the pharmacogenetics of certain cancers in order to better understand what drugs to use to treat them. Clinicians can also access primary literature pertinent to the gene, gene variant, or drug of study, and can even find similar molecules which may work as experimental alternatives.**

### **Secondary Characteristics: Data Collection**
> **PharmGKB is a secondary database which uses a combination of natural language processing methods, as well as hierarchical, in-house manual curation to mine clinical reports, journal articles, as well as primary databases to provide high quality pharmacogenomic data. Every entry includes a links and downloads section to help users visit the automatically generated portions of the database.**

### **Data Storage, Format, and Usage**
![[The hierarchy of knowledge present in the PharmGKB database](https://3.bp.blogspot.com/-rggZzD7zCTw/VgQdIK7gChI/AAAAAAAABt4/tA5WoOePKXU/s1600/pyramid-brokenout-web.png)][logo3]

[logo3]: https://3.bp.blogspot.com/-rggZzD7zCTw/VgQdIK7gChI/AAAAAAAABt4/tA5WoOePKXU/s1600/pyramid-brokenout-web.png "Knowledge Pyramid"

> **PharmGKB is remarkable for its streamlined look and ample use of formatting on its webpage, creating an experience that is removed from typical databases. For example, Variant Annotation tables for particular genes include links to publications. The search bar suggests users add search terms together to create new combinations, in order to discover compare and contrast drugs, genes, and more. Format is in the form of lists of annotations and links to publications, with many sources pointing back to "AmiGO 2," a primary gene ontology database. The above image outlines how PharmGKB curates and selects it's content. The data found on PharmGKB is mainly used to determine drug interactions, dosing guidelines, as well as genes of pharmacogenomic significance for clinical researchers.**

### **Restrictions**
> **PharmGKB is managed by Stanford University and is published under a Creative Commons Attribution-ShareALike 4.0 license. This public license allows users to freely access and share the information found in PharmGKB.**

### **PharmGKB in Literature**
> **The following article titled [VKORC1 Pharmacogenomics Summary](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3086043/) uses PharmGKB as it's primary database reference to study the clinical affects of three different VKORC1 variants. Additional literature sources automatically curated by PharmGKB can be found [here.](https://www.pharmgkb.org/gene/PA133787052/literature)**

### **VKORC1 in PharmGKB**
> **A search of *VKORC1* in PharmGKB returns 47 instances of prescribing information, 33 clinical annotations, and one mechanism of action. *VKORC1* is also listed as a very important pharmacogenetics gene summary due to its stringent dosing requirements highly dependent on genetic polymorphisms.  Additional information consists of location information as well as enzyme and gene names. *VKORC1* is located on chromosome 16, “GRCh38.p7 -  chr16 : 31090842 - 31094999.” [^6] Along with common gene information, PharmGKB includes a large number of prescription study annotations that serve to support the five different sets of clinical guidelines put forth for *VKORC1* and other similar genes that affect Warfarin sensitivity.**

## **Comparison and Conclusion**

> **Locus‐Specific Data Bases (LSDB), like the Leiden Open Variation Database (LOVD) and PharmGKB, play similar roles in annotating variants of genes such as VKORC1. However, unlike LOVD not just anyone can contribute to PharmGKB. Beacause it features secondary characteristics like dosing instructions intended for use by physicians in real world settings, the curators of PharmGKB justifiably choose not to accept primary information submitted through the website, but rather primary information mined from databases of journal articles which have undergone extensive peer review. While both include detailed curation by human experts, PharmGKB employs natural language processing techniques to help assemble as much information as possible. For all the computational tools employed by PharmGKB curators, the LOVD includes detailed and extensive documentation that dives into the structure of the database, code extensions, and curation procedures used to create and manage the database. This ease of management comes at the cost of transparency; LOVD is challenged by an outdated user interface and somehwhat awkward controls. Overall these databases differ in ther primary and secondary characteristics. What makes the Leiden Open Variation Database a primary database is it's emphasis on manually uploaded data from individual researchers in small scale clinical settings, while PharmGKB is defined by it's agglomeration of clinical trials and individual studies pubished elsewhere in other primary databases as well as medical journals.**

***

[^1]: What is Atrial Fibrillation (AFib or AF)? (n.d.). Retrieved October 15, 2019, from www.heart.org website: [https://www.heart.org/en/health-topics/atrial-fibrillation/what-is-atrial-fibrillation-afib-or-af](https://www.heart.org/en/health-topics/atrial-fibrillation/what-is-atrial-fibrillation-afib-or-af)

[^2]: VKORC1 gene homepage—Global Variome shared LOVD. (n.d.). Retrieved September 28, 2019, from [https://databases.lovd.nl/shared/genes/VKORC1](https://databases.lovd.nl/shared/genes/VKORC1)

[^3]: Owen, R. P., Gong, L., Sagreiya, H., Klein, T. E., & Altman, R. B. (2010). VKORC1 Pharmacogenomics Summary. Pharmacogenetics and Genomics, 20(10), 642–644. [https://doi.org/10.1097/FPC.0b013e32833433b6](https://doi.org/10.1097/FPC.0b013e32833433b6)

[^4]: Fokkema, I. F. A. C., Taschner, P. E. M., Schaafsma, G. C. P., Celli, J., Laros, J. F. J., & Dunnen, J. T. den. (2011). LOVD v.2.0: The next generation in gene variant databases. Human Mutation, 32(5), 557–563. [https://doi.org/10.1002/humu.21438](https://doi.org/10.1002/humu.21438)

[^5]: M. Whirl-Carrillo, E.M. McDonagh, J. M. Hebert, L. Gong, K. Sangkuhl, C.F. Thorn, R.B. Altman and T.E. Klein. "Pharmacogenomics Knowledge for Personalized Medicine" Clinical Pharmacology & Therapeutics (2012) 92(4): 414-417.

[^6]: VKORC1—Overview. (n.d.). Retrieved October 15, 2019, from PharmGKB website: [https://www.pharmgkb.org/gene/PA133787052/overview](https://www.pharmgkb.org/gene/PA133787052/overview)


00_Control_Panel
    tPhrases
    tWeights
01_Output
    tOutput
02_Static_Page_Analysis
    optional spilled diagnostic output
03_Manual_Review
    manual labels / reviewer notes
04_Training_Set
    later reviewed examples
feature_name                    match_type      phrase
has_age_threshold               CONTAINS        18+
has_age_threshold               CONTAINS        21+
has_age_threshold               CONTAINS        over 18
has_age_threshold               CONTAINS        over 21
has_age_threshold               CONTAINS        18 years of age
has_age_threshold               CONTAINS        21 years of age
has_age_threshold               CONTAINS        age of majority
has_age_threshold               CONTAINS        legal age
has_age_threshold               CONTAINS        must be 18
has_age_threshold               CONTAINS        must be 21
has_age_verification_phrase      CONTAINS        age verification
has_age_verification_phrase      CONTAINS        verify your age
has_age_verification_phrase      CONTAINS        age check
has_age_verification_phrase      CONTAINS        confirm your age
has_age_verification_phrase      CONTAINS        validate your age
has_age_verification_phrase      CONTAINS        certify that you are
has_age_verification_phrase      CONTAINS        by entering you confirm
has_age_verification_phrase      CONTAINS        I am at least
has_age_verification_phrase      ALL_TERMS       verify|age
has_age_verification_phrase      ALL_TERMS       confirm|age
has_dob_phrase                  CONTAINS        date of birth
has_dob_phrase                  CONTAINS        birth date
has_dob_phrase                  CONTAINS        birth month
has_dob_phrase                  CONTAINS        birth year
has_dob_phrase                  CONTAINS        mm/dd/yyyy
has_dob_phrase                  ALL_TERMS       date|birth
has_dob_phrase                  ALL_TERMS       month|day|year
has_gate_action                 CONTAINS        enter
has_gate_action                 CONTAINS        exit
has_gate_action                 CONTAINS        continue
has_gate_action                 CONTAINS        submit
has_gate_action                 CONTAINS        confirm
has_gate_action                 CONTAINS        agree
has_gate_action                 CONTAINS        yes, I am
has_gate_action                 CONTAINS        I agree
has_gate_structure              CONTAINS        age gate
has_gate_structure              CONTAINS        age-gate
has_gate_structure              CONTAINS        age modal
has_gate_structure              CONTAINS        age popup
has_gate_structure              CONTAINS        age verification modal
has_gate_structure              CONTAINS        restricted access
has_gate_structure              CONTAINS        access restricted
has_gate_structure              CONTAINS        you must be of legal age
has_gate_structure              ALL_TERMS       age|gate
has_gate_structure              ALL_TERMS       access|restricted
has_gate_script                 CONTAINS        agegate
has_gate_script                 CONTAINS        age_gate
has_gate_script                 CONTAINS        age-check
has_gate_script                 CONTAINS        agecheck
has_gate_script                 CONTAINS        age-verification
has_gate_script                 CONTAINS        ageverification
has_gate_script                 CONTAINS        verify-age
has_gate_script                 CONTAINS        verifyage
has_gate_cookie                 CONTAINS        age_verified
has_gate_cookie                 CONTAINS        ageverified
has_gate_cookie                 CONTAINS        age_confirmed
has_gate_cookie                 CONTAINS        ageconfirmed
has_gate_cookie                 CONTAINS        verify_age
has_gate_cookie                 CONTAINS        confirmed_age
has_restricted_context          CONTAINS        adult
has_restricted_context          CONTAINS        mature
has_restricted_context          CONTAINS        age restricted
has_restricted_context          CONTAINS        restricted product
has_restricted_context          CONTAINS        not intended for minors
has_restricted_context          CONTAINS        minors are prohibited
has_store_context               CONTAINS        add to cart
has_store_context               CONTAINS        checkout
has_store_context               CONTAINS        shopping cart
has_store_context               CONTAINS        product
has_store_context               CONTAINS        quantity
has_store_context               CONTAINS        shipping
has_store_context               CONTAINS        payment
has_policy_context              CONTAINS        privacy policy
has_policy_context              CONTAINS        terms of service
has_policy_context              CONTAINS        terms and conditions
has_policy_context              CONTAINS        refund policy
has_policy_context              CONTAINS        shipping policy
has_policy_context              CONTAINS        cookie policy
has_review_blocker              CONTAINS        enable javascript
has_review_blocker              CONTAINS        checking your browser
has_review_blocker              CONTAINS        access denied
has_review_blocker              CONTAINS        forbidden
has_review_blocker              CONTAINS        captcha
has_review_blocker              CONTAINS        verify you are human
has_review_blocker              CONTAINS        cloudflare
has_review_blocker              CONTAINS        blocked
has_review_blocker              CONTAINS        unavailable
has_review_blocker              CONTAINS        password protected
has_review_blocker              CONTAINS        coming soon
has_review_blocker              CONTAINS        domain for sale
Table: tWeights
feature_name                    weight    pass_group
has_age_threshold               5         AGE
has_age_verification_phrase      5         AGE
has_dob_phrase                  4         AGE
has_gate_action                 3         GATE
has_gate_structure              4         GATE
has_gate_script                 3         GATE
has_gate_cookie                 3         GATE
has_restricted_context          2         CONTEXT
has_store_context               1         CONTEXT
has_policy_context              0         NEUTRAL
has_review_blocker              -4        BLOCKER
has_policy_only                 -4        PENALTY
has_boilerplate_only            -5        PENALTY
NORMTEXT =LAMBDA(x,LET(y,LOWER(IFERROR(x&"","")),z1,SUBSTITUTE(y,CHAR(160)," "),z2,SUBSTITUTE(z1,CHAR(10)," "),z3,SUBSTITUTE(z2,CHAR(13)," "),z4,SUBSTITUTE(z3,CHAR(9)," "),z5,SUBSTITUTE(z4,"&nbsp;"," "),z6,SUBSTITUTE(z5,"&amp;"," and "),z7,SUBSTITUTE(z6,"-"," "),z8,SUBSTITUTE(z7,"_"," "),z9,SUBSTITUTE(z8,"/"," "),TRIM(z9)))
AG_NORMALIZE_URL =LAMBDA(url,LET(raw,IFERROR(TRIM(url&""),""),IF(raw="","",LET(l,LOWER(raw),IF(OR(LEFT(l,7)="http://",LEFT(l,8)="https://"),raw,"https://"&raw)))))
AG_FETCH_HTML =LAMBDA(normalizedUrl,IF(normalizedUrl="","",IFERROR(NORMTEXT(LEFT(WEBSERVICE(normalizedUrl),32700)),"")))
AG_FETCH_STATUS =LAMBDA(normalizedUrl,html,IF(normalizedUrl="","",IF(html="","FETCH_ERROR","OK")))
MATCH_SIGNAL =LAMBDA(html,matchType,pattern,LET(h,html,p,NORMTEXT(pattern),mt,UPPER(TRIM(matchType&"")),IF(mt="CONTAINS",--ISNUMBER(SEARCH(p,h)),IF(mt="ALL_TERMS",--AND(ISNUMBER(SEARCH(TEXTSPLIT(p,"|"),h))),IF(mt="ANY_TERMS",--OR(ISNUMBER(SEARCH(TEXTSPLIT(p,"|"),h))),0)))))
AG_FEATURE_HIT =LAMBDA(html,feature,IFERROR(LET(rows,FILTER(HSTACK(tPhrases[match_type],tPhrases[phrase]),(LOWER(tPhrases[feature_name])=LOWER(feature))*(tPhrases[phrase]<>"")),mts,CHOOSECOLS(rows,1),pats,CHOOSECOLS(rows,2),--OR(MAP(mts,pats,LAMBDA(mt,p,MATCH_SIGNAL(html,mt,p))))),0))
AG_RAW_HITS =LAMBDA(html,fetchStatus,LET(features,tWeights[feature_name],MAP(features,LAMBDA(f,IF(OR(fetchStatus<>"OK",LOWER(f)="has_boilerplate_only",LOWER(f)="has_policy_only"),0,AG_FEATURE_HIT(html,f))))))
AG_FINAL_HITS =LAMBDA(rawHits,LET(features,tWeights[feature_name],policyHit,XLOOKUP("has_policy_context",features,rawHits,0),nonBoilerplateEvidence,SUM(FILTER(rawHits,(features<>"has_policy_context")*(features<>"has_policy_only")*(features<>"has_boilerplate_only"),0)),policyOnly,--AND(policyHit=1,nonBoilerplateEvidence=0),boilerplateOnly,policyOnly,IF(features="has_policy_only",policyOnly,IF(features="has_boilerplate_only",boilerplateOnly,rawHits))))
AG_SCORE =LAMBDA(hits,SUM(hits*tWeights[weight]))
AG_HAS_GROUP =LAMBDA(hits,groupName,SUM(FILTER(hits,UPPER(tWeights[pass_group])=UPPER(groupName),0))>0)
AG_MATCHED_PHRASES =LAMBDA(html,fetchStatus,IF(fetchStatus<>"OK","",IFERROR(TEXTJOIN(" | ",TRUE,UNIQUE(FILTER(tPhrases[feature_name]&":"&tPhrases[phrase],(tPhrases[phrase]<>"")*ISNUMBER(XMATCH(tPhrases[feature_name],tWeights[feature_name]))*MAP(tPhrases[match_type],tPhrases[phrase],LAMBDA(mt,p,MATCH_SIGNAL(html,mt,p)))))),"")))
AG_DECISION =LAMBDA(normalizedUrl,fetchStatus,staticScore,hits,[minScore],LET(threshold,IF(ISOMITTED(minScore),8,minScore),IF(normalizedUrl="","",IF(fetchStatus<>"OK","REVIEW",IF(AND(staticScore>=threshold,AG_HAS_GROUP(hits,"AGE"),AG_HAS_GROUP(hits,"GATE"),NOT(AG_HAS_GROUP(hits,"BLOCKER")),XLOOKUP("has_boilerplate_only",tWeights[feature_name],hits,0)=0),"PASS","REVIEW")))))
AGEGATE_TRIAGE =LAMBDA(url,[minScore],LET(normalizedUrl,AG_NORMALIZE_URL(url),html,AG_FETCH_HTML(normalizedUrl),fetchStatus,AG_FETCH_STATUS(normalizedUrl,html),rawHits,AG_RAW_HITS(html,fetchStatus),hits,AG_FINAL_HITS(rawHits),staticScore,AG_SCORE(hits),matchedPhrases,AG_MATCHED_PHRASES(html,fetchStatus),finalResult,IF(ISOMITTED(minScore),AG_DECISION(normalizedUrl,fetchStatus,staticScore,hits),AG_DECISION(normalizedUrl,fetchStatus,staticScore,hits,minScore)),HSTACK(normalizedUrl,finalResult,staticScore,fetchStatus,matchedPhrases)))
AGEGATE_RESULT =LAMBDA(url,[minScore],IF(ISOMITTED(minScore),CHOOSECOLS(AGEGATE_TRIAGE(url),2),CHOOSECOLS(AGEGATE_TRIAGE(url,minScore),2)))
AGEGATE_SCORE =LAMBDA(url,[minScore],IF(ISOMITTED(minScore),CHOOSECOLS(AGEGATE_TRIAGE(url),3),CHOOSECOLS(AGEGATE_TRIAGE(url,minScore),3)))
AGEGATE_EVIDENCE =LAMBDA(url,[minScore],IF(ISOMITTED(minScore),CHOOSECOLS(AGEGATE_TRIAGE(url),5),CHOOSECOLS(AGEGATE_TRIAGE(url,minScore),5)))
Optional for training feature output:
AGEGATE_HITS =LAMBDA(url,LET(normalizedUrl,AG_NORMALIZE_URL(url),html,AG_FETCH_HTML(normalizedUrl),fetchStatus,AG_FETCH_STATUS(normalizedUrl,html),AG_FINAL_HITS(AG_RAW_HITS(html,fetchStatus))))
AGEGATE_HIT_ROW =LAMBDA(url,TRANSPOSE(AGEGATE_HITS(url)))
Use:tOutput[result] = AGEGATE_RESULT([@url])
Diagnostic spill: =AGEGATE_TRIAGE(A2)
Training feature row, columns must match tWeights[feature_name] order: =AGEGATE_HIT_ROW([@url])

Manual Review Table

url
static_result
static_score
matched_phrases
manual_result
manual_notes
review_date
reviewer_initials

Formulas:

static_result =AGEGATE_RESULT([@url])

static_score =AGEGATE_SCORE([@url])

matched_phrases =AGEGATE_EVIDENCE([@url])

1 = reviewer confirmed adequate static evidence
0 = not enough / unclear / blocked

—

Excel Keyboard / Mouse Reference

New workbook                 Ctrl+N
Save                         Ctrl+S
Save As                      F12
Open                         Ctrl+O
Print                        Ctrl+P
Undo / Redo                  Ctrl+Z / Ctrl+Y
Find / Replace               Ctrl+F / Ctrl+H
Go To                        Ctrl+G or F5
Edit active cell             F2
Enter same value in selection Ctrl+Enter
Fill down / right            Ctrl+D / Ctrl+R
Flash Fill                   Ctrl+E
AutoSum                      Alt+=
Filter toggle                Ctrl+Shift+L
Create Table                 Ctrl+T
Select current region        Ctrl+*
Select entire table column   Ctrl+Space inside table
Select entire table row      Shift+Space inside table
Insert row/column            Ctrl+Shift++
Delete row/column            Ctrl+-
Format Cells                 Ctrl+1
Format as currency           Ctrl+Shift+$
Format as percent            Ctrl+Shift+%
Format as date               Ctrl+Shift+#
Format as number             Ctrl+Shift+!
Today / current time         Ctrl+; / Ctrl+Shift+;
Recalculate workbook         F9
Recalculate sheet            Shift+F9
Full recalculation           Ctrl+Alt+F9
Refresh all                  Ctrl+Alt+F5
Name Manager                 Ctrl+F3
Create names from selection  Ctrl+Shift+F3
Show formulas                Ctrl+`
Freeze panes mouse           View > Freeze Panes
Manual calc mouse            Formulas > Calculation Options > Manual
Power Query from table       Data > From Table/Range
Remove duplicates mouse      Data > Remove Duplicates
Data validation mouse        Data > Data Validation
Evaluate formula mouse       Formulas > Evaluate Formula

---

Alt Ribbon Paths

Manual calculation           Alt M X M
Automatic calculation        Alt M X A
Name Manager                 Alt M N
Evaluate Formula             Alt M V
Trace Precedents             Alt M P
Trace Dependents             Alt M D
Remove Arrows                Alt M A A
Sort A-Z                     Alt A S A
Sort Z-A                     Alt A S D
Advanced Filter              Alt A Q
Remove Duplicates            Alt A M
Data Validation              Alt A V V
Text to Columns              Alt A E
Refresh All                  Alt A R A
From Table/Range             Alt A P T
PivotTable                   Alt N V
Format as Table              Alt H T
Conditional Formatting       Alt H L
Wrap Text                    Alt H W
Merge Cells                  Alt H M C
Auto-Column Width.           Alt H O I

---

Workbook Build Pattern

00_Control_Panel       tables, thresholds, named variables
01_Output              final user-facing results only
02_Work                formulas / diagnostics / audit math
03_Manual_Review       human result, notes, reviewer, date
04_Training_Set        later labels for model improvement
………[add sheets]
99_Lookups             reference tables / mapping tables

---

Excel Tables

Create table            Ctrl+T
Rename table            Table Design > Table Name
Use tables, not ranges  tData[Column]
Current row             [@Column]
Entire column           tData[Column]
Headers                 tData[#Headers]
All table               tData[#All]
Totals row              tData[#Totals]

Current row value =[@Amount]

Table column sum =SUM(tData[Amount])

Current row calculation =[@Gross]-[@Fee]+[@Adjustment]

Structured XLOOKUP =XLOOKUP([@ID],tLookup[ID],tLookup[Value],"")

---

Named Formula Pattern

MYFUNC =LAMBDA(x,LET(a,x+1,b,a*2,b))

Name Manager            Ctrl+F3
Use LET for readability
Use LAMBDA for reuse
Use tables for inputs
Use named functions to avoid giant formulas

---

Error Handling

Blank if error =IFERROR(formula,"")

Default zero if error =IFERROR(formula,0)

Return REVIEW on error =IFERROR(formula,"REVIEW")

Safe text coercion =IFERROR(TRIM(A2&""),"")

Safe number coercion =IFERROR(--A2,0)

Check blank =IF(A2="","",formula)

Check numeric =IF(ISNUMBER(A2),formula,"REVIEW")

Check missing lookup =XLOOKUP(A2,tMap[Key],tMap[Value],"MISSING")

---

Core Lookup Formulas

Exact lookup =XLOOKUP(A2,tMap[Key],tMap[Value],"NOT FOUND")

Two-way lookup =INDEX(tData,MATCH(rowKey,tData[Key],0),MATCH(colName,tData[#Headers],0))

Multiple criteria lookup =XLOOKUP(1,(tData[Key1]=A2)*(tData[Key2]=B2),tData[Return],"NOT FOUND")

Return multiple columns =XLOOKUP(A2,tData[ID],tData[[Name]:[Status]],"NOT FOUND")

Approximate threshold lookup =XLOOKUP(score,tBands[Min],tBands[Label],"",1)

Last match =XLOOKUP(A2,tData[Key],tData[Value],"NOT FOUND",0,-1)

Match position =XMATCH(A2,tData[Key],0)

Return row by ID =FILTER(tData,tData[ID]=A2,"NO ROW")

---

Filter / Sort / Unique

Filter rows =FILTER(tData,tData[Status]="OPEN","NONE")

Filter multiple criteria AND =FILTER(tData,(tData[Status]="OPEN")*(tData[Amount]>0),"NONE")

Filter multiple criteria OR =FILTER(tData,(tData[Status]="OPEN")+(tData[Status]="REVIEW"),"NONE")

Unique list =UNIQUE(tData[Merchant])

Sorted unique list =SORT(UNIQUE(tData[Merchant]))

Top 10 rows by amount =TAKE(SORTBY(tData,tData[Amount],-1),10)

Choose columns =CHOOSECOLS(tData,1,3,5)

Drop first row =DROP(range,1)

Take last 5 rows =TAKE(range,-5)

---

SUMIFS / COUNTIFS / Control Totals

Sum by one condition =SUMIFS(tData[Amount],tData[Merchant],A2)

Sum by date range =SUMIFS(tData[Amount],tData[Date],">="&startDate,tData[Date],"<="&endDate)

Sum by multiple conditions =SUMIFS(tData[Amount],tData[Merchant],A2,tData[Type],B2)

Count by condition =COUNTIFS(tData[Status],"REVIEW")

Count blanks =COUNTBLANK(tData[Result])

Control total variance =SUM(tDetail[Amount])-SUM(tSummary[Amount])

Balanced? =IF(ROUND(SUM(tDetail[Amount])-SUM(tSummary[Amount]),2)=0,"BALANCED","VARIANCE")

Exception count =COUNTIFS(tData[Variance],"<>0")

Exception amount =SUMIFS(tData[Variance],tData[Variance],"<>0")

---

Date Formulas

Today =TODAY()

Now =NOW()

Month start =EOMONTH(A2,-1)+1

Month end =EOMONTH(A2,0)

Weekday number =WEEKDAY(A2,2)

Weekend flag =--(WEEKDAY(A2,2)>5)

Year-month key =TEXT(A2,"yyyy-mm")

Date from parts =DATE(year,month,day)

Days between =endDate-startDate

Business days =NETWORKDAYS(startDate,endDate)

Add business days =WORKDAY(startDate,n)

Aging bucket =IFS(days<=0,"CURRENT",days<=30,"1-30",days<=60,"31-60",days<=90,"61-90",TRUE,"90+")

---

Text Cleaning

Trim spaces =TRIM(A2)

Lowercase =LOWER(A2)

Remove nonbreaking spaces =SUBSTITUTE(A2,CHAR(160)," ")

Clean line breaks =SUBSTITUTE(SUBSTITUTE(A2,CHAR(10)," "),CHAR(13)," ")

Normalize text =LOWER(TRIM(SUBSTITUTE(SUBSTITUTE(A2,CHAR(160)," "),CHAR(10)," ")))

Contains phrase =ISNUMBER(SEARCH("phrase",LOWER(A2)))

Contains any phrase list =--OR(ISNUMBER(SEARCH(tPhrases[phrase],LOWER(A2))))

Text before delimiter =TEXTBEFORE(A2,"?")

Text after delimiter =TEXTAFTER(A2,"/")

Split text =TEXTSPLIT(A2,"|")

Join text =TEXTJOIN(" | ",TRUE,range)

Remove protocol =SUBSTITUTE(SUBSTITUTE(A2,"https://",""),"http://","")

---

URL Cleaning

Add https if missing =LET(u,TRIM(A2),l,LOWER(u),IF(OR(LEFT(l,7)="http://",LEFT(l,8)="https://"),u,"https://"&u))

Domain only rough =TEXTBEFORE(SUBSTITUTE(SUBSTITUTE(A2,"https://",""),"http://",""),"/")

Remove query string =TEXTBEFORE(A2&"?","?")

Remove trailing slash =IF(RIGHT(A2)="/",LEFT(A2,LEN(A2)-1),A2)

---

Reconciliation Formulas

Expected net =[@Gross]-[@Fee]+[@Adjustment]

Variance =ROUND([@Expected_Net]-[@Actual_Net],2)

Variance flag =IF(ABS([@Variance])>=0.01,"EXCEPTION","OK")

Percent variance =IFERROR([@Variance]/[@Expected_Net],0)

Signed direction =IF([@Variance]>0,"OVER",IF([@Variance]<0,"SHORT","BALANCED"))

Absolute variance =ABS([@Variance])

Tolerance check =IF(ABS([@Variance])<=0.01,"OK","REVIEW")

Control total by date =SUMIFS(tData[Amount],tData[Date],[@Date])

Expected settlement T+1 =XLOOKUP([@Date]+1,tACH[Process_Date],tACH[Amount],0)

T+0 to T+3 settlement window =SUMIFS(tACH[Amount],tACH[Process_Date],">="&[@Date],tACH[Process_Date],"<="&[@Date]+3)

Window variance =ROUND([@Expected_Settlement]-[@Window_ACH],2)

First date account hits zero =XLOOKUP(0,tLedger[Balance],tLedger[Date],"NO ZERO",0)

Last zero balance date =XLOOKUP(0,tLedger[Balance],tLedger[Date],"NO ZERO",0,-1)

---

Exception / Review Logic

Basic status =IFS([@fetch_status]<>"OK","REVIEW",[@score]>=8,"PASS",TRUE,"REVIEW")

Manual override =IF([@manual_result]<>"",[@manual_result],[@static_result])

Priority =IFS([@fetch_status]<>"OK","HIGH",[@score]<5,"HIGH",[@score]<8,"NORMAL",TRUE,"LOW")

Missing required field =IF(OR([@URL]="",[@Merchant]="",[@Date]=""),"MISSING","OK")

Duplicate key =IF(COUNTIFS(tData[Key],[@Key])>1,"DUPLICATE","OK")

Valid amount =IF(ISNUMBER([@Amount]),"OK","BAD AMOUNT")

Audit flag =TEXTJOIN(" | ",TRUE,IF([@Variance]<>0,"VARIANCE",""),IF([@Status]="REVIEW","REVIEW",""),IF([@Duplicate]="DUPLICATE","DUPLICATE",""))

---

Dynamic Array Row Operations

Apply formula to each row =BYROW(range,LAMBDA(r,SUM(r)))

Apply formula to each column =BYCOL(range,LAMBDA(c,AVERAGE(c)))

Map two arrays =MAP(array1,array2,LAMBDA(a,b,a-b))

Reduce list to one value =REDUCE(0,array,LAMBDA(acc,x,acc+x))

Scan running total =SCAN(0,array,LAMBDA(acc,x,acc+x))

Create sequence =SEQUENCE(10)

Horizontal stack =HSTACK(range1,range2)

Vertical stack =VSTACK(range1,range2)

---

Core Linear Algebra in Excel

Vector = one column or one row of numbers
Matrix = rectangular table of numbers
Dot product = SUMPRODUCT(vector1,vector2)
Matrix multiply = MMULT(matrixA,matrixB)
Transpose = TRANSPOSE(matrix)
Inverse = MINVERSE(matrix)
Determinant = MDETERM(matrix)
Identity matrix = MUNIT(n)

Dot product =SUMPRODUCT(xVector,wVector)

Weighted score =SUMPRODUCT(featureHits,weights)

Matrix multiply =MMULT(A,B)

Transpose matrix =TRANSPOSE(A)

Inverse matrix =MINVERSE(A)

Identity matrix =MUNIT(5)
---

Linear Algebra Patterns

Feature score =SUMPRODUCT(tFeatures[@[x1]:[x9]],tWeights[weight])

Multiple row scores =MMULT(featureMatrix,weightVector)

Normalize vector length =SQRT(SUMSQ(vector))

Unit vector =vector/SQRT(SUMSQ(vector))

Euclidean distance =SQRT(SUMXMY2(vectorA,vectorB))

Manhattan distance =SUM(ABS(vectorA-vectorB))

Cosine similarity =SUMPRODUCT(vectorA,vectorB)/(SQRT(SUMSQ(vectorA))*SQRT(SUMSQ(vectorB)))

Cosine distance =1-(SUMPRODUCT(vectorA,vectorB)/(SQRT(SUMSQ(vectorA))*SQRT(SUMSQ(vectorB))))

Centered value =x-AVERAGE(range)

Z-score =(x-AVERAGE(range))/STDEV.S(range)

Min-max scale =(x-MIN(range))/(MAX(range)-MIN(range))

Weighted average =SUMPRODUCT(values,weights)/SUM(weights)

---

Regression / Model Prep

Linear prediction =intercept+SUMPRODUCT(featureHits,coefficients)

Logistic probability =1/(1+EXP(-(intercept+SUMPRODUCT(featureHits,coefficients))))

Odds =p/(1-p)

Log odds =LN(p/(1-p))

Class by threshold =IF(probability>=0.8,"PASS","REVIEW")

Residual =actual-predicted

Squared error =(actual-predicted)^2

Mean squared error =AVERAGE(squaredErrors)

Root mean squared error =SQRT(AVERAGE(squaredErrors))

Mean absolute error =AVERAGE(ABS(actualRange-predictedRange))

---

Normal Equation Linear Regression

X = feature matrix with intercept column
y = target column
β = coefficient vector
β = (XᵀX)^-1 Xᵀy

Beta coefficients =MMULT(MMULT(MINVERSE(MMULT(TRANSPOSE(X),X)),TRANSPOSE(X)),y)

Use only when XᵀX is invertible.
If unstable, use LINEST or simpler hand-weighted model.

---

Classification Metrics

True Positive =COUNTIFS(tVal[actual],1,tVal[predicted],1)

False Positive =COUNTIFS(tVal[actual],0,tVal[predicted],1)

True Negative =COUNTIFS(tVal[actual],0,tVal[predicted],0)

False Negative =COUNTIFS(tVal[actual],1,tVal[predicted],0)

Precision =TP/(TP+FP)

Recall =TP/(TP+FN)

Accuracy =(TP+TN)/(TP+FP+TN+FN)

False positive rate =FP/(FP+TN)

Review reduction =COUNTIFS(tVal[result],"PASS")/ROWS(tVal[result])

---

Useful Statistical Formulas

Average =AVERAGE(range)

Median =MEDIAN(range)

Standard deviation =STDEV.S(range)

Variance =VAR.S(range)

Percentile =PERCENTILE.INC(range,0.95)

Rank =RANK.EQ(value,range,0)

Correlation =CORREL(rangeX,rangeY)

Covariance =COVARIANCE.S(rangeX,rangeY)

Confidence interval half-width =CONFIDENCE.T(0.05,STDEV.S(range),COUNT(range))

Lower CI =AVERAGE(range)-CONFIDENCE.T(0.05,STDEV.S(range),COUNT(range))

Upper CI =AVERAGE(range)+CONFIDENCE.T(0.05,STDEV.S(range),COUNT(range))

---

Drift / CUSUM

Mean baseline =AVERAGE(baselineRange)

Std baseline =STDEV.S(baselineRange)

Z score =([@Value]-baselineMean)/baselineStd

CUSUM positive =MAX(0,previousCUSUM+[@Value]-target-k)

CUSUM negative =MIN(0,previousCUSUM+[@Value]-target+k)

Simple cumulative variance =SUM(INDEX(tData[Variance],1):[@Variance])

Running total with SCAN =SCAN(0,tData[Variance],LAMBDA(a,b,a+b))

---
SQL mental model
Excel Table      = table
Power Query      = ETL pipeline
Loaded Table     = view/output
PivotTable       = grouped report
XLOOKUP          = left join for one return field
Power Query Merge= database join

---

Data Validation Lists

Simple list source
PASS,REVIEW,FAIL,N/A

Table-backed list source =tStatusList[Status]

Manual result options
PASS
REVIEW
FAIL
N/A

---

Conditional Formatting Rules

Variance <> 0           highlight exception
ABS(variance) > tolerance    high exception
fetch_status = FETCH_ERROR     review color
result = REVIEW                review color
duplicate = DUPLICATE       duplicate color
manual_result <> static_result  check color
blank required field     missing data color

Formula rule examples =$D2<>0
=ABS($D2)>0.01
=$E2="REVIEW"
=$F2="FETCH_ERROR"
=COUNTIF($A:$A,$A2)>1

---

Data QA Checklist Formulas

Row count =ROWS(tData)

Unique key count =ROWS(UNIQUE(tData[Key]))

Duplicate count =ROWS(tData)-ROWS(UNIQUE(tData[Key]))

Blank required fields =COUNTBLANK(tData[Required_Field])

Min date =MIN(tData[Date])

Max date =MAX(tData[Date])

Total amount =SUM(tData[Amount])

Positive amount total =SUMIFS(tData[Amount],tData[Amount],">0")

Negative amount total =SUMIFS(tData[Amount],tData[Amount],"<0")

Check total equals source =IF(ROUND(SUM(tData[Amount])-sourceTotal,2)=0,"OK","CHECK")

---

Clean Model Pattern

Raw data table
→ clean normalized fields
→ lookup/mapping fields
→ feature flags
→ score
→ rule result
→ manual review override
→ final output

Final result =IF([@manual_result]<>"",[@manual_result],[@static_result])

Reason code =TEXTJOIN(" | ",TRUE,IF([@score]<8,"LOW SCORE",""),IF([@fetch_status]<>"OK","FETCH ERROR",""),IF([@manual_result]<>"","MANUAL OVERRIDE",""))
