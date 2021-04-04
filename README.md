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
## Sonuçlar
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
| NNumber of Cluster | Cluster number where the E484K mutation is found |The cluster
number where the
N501Y mutation is
located| E484K'nin bulunduğu cluster'daki eleman sayısı | N501Y'nin bulunduğu cluster'daki eleman sayısı |Number of
elements in the set
with the N501Y
mutation
|----------------|-----------------------------|-----------------------------|------------------------------------------------|------------------------------------------------|
| 2              | 1                           | 1                           | 445                                            | 445                                            |
| 3              | 1                           | 1                           | 299                                            | 299                                            |
| 4              | 3                           | 3                           | 164                                            | 164                                            |
| 5              | 3                           | 3                           | 164                                            | 164                                            |
| 6              | 5                           | 3                           | 118                                            | 66                                             |
| 7              | 5                           | 3                           | 119                                            | 65                                             |
| 8              | 1                           | 1                           | 57                                             | 57                                             |
| 9              | 8                           | 8                           | 56                                             | 56                                             |
| 10             | 9                           | 9                           | 30                                             | 30                                             |
| 11             | 9                           | 9                           | 30                                             | 30                                             |
| 12             | 9                           | 9                           | 29                                             | 29                                             |

## Kullandığımız Dosyalar
### [Deneysel Veriseti](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/Deneysel_veriseti.csv)
SARS-CoV-2’nin S-proteininindeki Hedef Tanıma Modülü (HTM) bölgesindeki olası tüm nokta mutasyonların ACE2 proteinine bağlanması üzerindeki etkilerini gösteren deneysel veriseti.
### [Özellikler](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/Ozellikler.csv)
Her bir aminoaside ait hidropati indeksi ve moleküler kütleyi gösteren veriseti. Kullandığımız verisetlerini oluştururken buradaki özelliklerden yararlandık.
### [veriduzenleme.py](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriduzenleme.py)
Varolan bazı verisetlerinden aldığımız veriyi bu kodla birleştirip ve düzenleyip verisetlerimizi oluşturduk.
### [Veriseti](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti.csv)
Kodumuzdaki veriyial() fonksiyonu ile oluşturduğumuz, hedef tanıma modülü'ndeki bütün mutasyonları ve bu mutasyonların hidropati farkı, moleküler kütle farkı, bağlanma ortalaması, ekspresyon ortalaması, polarite farkı ve hacim farkı özelliklerini bulunduran veriseti. Farkları hesaplarken mutant aminoaside ait olan özelliği vahşitip aminoasidinden çıkardık.
### [Veriseti Bağlanma Sıfır ve Üstü](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti_baglanma_sifir_ve_ustu)
[veriseti](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti.csv) dosyasındaki bağlanma afinitesi (bind_avg) değeri sıfıra eşit veya sıfırdan büyük olan mutasyonları içermektedir. Bu verisetini oluşturmak için kodumuzdaki baglanmasifirveustu() fonksiyonu ile bağlanma değeri sıfıra eşit olan veya sıfırdan büyük olan mutasyonları seçtik.
### [Veriseti Yeni Özellikler](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti_yeni_ozellikler) 
[veriseti](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti.csv) dosyasına kodumuzdaki yeniozellikekle() fonksiyonuyla halka sayısı farkı, hidrojen atomu sayısı farkı, oksijen atomu sayısı farkı, çift bağ sayısı farkı özelliklerini ekledik.
### [Veriseti Yeni Özellikler Bağlanma Sıfır ve Üstü](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/Veriseti_Yeni_Ozellikler_Baglanma_Sifir_ve_Ustu.csv)
[Veriseti Yeni Özellikler](https://github.com/BiyoinformatikProje/Bulasiciligi-Arttiran-Koronavirus-SARS-CoV-2-Mutasyonlarinin-Tahmini/blob/main/veriseti_yeni_ozellikler) dosyasındaki bağlanma değeri (bind_avg) sıfır ve üstü olan mutasyonları seçtiğimiz veriseti. Bu verisetini oluşturmak için baglanmasıfırveustu() fonksiyonunu kullandık.
