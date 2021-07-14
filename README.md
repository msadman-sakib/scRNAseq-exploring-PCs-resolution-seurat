# Problem

In scRNAseq analysis, a major hyperparameter tuning step when using
`Seurat` is, selecting the principal components (PC) in the
`FindNeighbors(..., dims = ___ )` and the resolution in
`FindClusters(...,resolution = ___ )` functions. Depending upon the
data, this parameter optimization can be very tedious, as there is no
consensus for setting a specific value for these. Because ultimately,
these two values in these two functions can dramatically change the cell
embedding/projection in the UMAP plot and the number of clusters. And
based on the number of cell clusters, further analysis such as, cell
marker gene identification, renaming the cell clusters number to an
actual cell name, and performing further down-stream analysis like
differential cell type abundance or differential expression among cell
clusters. Of course, one can take a look at the ElbowPlot() and see at
which PC, the standard deviation is the lowest. But sometimes, it is
good to test out all the different PCs and resulting cell clusters from
it in a iterative approach.

# Solution:

One idea can be, to check all possible combinations of PCS and
resolutions simulatneously, to see how many cell clusters appear in the
data. From this, the researcher can make a more informed decision on
testing and selecting these two parameters.


Please go to analysis-script.md for the analysis and plots. Or click [here](https://github.com/msadman-sakib/scRNAseq-exploring-PCs-resolution-seurat/blob/master/analysis-script.md)
