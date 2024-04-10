# Hi I'm Tyler
I'm a 5th year graduate student in the [Brock Lab](https://www.brocklab.com/) at UT Austin. I combine single-cell transcriptomics, imaging, and deep learning to better understand phenotype composition, stability, and change in *in-vitro* cancer cell lines. 

Email: tyler_jost@utexas.edu

LinkedIn: www.linkedin.com/in/tyler-jost

If you are interested in trained models, imaging data, or more details, please reach out!
<!---
TylerJost/TylerJost is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
# Project Overview


## Unpublished Projects
### Deep Learning for Raman Spectroscopy
Raman spectroscopy is an imaging modality that already has multiple industrial uses for identification of chemicals. It has also been shown as a tool for label-free identification of biological matter such as pathogenic bacteria. We questioned whether it would be useful for identifying cells with minimal RNA expression differences that would normally be identifiable only through sequencing methods. While this project never reached publication status, it was an interesting venture into 3D convolutional neural networks. Previous work only used the maximum intensity image, however we hypothesized that using all of the spectra within a cell could provide a better input for a deep neural network. 

![Raman spectroscopy representations](/figures/ramanImage.png)

### Longitudinal Microscopy Database
In the field of mathematical biology, there is a strong need for the reuse of data. Machine learning has largely standardized a lot of this, and it's easy for me to try out a new network structure, etc. on MNIST, CIFAR-10, and more by just downloading the dataset. A lot of this lack of reuse could be solved by a central repository. But doing so requires something standardized and fast. To accomplish this, I designed a MySQL database as well as a frontend to access this data. This was a great way to become familiar with MySQL, specifically building out the database in a way that made sense for all types of experiments. For example, within our machine alone you can vary fluorescence, the way the amount of cells is reported, the level of depth the image was taken, and more. But after it was built, accessing the data was *much* more enjoyable than flat CSVs. 

![Entity relationship diagram](/figures/databaseRepresentation.png)
