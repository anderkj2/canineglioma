---
title: Immune Microenvironment Analysis
---

## Immunohistochemistry 

Hematoxylin & Eosin staining was used to classify glioma grade and lineage. The immunohistochemistry panel included those antibodies that have been documented to work in canine tissues and include myeloid microglia/macrophages (IBA1), monocytes (CD14) and their M2 skew subtype (CD163), and lymphoid T cells (CD3) and B cells (CD79a). Slides with 5um sections, were deparaffinized and rehydrated in a dry incubator (60°C for 1 hour), xylene, and histological grade ethanol. Antigen retrieval was performed using citrate buffer and a pressure cooker at 120°C23 for 12 minutes. Quenching for endogenous peroxidase was performed with 3% H2O2 for 15 minutes at room temperature. Non-specific binding was minimized using ready-to-use protein blocker (Dako) applied for 15 minutes before the application of the primary antibody overnight at 4°C. All the washing was done using 1x T-PBS buffer mixed with 0.1% Tween 20. The biotinylated secondary antibody was applied for 30 minutes at room temperature followed by three washes with buffer for 5 minutes each. Color development was performed using the DAKO DAB kit and color change was monitored until an appropriate detectable level was achieved (10-60 sec depending on the antibody). Slides were counterstained with hematoxylin (25 seconds) and bluing buffer, then rehydrated and cover-slipped with long lasting mounting solution. The immunohistochemistry quantification were done blindly relative to the tumor pathology. 

## Scanning and tissue segmentation

Scanning and analysis were performed using the PerkinElmer Vectra Automated Quantitative Pathology Imaging System and the inForm Cell Analysis software (ver 2.4). Slides were scanned twice on low- and high-power fields as follows: the first scan was of the whole slide on low power field (10x) for manual tissue segmentation to identify three tumor regions/categories as necrotic center, tumor and invasive edge under the neuropathologist’s supervision/direction. For each region, every fourth field was imaged (25%) on high-power field (20x) and resulted in 21 to 274 fields per slide, which varies according to the size of the tissue and presence or absence of necrosis. For the training set, heterogeneous fields were randomly selected to include tissue, non-tissue and damaged areas. Hematoxylin and DAB was used to identify the nuclei. Positive and negative cells were distinguished visually and three optical densities (OD) thresholds were set accordingly. The thresholds allowed 4-bin (0 = negative, +1 = weak positive, +2 = intermediate, +3 = strong positive) sorting of cells depending on the positivity and its intensity. The intermediate positivity threshold was calculated as the midpoint after setting the lower and higher threshold. The algorithm of the training set was applied for all the high-power fields captured. The results were inspected and the nonspecific and defective fields were removed before compiling the dataset. The same process was applied for all seven markers.


## CIBERSORT based expression analysis 

Processed RNA-seq expression matrices from canine (n=40; 25 HGG, 14 LGG, 1 unknown grade), adult (n=703; 529 LGG, 174 GBM), and pediatric glioma (n=92; 42 LGG, 50 HGG) were each run as separate jobs into the CIBERSORT webserver (https://cibersort.stanford.edu) and processed in relative mode using the following parameters: Signature Genes: LM22 CIBERSORT default, Permutations run: 100, Quantile normalization disabled (Newman et al., 2015). The resulting cellular fraction tables were then collapsed from 22 cell types into 11 based on lineage, using groupings from a prior publication (Gentles et al., 2015).