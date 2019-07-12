# Motivation
The scalability problem is the bottleneck for applications in large-scale systems. We consider the scalability problem of Re-ID from three aspects:  
(1) low labelling cost by reducing label amount  
(2) low extension cost by reusing existing knowledge  
(3) low testing computation cost by using lightweight models.  
# Contribution
(1) We propose a Multi-teacher Adaptive Similarity Distillation Framework, which requires only a few labelled identities of target domain to transfer
knowledge from multiple teacher models to a user-specified lightweight student model without accessing source domain data.  
(2) We propose the Log-Euclidean Similarity Distillation Loss for Re-ID and further integrate the Adaptive Knowledge Aggregator to select effective teacher models to transfer target-adaptive knowledge.
# Overview
## Pipeline
![Figure 1. A scalable adaptation Re-ID system](https://github.com/xiaoaoran/PersonReID/blob/master/images/2019/CVPR2019/1_Wu_Distilled_Person_Re-Identification_Towards_a_More_Scalable_System.jpg)
## Framework
![Figure 2. Overview of the Multi-teacher Adaptive Similarity Distillation Framework](https://github.com/xiaoaoran/PersonReID/blob/master/images/2019/CVPR2019/2_Wu_Distilled_Person_Re-Identification_Towards_a_More_Scalable_System.jpg)
Let $H_S$ denote the student model to be learned andHT denote the teacher model that is fixed. The pairwise similarity matrices of the student model $H_S$ and the teacher model HT are denoted by $A_S$ and $A_T$ ,
respectively. To transfer knowledge from teacher to student,
we minimize the distance between the student similarity
matrix AS and the teacher similarity matrix AT as follow:
