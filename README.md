# Bioinfo

Adaboost based pre-computed genome-wide prediction scores for functional 5' UTR SNVs.

Description of colums:

chrom: Chromossome name

hg19_coord: The genomic coordinates, gene and transcript names were obtained from the GRCh37 (Hg19) assembly in Ensembl archive.

ref_base: The adaboost scores do not differ between diferent SNVs at the same position (example, between "A->T", "A->C", "A->G"), therefore only the reference base ("A" in this case) is annotated in the table. This refers to the base in the + strand, regardless of the gene orientation.

adaboost: Score predicted by the adaboost model, scaled between 0-1, the higher the more functional a SNV is predicted to be at the position. A single genomic position may have more than one adaboost score because the distance from the closest translation initiation site (TIS), one of the model predictors, may be different for different transcript isoforms. This takes in consideration alternative TIS sites from TISdb (Wan and Qian, 2013) found in the isoforms. Each table line contains only one score.

gene_symbol: HGNC gene symbol

strand: Gene orientation

gene: Ensemble gene name

transcripts: Ensemble transcript names containing the position and associated with the adaboost score. Multiple names separated by ";"
