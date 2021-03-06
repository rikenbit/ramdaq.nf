# CHANGELOG

## ramdaq: Changelog

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## v1.2.2 (`-r 1.2.2`) [2021-06-22]

### `v1.2.2 Fixed`

- Fixed the problem where hyphens in sample names were converted in MultiQC

## v1.2.1 (`-r 1.2.1`) [2021-06-14]

### `v1.2.1 Added`

- Added `--entire_max_cpus` and `--entire_max_memory` options to set upper limit of CPU and memory usage of the entire workflow.

### `v1.2.1 Fixed`

- Fixed the problem of high load average for some alignment steps
- Fixed a typo in the name of the log file that is copied to the output directory

## v1.2 (`-r 1.2`) [2021-05-26]

### `v1.2 Added`

- Support for outputting gene-level quantification results of RSEM
- Added RSEM results of the number of detected genes and transcripts in MultiQC report
- Changed the unit of the number of reads from M Seqs to K Seqs in MultiQC report
- New bigWig file output from R1, R2, forward, and reverse BAM files
- Save a copy of `.nextflow.log` in the output directory

### `v1.2 Fixed`

- Fixed the caluclation of read assgined rate of all genes, mitochondrial, rRNA, and histone by featureCounts
- Fixed rRNA annotation for GRCm39
- Fixed TPM calculation for ERCC
- Corrected URL of remote annotation files in `conf/remote_annotation.config`
- Improved human rRNA annotation GTF

## v1.1 (`-r 1.1`) [2021-03-30]

### `v1.1 Added`

- The new CI-test pattern for github actions
- A new option to allow the number of ERCC copies to be specified arbitrarily
- The process of transcripts quantification using RSEM-Bowtie2
- A new annotation files (gencode mouse vM26, human v37)
- The ability to run a quantitative process for each transcript if samples contain Spike-In RNA Variant (SIRV) Control
- A new bamQC plot "Junction Annotation" from RSeQC
- The process of adjusting BED in the workflow to account for noncoding region assignments to correct
- A new config "remote_annotation.config" obtaining annotations from [public data](https://bioinformatics.riken.jp/ramdaq)

### `Fixed`

- Markdown linting error in github actions
- The problem of "_1" and "_2" in the file name being erased in MultiQC report
- The problem of MultiQC causing memory error
- An error that occurred frequently at the end of a long pipeline
- An error that occurred when drawing a histone assigned plot at only one sample.
- Hide the aggregate results of rRNA in "General Stats" of MultiQC report
- Corrected the notation "assigned to gene" to "assigned to genome"
- Output the plot even if the data are all 0

### `Dependencies`

### `Deprecated`

- igenomes.config
