## Steps

* 1 Data Preprocessing 
	* Raw Unmapped Reads... (come in uBAM or FASTQ, FASTA) Reads are stored in SAM or BAM Files...
	* Do QC FastQc (FastQC)
	* Map Reads to Reference Genome (BWA-MEM) [BWA algo -> BWA-backtrack (for Illumina seq of up to 100bp), BWA-SW and BWA-MEM 70bm to 	  1MegaBP
	* Flag Duplicate Reads (MarkDuplicatesSpark - GATK)
	* Recalibrate Base Quality Scores (BaseCalibrator ApplyBQSR GATK) -> compute stats 
	* Analysis-Ready Reads...BAM 
2. Variant Calling
	* Analysis-Ready Reads 
	* Call Variants Per-Sample -> HaplotypeCaller (GATK)


Requirements:
Unix OS (MacOS, Linux, BSD)
Java 1.8

Tools:
GATK4.44
BWA
FastQC
Samtools
MultiQC