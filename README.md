# MDRIPred: Predicting Inhibitors Against Drug-Tolerant Mycobacterium tuberculosis

Welcome to the official repository for **MDRIPred**, a computational platform developed for predicting inhibitors against drug-tolerant *Mycobacterium tuberculosis* (H37Rv). The system was designed to identify compounds effective against both replicative and non-replicative phases of tuberculosis under carbon starvation conditions.

This platform supports tuberculosis drug discovery by integrating machine learning, molecular fingerprints, pharmacophore analysis, and structural feature analysis.

Web Server: http://crdd.osdd.net/oscadd/mdri/

---

# Citation

Singla, D., Tewari, R., Kumar, A., & Raghava, G. P. S. (2013).  
**Designing of inhibitors against drug tolerant Mycobacterium tuberculosis (H37Rv).**  
Chemistry Central Journal, 7, 49.  
https://doi.org/10.1186/1752-153X-7-49
https://doi.org/10.5281/zenodo.20081512
---

# About the Study

Tuberculosis (TB), caused by *Mycobacterium tuberculosis* (M.tb), remains one of the deadliest infectious diseases worldwide. The emergence of multidrug-resistant (MDR) and extensively drug-resistant (XDR) strains has created an urgent need for discovering new anti-tubercular compounds.

This study focuses on identifying inhibitors effective against:

* Replicative phase M.tb
* Non-replicative (drug-tolerant) phase M.tb

The computational models were developed using high-throughput screening datasets and machine learning approaches to accelerate anti-tuberculosis drug discovery.

---

# Dataset Information

The datasets were obtained from PubChem BioAssay screens:

* AID-492952 (Replicative phase)
* AID-488890 (Non-replicative phase)

## Replicative Dataset (Rep_dataset)

* Total compounds: 2135
* Inhibitors: 1355
* Non-inhibitors: 780

## Non-Replicative Dataset (NRep_dataset)

* Total compounds: 2135
* Inhibitors: 1206
* Non-inhibitors: 929

The compounds were processed after removing salts and ion-containing molecules.

---

# Key Features

## Machine Learning Models

Support Vector Machine (SVM)-based classification models were developed using multiple molecular fingerprint classes:

* PubChem fingerprints
* MACCS fingerprints
* EState fingerprints
* SubStructure fingerprints

The models predict whether a compound acts as an inhibitor or non-inhibitor against drug-tolerant M.tb.

---

## Best Model Performance

### Replicative Phase

* Best MCC: 0.45
* Best model: MACCS fingerprint model
* Accuracy: ~73%

### Non-Replicative Phase

* Best MCC: 0.28
* Best model: Hybrid fingerprint model
* Accuracy: ~64%

---

# Molecular Property Analysis

The study identified important physicochemical properties associated with anti-tubercular activity.

## Important Descriptors

* Molecular weight
* Polar surface area (PSA)
* Hydrogen bond acceptor count
* Rotatable bond count
* logP

---

# Important Observations

## Replicative Phase Inhibitors

Preferred properties include:

* Molecular weight > 300 Da
* Hydrogen bond acceptor > 5
* Rotatable bond count > 6
* Polar surface area > 88 Å²

## Non-Replicative Phase Inhibitors

Preferred properties include:

* Molecular weight < 380 Da
* Rotatable bond count between 2–4

These rules may assist researchers in designing new anti-tubercular molecules.

---

# Substructure Fragment Analysis

Substructure fragment analysis identified important molecular motifs associated with inhibitory activity.

## Important Fragments in Replicative Inhibitors

* hetero_N_nonbasic
* heterocyclic
* carboxylic_ester
* hetero_N_basic_no_H

## Important Fragments in Non-Replicative Inhibitors

* hetero_O
* ketone
* secondary_mixed_amine
* vinylogous_halide

## Common Important Fragments

The following fragments were important in both phases:

* Nitro
* Alkyne
* Enamine

---

# SMART Filtering

SMART filtering was applied using:

* Abbott ALARM filters
* Glaxo filters
* Pfizer LINT filters

This analysis helped identify undesirable chemical fragments related to toxicity and poor drug-like properties.

---

# Pharmacophore Analysis

Pharmacophore models were generated using first-line and second-line anti-tubercular drugs including:

* Rifampicin
* Ethambutol
* Streptomycin
* Ethionamide
* Cycloserine
* Kanamycin
* Amikacin

These pharmacophore models were used to identify structurally similar compounds within the datasets.

---

# Feature Selection Algorithm

The study introduced a novel feature selection method called:

## MCCA (Matthews Correlation Coefficient Algorithm)

MCCA was used for selecting informative fingerprints and descriptors for model development.

The method showed performance comparable or superior to frequency-based feature selection methods.

---

# Web Server Features

The MDRIPred webserver allows users to:

* Predict inhibitors against drug-tolerant M.tb
* Analyze compounds for replicative and non-replicative activity
* Perform pharmacophore similarity analysis
* Upload molecular structures
* Draw structures using JME editor

---

# Input Submission Options

Users can submit molecules using:

* JME molecular editor
* MOL/MOL2 file format
* File upload option

---

# Technologies Used

The webserver was developed using:

* Linux environment
* CGI-Perl scripts
* SVMlight package
* PaDEL descriptor software
* Pharmagist software

---

# Applications

MDRIPred can be used for:

* Anti-tuberculosis drug discovery
* Virtual screening
* Lead optimization
* QSAR studies
* Molecular property analysis
* Pharmacophore screening
* Drug resistance research

---

# Availability

The webserver is freely available for academic and research purposes.

Web Server:  
http://crdd.osdd.net/oscadd/mdri/

---

# Contact

## Prof. Gajendra P. S. Raghava

Bioinformatics Centre  
CSIR-Institute of Microbial Technology  
Chandigarh, India

Email: raghava@iiitd.ac.in

---

# License

This work is distributed under the  
**Creative Commons Attribution License**

---

# Acknowledgements

The authors acknowledge support from:

* Council of Scientific and Industrial Research (CSIR)
* Open Source Drug Discovery (OSDD)
* Department of Biotechnology (DBT)
* Government of India

We also acknowledge the PubChem BioAssay resource and the scientific community contributing to tuberculosis drug discovery research.
