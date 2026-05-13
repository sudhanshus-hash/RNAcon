# RNAcon: Prediction and Classification of ncRNAs Using Structural Information

RNAcon is a computational tool developed for the prediction and classification of non-coding RNAs, also known as ncRNAs.

The tool first discriminates coding RNA sequences from non-coding RNA sequences and then classifies non-coding RNAs into different functional classes using structural information. RNAcon uses sequence composition, RNA secondary structure prediction, graph properties, and machine learning models to support large-scale ncRNA analysis.

Web Server: https://webs.iiitd.edu.in/raghava/rnacon/



## Citation

Panwar, B., Arora, A., and Raghava, G. P. S. Prediction and classification of ncRNAs using structural information. BMC Genomics, 15, 127, 2014.

https://doi.org/10.1186/1471-2164-15-127


This tool and dataset is also available on Zenodo at https://doi.org/10.5281/zenodo.20155170



## About the Research

Non-coding RNAs are RNA transcripts that do not encode proteins but play important roles in cellular processes such as gene regulation, RNA processing, RNA modification, chromosome stability, protein stability, and developmental regulation.

With the growth of high-throughput sequencing data, there is a major need for computational methods that can identify whether a transcript is coding or non-coding and further classify ncRNAs into their respective functional families.

RNAcon was developed to perform both tasks: prediction of ncRNAs and classification of ncRNAs into different classes.

Data Compilation: For ncRNA prediction, non-coding RNA sequences were collected from the Rfam database and coding RNA sequences were collected from the RefSeq database. For ncRNA classification, the study used datasets from 18 different ncRNA classes originally used in the GraPPLE study.

Methodology: RNAcon uses an SVM-based model with tri-nucleotide composition for discriminating coding and non-coding RNA sequences. For classifying ncRNAs, RNA secondary structures were predicted using IPknot, graph properties were calculated using the igraph R package, and machine learning classifiers were used to assign ncRNAs into functional classes.



## Key Features

### 1. ncRNA Prediction

Predictive Modeling: Allows users to submit RNA sequences and predict whether they are coding or non-coding.

Tri-Nucleotide Composition: RNAcon uses tri-nucleotide composition as a simple and efficient feature for distinguishing coding and non-coding RNA sequences.

Performance: The tri-nucleotide composition-based SVM model achieved 98.98% accuracy and MCC 0.98 on the main dataset.



### 2. ncRNA Classification

Structural Classification: RNAcon classifies non-coding RNAs into different functional classes using RNA structural information.

Graph Properties: RNA secondary structures are represented as graphs, where nucleotides act as nodes and interactions act as edges.

Machine Learning Models: Different classifiers were tested, including BayesNet, NaiveBayes, MultilayerPerceptron, IBk, libSVM, SMO, and RandomForest.

Best Classifier: RandomForest performed best for classifying ncRNAs into 18 different classes using graph properties.

Performance: RNAcon achieved overall sensitivity of 0.43 and MCC 0.40, outperforming the GraPPLE method, which achieved sensitivity 0.33 and MCC 0.29.



### 3. Integrated Web-Bench

Prediction Module: Identifies whether a submitted RNA sequence is coding or non-coding.

Classification Module: Classifies predicted non-coding RNA sequences into their respective ncRNA classes.

Standalone Tool: RNAcon is also available as a standalone Linux-based command-line tool for large-scale analysis.

Fast Processing: The standalone version can process large RNA datasets efficiently, making it useful for transcriptomic and NGS-based studies.



## Applications

ncRNA Discovery: RNAcon can help identify novel non-coding RNA transcripts from large sequence datasets.

Transcriptome Analysis: The tool can support analysis of high-throughput sequencing and transcriptomic data.

Functional Annotation: RNAcon can help classify ncRNAs into functional families using structural information.

Comparative Genomics: The tool can assist in studying ncRNA classes across different organisms.

RNA Bioinformatics: RNAcon provides a computational framework for studying sequence and structure-based features of non-coding RNAs.



## Contact and Authors

Prof. Gajendra P. S. Raghava  
Corresponding Author  

Email: raghava@iiitd.ac.in

Department of Computational Biology, Indraprastha Institute of Information Technology (IIIT Delhi), New Delhi, India. 



## Support

RNAcon was developed with financial assistance from the Council of Scientific and Industrial Research and the Department of Biotechnology, Government of India.

The authors also acknowledge Dr. Ge Gao for providing the CONC dataset and Dr. Liam Childs for providing the datasets used in the GraPPLE method.
