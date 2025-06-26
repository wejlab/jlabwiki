# Resources for Developing MetaScope

A curated list of literature, tutorials, and technical documentation to support the development and improvement of the MetaScope metagenomic profiling pipeline.

---

## 📄 PathoScope Literature

- [**Comprehensive identification of pathogens in clinical samples by unbiased metagenomic sequencing**](https://genome.cshlp.org/content/23/10/1721.full.pdf+html)
    
    This foundational paper introduces the original PathoScope framework for accurate pathogen identification using metagenomic sequencing data.
    
- [**PathoScope: Metagenomic strain identification using a likelihood-based scoring method**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-15-262)
    
    Describes the underlying statistical model that enables strain-level classification from sequencing reads.
    
- [**PathoScope 2.0: A framework for strain identification in environmental or clinical samples**](https://microbiomejournal.biomedcentral.com/articles/10.1186/2049-2618-2-33)
    
    Details improvements in accuracy and speed in PathoScope 2.0, supporting complex microbial profiling tasks.
    

---

## 📘 PathoScope 2.0 Tutorial

- [**PathoScope 2.0 Extended Tutorial PDF**](https://static-content.springer.com/esm/art:10.1186/2049-2618-2-33/MediaObjects/40168_2014_59_MOESM5_ESM.pdf)
    
    A step-by-step guide explaining installation, configuration, and use of PathoScope 2.0 on real data.
    

---

## 🫁 Case Study: Asthma and the Microbiome

- [**The airway microbiome in asthma: a case-control study**](https://bmcmedgenomics.biomedcentral.com/articles/10.1186/s12920-015-0121-1)
    
    Demonstrates an application of metagenomic profiling (including PathoScope) in the analysis of airway microbiota and its link to asthma.
    

---

## 🔧 Rsubread

- [**Rsubread User Guide (PDF)**](https://bioconductor.org/packages/release/bioc/vignettes/Rsubread/inst/doc/SubreadUsersGuide.pdf)
    
    The official vignette for using Rsubread, a fast alignment and feature counting package commonly used with metagenomic pipelines.
    
- [**Rsubread in Practice: Publication Summary**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3664803/)
    
    A peer-reviewed article showcasing the performance and use cases of Rsubread.
    

---

## 🧬 Biostrings and DNAStringSet

- [**Intro to Biostrings Objects (Kasper Hansen)**](https://kasperdanielhansen.github.io/genbioconductor/html/Biostrings.html)
    
    An accessible guide to using `DNAStringSet` and related objects for string manipulation in genomics.
    
- [**Biostrings Lab Tutorial (Stanford)**](https://web.stanford.edu/class/bios221/labs/biostrings/lab_1_biostrings.html)
    
    A practical lab for learning the basics of Biostrings operations in R.
    

---

## 🗃 Working with SAM/BAM Files

- [**Rsamtools Overview**](http://bioconductor.org/packages/release/bioc/vignettes/Rsamtools/inst/doc/Rsamtools-Overview.pdf)
    
    Documentation for the `Rsamtools` package, which enables manipulation and querying of `.sam` and `.bam` files from R.
    
- [**SAM/BAM File Format Specification (HTS-specs)**](https://samtools.github.io/hts-specs/SAMv1.pdf)
    
    Technical reference for the SAM/BAM format, with a detailed explanation of file structure and headers (see page 10).
    

---

## 🧭 Reference Genomes

- [**Overview of Reference Genomes (ScienceDirect)**](https://www.sciencedirect.com/topics/neuroscience/reference-genome)
    
    A high-level overview of what reference genomes are and their importance in sequence alignment and classification.
    
- [**PathoMap (PathoScope GitHub Wiki)**](https://github.com/PathoScope/PathoScope/wiki/PathoMap)
    
    Official documentation for PathoMap, a key reference database component of the PathoScope framework.