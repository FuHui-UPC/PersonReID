# Motivation
The scalability problem is the bottleneck for applications in large-scale systems. We consider the scalability problem of Re-ID from three aspects:  
(1) low labelling cost by reducing label amount  
(2) low extension cost by reusing existing knowledge  
(3) low testing computation cost by using lightweight models.  
# Contribution
(1) We propose a Multi-teacher Adaptive Similarity Distillation Framework, which requires only a few labelled identities of target domain to transfer
knowledge from multiple teacher models to a user-specified lightweight student model without accessing source domain data.  
(2) We propose the Log-Euclidean Similarity Distillation Loss for Re-ID and further integrate the Adaptive Knowledge Aggregator to select effective teacher models to transfer target-adaptive knowledge.
