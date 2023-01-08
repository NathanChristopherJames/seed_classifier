# Altered ploidy levels results in parent-of-origin effects on Arabidopsis 
# seeds

## Introduction
Seeds are a vital agricultural commodity, being used directly for human 
consumption and by being the carriers of the next generation of crops. How 
to ensure that seeds which are produced are both large and viable is 
therefore an important area of scientific investigation. One method that 
is able to affect the size of seeds is by altering their ploidy levels, 
i.e., by changing the number of chromosomal sets within the seed. 
Unfortunately, plants do not always respond well to these changes, 
resulting in a loss of seed viability. In *Arabidopsis thaliana*, the 
effects of increased ploidy levels differ depending on the parent (pollen 
or egg cell) that provided the additional chromosomal sets: maternal 
excess results in smaller seeds, while paternal excess results in larger 
seeds. Although paternal excess can induce a larger seed size, certain 
ecotypes of Arabidopsis are not able to tolerate this additional genomic 
content, exhibiting as small, dark, shriveled seeds. Thus, this phenotype 
is of interest to uncover the regulatory factors involved in controlling 
seed size and viability. 

For this experimental investigation, machine learning will be used to 
provide further support that the pollen parents did have an increased 
ploidy level that were crossed to the maternal parent. Since the wild-type 
seeds differ in both seed size and texture (shriveled or smooth), these 
characteristics will be used to aid in classification. This is only a 
basic approach to seed classification, and in the future, it is the 
author's hope to build on these skills attained in order to classify seeds 
based on data acquired through pictures and other electromagnetic 
radiation.

## Methods
Seeds have not yet been analyzed and could not be used for this 
investigation. Therefore, data will be an estimate and based on previous 
work done by Wilkins (2021). Estimated seed weights and textures will be 
replaced with actual measurements to train and test all models in the 
future.

Arabidopsis seed weight and texture have been shown to be good indicators 
of altered ploidy levels. Since these measurements provide some separation 
of data points when plotted against each other, the k-nearest neighbors 
model was used to assess the outcome of the different parental crosses. 
Mean seed weights and mean percent shriveled seeds represent the means for 
an individual seed pod (silique). Model was created using scikit-learn in 
Python. All code and info can be found at 
https://github.com/NathanChristopherJames/seed_classifier.git.

## Results
Although the k-nearest neighbors model had a score of 1, after plotting 
the model results it was noticed that the diploid (wild-type) group 
extended into the triploid group on the right of the graph. Therefore, a 
cross validation of the n_neighbors hyperparameter was performed to 
determine if there was a more suitable hyperparameter. Following the 
hyperparameter cross validation, a graph of the results did highlight that 
a smaller n_neighbors (between 1-3) would be better suited than the 
original n_neighbors of 5. After replotting these results with the new 
hyperparameter, the diploid group no longer extended into the triploid 
group, providing a more accurate model; the model score also remained at 
1. 

## Discussion
By using the k-nearest neighbors model, it was demonstrated that this 
could be a useful tool in providing additional support that the plant 
crosses performed did result in triploid embryos. By further finetuning 
the model with adjusted hyperparameters, the accuracy of the model was 
improved to the right of the plotted diploid seeds. However, to the left 
side of this grouping the current model would still classify aberrant 
seeds that are smaller with under 30% of the seed total being shriveled. 
Therefore, additional seed data for this area of the plot would be useful 
in the future; this could be satisfied with maternal excess triploid 
embryos that produce smaller seed sets. 

An additional classification of these different triploid seeds may also be 
interesting to add to the model in the future. For example, the upper left 
side of the graph is one specific ecotype of Arabidopsis, while the lower 
right side are a variety of different ecotypes. By including this 
categorical data into the model, it may extend the application of this 
machine learning tool.

## References
Wilkins, C. A. (2021). Epigenetic regulation of seed size in Arabidopsis: 
harnessing ecotype variation in paternal killer genes. Unpublished.



