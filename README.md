# Hi I'm Tyler
I'm a postdoctoral research fellow in the [Laboratory for Systems Pharmacology](https://labsyspharm.org/) and [Nirmal Lab](https://nirmallab.com) at Harvard Medical School/Brigham and Women's Hospital. I combine single-cell transcriptomics, imaging, and deep learning to better understand cancer.

Email: ty.jost@gmail.com

LinkedIn: www.linkedin.com/in/tyler-jost

If you are interested in trained models, imaging data, or more details, please reach out!
<!---
TylerJost/TylerJost is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

# Project Overview
## Cluster Cleaver
clusterCleaver is a computational pipeline for analyzing cluster data in single-cell RNA sequencing (scRNAseq). You can check out our paper [here](https://www.nature.com/articles/s41540-024-00441-6). This is a scanpy-compatible package which leverages the Earth Mover's Distance (EMD) to find genes which can be used to distinguish between clusters of cells. We also validated that our method worked, separating two breast cancer transcriptomic subpopulations. I generated the algorithm and performed the sequencing analysis. 

![](/figures/231Expression.png)

UMAP and gene expression histograms for a top MDA-MB-231 cell line marker, ESAM.

Repo: https://github.com/brocklab/clusterCleaver

## This Week in Music
This week in music is a personal project I started to let myself know about live bands playing near me. I first scrape upcoming concerts near me. However, these are often presented like:
> Australian punk night presents: THE CHATS / COSMIC PSYCHOS / THE SCHIZOPHONICS

This is pretty hard to parse with just a simple regex. So I finetuned a BERT LLM to extract these names. I then used the Spotify API to add songs from these artists into a playlist for the upcoming week. Originally it was just for Austin, TX but I've now expanded it to Boston and hopefully can do it for more cities.

Repo: https://github.com/TylerJost/twia

### Cell Morphology for Transcriptomic Subpopulations
Cell morphology work often focuses on shape and texture, and typically identification is not done on subpopulations *within* a cell line but instead on other features such as metastatic variability, gene deletions, etc. We wanted to know if cells with transcriptomic changes within a cell line could also be identified using basic phase contrast imaging. To do so, we used our isolated populations found from the statistical approach mentioned above. We labeled each subpopulations and used a convolutional neural network to identify subpopulation. We found that, despite being relatively unperturbed, intra cell line populations are identifiable through computer vision. Additionally, we found that including neighborhood interactions instead of just shape and texture (possible primarily due to our use of deep learning) allowed us to improve our classification abilities. You can check out our preprint [here](https://pmc.ncbi.nlm.nih.gov/articles/PMC11245002/). It's in press and will soon be published. 

<img src=/figures/increasingBB.png width=50% height=50%>
The AUC increases (bottom) until the bounding box is made to be too large. Example images are on the top panel

Repo: https://github.com/brocklab/transcriptomicClusterMorph

<!---
Link: TBD
## Unpublished Projects
### Deep Learning for Raman Spectroscopy
Raman spectroscopy is an imaging modality that already has multiple industrial uses for identification of chemicals. It has also been demonstrated to be a reliable tool for label-free identification of biological matter such as pathogenic bacteria. We questioned whether it would be useful for identifying cells with minimal RNA expression differences that would normally be identifiable only through sequencing methods. While this project never reached publication status, it was an interesting venture into 3D convolutional neural networks. Previous work only used the maximum intensity image, however we hypothesized that using all of the spectra within a cell could provide a better input for a deep neural network. We maxed out at 80% accuracy, which is likely lower than what it can do, but gathering enough data to satisfy a deep neural network is one of the most difficult challenges that needs to be addressed on an experimental level. 

![](/figures/ramanImage.png)

Raman spectroscopy representations for a singular cell. On the left is the projection image, but the right contains all of the information for each pixel on the left. Incorporating this information could give greater insight into subtle changes in cell state.

### Longitudinal Microscopy Database
In the field of mathematical biology, there is a strong need for the reuse of data. Machine learning has largely standardized a lot of this, and it's easy for me to try out a new network structure, etc. on MNIST, CIFAR-10, and more by just downloading the dataset. A lot of this lack of reuse could be solved by a central repository. But doing so requires something standardized and fast. To accomplish this, I designed a MySQL database as well as a frontend to access this data. This was a great way to become familiar with MySQL, specifically building out the database in a way that made sense for all types of experiments. For example, within our machine alone you can vary fluorescence, the way the amount of cells is reported, the level of depth the image was taken, and more. But after it was built, accessing the data was *much* more enjoyable than flat CSVs. 

![](/figures/databaseRepresentation.png)

The entity relationship diagram for the database. 
--->
