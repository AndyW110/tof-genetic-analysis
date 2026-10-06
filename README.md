# Rare de novo variants in non-syndromic tetralogy of Fallot: a compact genomic analysis

A small, end-to-end re-analysis of published de novo variants from non-syndromic
tetralogy of Fallot (TOF), built as a reproducible data-analysis demonstration.

## Overview
Starting from publicly released supplementary variant tables, this project performs
data cleaning, gene-set cross-referencing, statistical testing and visualisation of
rare, protein-altering de novo variants in TOF probands.

## Data sources
- Page et al. (2023), *Frontiers in Cardiovascular Medicine* — 362 non-syndromic TOF
  probands; Supplementary Tables 1-3 (PMC10569225).
- Richter et al. (2020), *Nature Genetics* — curated CHD / chromatin / cilia gene sets
  (Supplementary Table 5; repository `frichter/wgs_chd_analysis`, MIT licence).

No controlled-access or patient-level data are redistributed here.

## Workflow
1. Load and clean 183 moderate/high-impact de novo variants (handle missing CADD,
   standardise gene symbols).
2. Describe variant consequences and the CADD score distribution.
3. Cross-reference curated human CHD, chromatin and cilia gene sets, plus the 13
   cardiovascular genes reported by Page et al.
4. Statistical tests: Fisher's exact test (LoF enrichment in known TOF genes) and
   Mann-Whitney U (CADD comparison); fetal-heart expression summary.
5. Visualise consequences, LoF burden, CADD, recurrently hit genes, gene-set overlap
   and pathway enrichment.

## Key findings
- 183 variants map to 179 genes across 144 probands; 120 variants have CADD >= 20.
- **CHD7** and **WASHC5** are recurrently hit known TOF genes; **CLUH** and **UNC13C**
  are recurrent novel candidates.
- Variants are enriched for cardiovascular morphogenesis, ventricle formation,
  septal development, muscle contraction and cytoskeleton organisation.
- LoF variants are enriched in known TOF genes (Fisher OR ~4.2, p ~0.027), and
  variants in those genes have higher CADD scores (Mann-Whitney p ~0.031).
- ~71% of variants with data lie in genes expressed in the fetal heart.

## Reproducibility
Open `TOF_analysis_colab.ipynb` in
[Google Colab](https://colab.research.google.com) and run all cells; data download is
automatic and requires no local installation.

## Limitations
This project starts from published variant tables and does not re-run read-level
variant calling. Case-control de novo rates were not significantly different in the
original study. Future work would use controlled-access data (dbGaP phs001194) with
read-level calling, non-coding (HeartENN) and structural-variant analyses, and
gene-level burden tests.

## References
- Page et al. 2023, Front. Cardiovasc. Med., PMC10569225.
- Richter et al. 2020, Nat. Genet. 52, 769-777.

Author: Andy· for training and skills demonstration only.
