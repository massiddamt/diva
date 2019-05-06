# DiVA WORKFLOW
**DiVA** (DNA Variant Analysis) is a pipeline for Next-Generation Sequencing **Exome** data anlysis.
______________________________
The pipeline workflow is composed by three major analysis sections:
 * [_Mapping_](#mapping): paired-end reads in fastq format are aligned against a reference genome to produce a deduplicated and recalibrated BAM file.

 * [_Variant Calling_](#variant-calling): a joint call is performed from all project's bam files
 
 * [_Annotation_](#annotation): discovered variants are annotated and results are converted in a set of different output file formats enabling downstream analysis for all kind of users
 
A complete view of the analysis workflow is provided by the pipeline's [graph](images/diva.png).

_________________________________

### Mapping
* Trimming
* Alingment
* Sort
* Merge
* MarkDuplicates
* Recalibration



### Variant Calling
* gVCF
* joint call
* variant recalibration


### Annotation
* kggseq
* bcftools annotation
* output format


### QC
* MULTIQC:
    * FASTQC
    * Picard HsMetrics
    * Picard InsertSize
    * Picard GC bias metrics
    * VCFtools relatedness
* Bedtools Coverage    
* Picard Mendelian Violations