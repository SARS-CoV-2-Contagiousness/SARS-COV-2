# Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness 
## Abstract
The COVID-19 pandemic, which emerged in 2019 and affected 223 countries, has caused
110 million cases and 2.5 million deaths until today (February 2020) (WHO, 2021). The
COVID-19 pandemic has reached this level of contagion as a result of the rapid spread of the
SARS-CoV-2 virus and its advantageous variants. The aforementioned advantageous variants
have occurred mainly through mutations seen on a single amino acid (dot) basis. These point
mutations may cause changes in the structure of SARS-CoV-2, as well as affect the efficiency
of interaction with the ACE2 protein, which the virus uses as the first step to enter the human
host. N501Y and E484K mutations that affect binding with ACE2 have been widely observed
in the UK, South Africa and Brazil since the beginning of 2020, and have caused concern all
over the world. In the project we designed based on this phenomenon, it was aimed to predict
the SARS-CoV-2 mutations that could be as effective as N501Y and E484K and could pose a
danger due to their high contagiousness. In line with this goal, as an original study,
experimental data on SARS-CoV-2 and ACE2 binding and stability were associated with
different amino acid properties, integrated into machine learning and computational biology
techniques, and analyzed in algorithms as a result of N501M, Q414A, N354K, Q498H,
N460K. It was determined that the N501W mutations are likely to have dangerous effects on
the spread of the coronavirus. We particularly suggest that particular attention should be paid
to the 501st position mutation, which is seen in one of the currently common variants, since
this position is repeatedly found in the lists. If these mutations are encountered during
sequencing, great sensitivity should be shown to prevent the spread of these mutations and
necessary health measures should be taken. The results of this research, conducted in the light
of machine learning and computational biology, will provide the infrastructure for future
studies on the COVID-19 pandemic and guide scientists in the fight against the virus.

## Aim of the project
Within the scope of our project, we aimed to predict which SARS-CoV-2 mutations will
increase the infectiousness of the virus by using machine learning and computational biology
techniques. For this purpose, we followed the steps below:
* Collecting information on mutations affecting the interaction between SARS-CoV-2 and
its target protein ACE2 from the literature,
* Obtaining and processing amino acid change properties that will biochemically
characterize the effect of SARS-CoV-2 mutations from the literature,
* To investigate which SARS-CoV-2 mutations may have the same effect as N501Y and
E484K mutations, using k-mean and expectation maximization algorithms to reveal the
pattern in the information listed above,
* Evaluation of mutations in the same class within the framework of the interaction between
SARS-CoV-2 and ACE2.
## Results
Within the scope of the project, we obtained the mutation-induced S-protein stability and
ACE2 binding change experimental data from Starr et al. This dataset includes 4221 S-protein
mutations. Using our self-written python code, we extracted 586 experimental mutation data
within this dataset that allowed or did not affect the S-protein binding to ACE2 better. We
then encoded these mutations in terms of also Hydropathy, Polarity, Volume, Molecular
weight, ring number in amino acid structure, oxygen number, hydrogen number and double
bond number changes and correlated them with our experimental data. Our dataset and all
pyton codes created in this way can be accessed from the link
https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-
Mutations . This set, which contains 586 mutations and includes N501Y and E484K data, was
introduced to two different machine learning grouping algorithms. Next, for different group
(cluster) numbers, it was investigated which mutations would fall into the same cluster with
the N501Y and E484K mutations. Our goal here was to remove dangerous SARS-CoV-2
mutations that could cause changes similar to the N501Y and E484K mutations. For this
purpose, we used K-means (k-means) clustering and EM (Expectation Maximization)
algorithms, which give the most consistent results among all the clustering algorithms we
have tried, through the Weka program, which is widely used for machine learning. The files
of all analysis results of the K-mean and Expectation Maximization Algorithms within the
scope of the project are given in the ANNEX-1.
### Results of the K-means clustering algorithm
| Number of Cluster | Cluster number where the E484K mutation is found | The cluster number where the N501Y mutation is located | The number of elements in the set with the E484K mutation | Number of elements in the set with the N501Y mutation |
|-------------------|--------------------------------------------------|--------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------|
| 2                 | 1                                                | 1                                                      | 445                                                       | 445                                                   |
| 3                 | 1                                                | 1                                                      | 299                                                       | 299                                                   |
| 4                 | 3                                                | 3                                                      | 164                                                       | 164                                                   |
| 5                 | 3                                                | 3                                                      | 164                                                       | 164                                                   |
| 6                 | 5                                                | 3                                                      | 118                                                       | 66                                                    |
| 7                 | 5                                                | 3                                                      | 119                                                       | 65                                                    |
| 8                 | 1                                                | 1                                                      | 57                                                        | 57                                                    |
| 9                 | 8                                                | 8                                                      | 56                                                        | 56                                                    |
| 10                | 9                                                | 9                                                      | 30                                                        | 30                                                    |
| 11                | 9                                                | 9                                                      | 30                                                        | 30                                                    |
| 12                | 9                                                | 9                                                      | 29                                                        | 29                                                    |
## Files We Used
### [Experimental Dataset](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/Experimental%20Dataset.csv)
Experimental dataset showing the effects of all possible point mutations in the Target Recognition Module (HTM) region of the S-protein of SARS-CoV-2 on ACE2 protein binding.
### [Features](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/Features.csv)
Dataset showing the hydropathy index and molecular mass of each amino acid. While creating the datasets we use, we made use of the features here.
### [editdata.py](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/editdata.py)
We created our datasets by combining the data we received from some existing datasets with this code and arranging them.
### [Dataset](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/dataset.csv)
The dataset we have created with the getdata() function in our code, which contains all the mutations in the target recognition module and the properties of hydropathy difference, molecular mass difference, binding mean, expression average, polarity difference and volume difference of these mutations. While calculating the differences, we  subtracted the property belonging to the mutant amino acid from the wildtype.
### [Dataset Bind Zero And Up](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/dataset_bind_0_and_up)
It contains mutations with a binding affinity (bind_avg) value in the dataset file equal to or greater than zero. To generate this dataset, we selected the mutations with the linking value equal to or greater than zero with the function linkmasifirveustu () in our code.
### [Dataset New Features](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/dataset_new_features) 
With the addnewfeatures() function in our code, we added the ring number difference, hydrogen atom number difference, oxygen atom number difference, double bond number difference to the dataset file.
### [Dataset_New_Features_Binding_Zero_And_Up](https://github.com/BiyoinformatikProje/Prediction-of-SARS-CoV-2-Mutations-that-Increase-Contagiousness/blob/main/Dataset_New_Features_Binding_Zero_And_Up.csv) 
The dataset where we select mutations with a binding value (bind_avg) of zero and above in the dataset new features file. We used the bind0andup() and addnewfeatures() functions to create this dataset.
