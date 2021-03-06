# mock-5

A mock community composed of 21 bacterial strains represented in equal abundances in two replicate samples, and the same strains represented in uneven abundances in two replicate samples. These are the same community members present in mock-3 and mock-4, which consist of the same mock community samples analyzed on separate Illumina sequencing runs. This was generated by Dr. Dirk Gevers at Broad Institute in 2012.

Previously called dataset B5 in [Bokulich et al. 2015](https://dx.doi.org/10.7287/peerj.preprints.934v2).

# Known Issues / Notes

The original QUAL scores for the index/barcode reads were not recovered, and thus ``mock-index-read.fastq.gz`` contains artificial index/barcode QUAL scores. QUAL scores from all other files are original.

Note:
These barcode reads contain golay barcodes, and the mapping barcodes need to be reverse-complemented to match the reads. Run in qiime-1 using the following command:
``split_libraries_fastq.py -i mock-forward-read.fastq.gz -o split_libraries -m sample-metadata.tsv -b mock-index-read.fastq.gz --rev_comp_mapping_barcodes``
