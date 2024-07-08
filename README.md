# Pseudobulk from BERLIN data

## BERLIN 1-Single_Cell_RNAseq_Analysis.R from BERLIN 

#### Read and Prepare data
    ~ Load the count file, meta file, and output folder files
    ~ Set seed and resolution
    ~ Create an output directory if it doesn't already exist
    ~ Read meta file as data frame
    ~ Read count file
    

#### Create Seurat Object and Perform Quality Control (QC)
    ~ Define a function for quality control (QC) using Seurat
    ~ Calculate percentage of mitochondrial and ribosomal genes
    ~ Filter cells based on QC criteria
    ~ Create a Seurat object and perform QC
    ~ Normalize data using LogNormalize method
    ~ Calculate cell cycle scores
    ~ Find highly variable features
    ~ Scale data by regressing out unwanted sources of variation
    ~ Perform dimensionality reduction and clustering
    ~ Find doublets using DoubletFinder

#### Using Reference databases
    ~ Load reference databases from celldex
    ~ Convert Seurat object to SingleCellExperiment
    ~ Auto-annotate cell types using reference databases from celldex
    ~ Add the celldex annotations to the metadata of the Seurat object

#### Updating Metadata
    ~ Add UMAP coordinates to the metadata
    ~ Add tSNE coordinates to the metadata


#### Saving files 
    ~ Write metadata to a file
    ~ Write seurat H5 file
    ~ Write out count data
        ~ Retrieve scaled_counts, raw counts, normalized data, scaled counts, and metadata
        ~ Add row names as a column for Alyssa Umap app
        ~ Write scaled_counts,raw_counts, normalized_data, and metadata to separate files

## BERLIN 2-Single_Cell_Post_Processing.R

#### Read and Prepare data
    ~ Load h5 file and output folder
    ~ Load the file as a Seurat object using the Load H5Seurat function
    ~ Create an output directory if it doesn't already exist

#### Find markrs and Gene Expression 
    ~ Generate the Markers for each clusters 
    ~ Set the Idents 


#### Random Cell matrix for Umap app 
    ~ Randomly sample cells
    ~ Iterate over columns of the subset Seurat object

#### Write out Gene set 
    ~ Create Single Cell Clusters list 
    ~ Save R Data file and export txt file 


## BERLIN- PSEUDOBULK 

#### Read and Prepare data
    ~ Load the count file, meta file, and output folder files
    ~ Load seurat_h5_unprocessed
    ~ Read the count file
    
#### Create Seurat Object and Perform Quality Control (QC)
    ~ Define a function for quality control (QC) using Seurat
    ~ Calculate percentage of mitochondrial and ribosomal genes
    ~ Filter cells based on QC criteria
    ~ Create a Seurat object and perform QC
    ~ Save H5 Seurat file 
    ~ Normalize data using LogNormalize method
    ~ Calculate cell cycle scores
    ~ Find highly variable features
    ~ Scale data by regressing out unwanted sources of variation

#### Pseudobulk 
    ~ Aggregate data 
    ~ Save Log normalized data and metafile 
    
    


    
    
