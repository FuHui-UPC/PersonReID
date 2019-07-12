# Motivation
Due to the challenging practical scenarios, current detection models often produce inaccurate bounding boxes, which inevitably degenerate the performance of existing Re-ID algorithms.
# Contibution
(1) we propose a novel coarse-to-fine pyramid model to relax the need of bounding boxes, which not only incorporates local and global information, but also inte-
grates the gradual cues between them. The pyramid model is able to match at different scales and then search for the correct image of the same identity, even when the image
pairs are not aligned.
(2) In addition, in order to learn discriminative identity representation, we explore a dynamic training scheme to seamlessly unify two losses and extract
appropriate shared information between them.
# Overview
## Problem
![image_problem](https://github.com/xiaoaoran/PersonReID/blob/master/images/2019/CVPR2019/1_Zheng_Pyramidal_Person_Re-IDentification_via_Multi-Loss_Dynamic_Training.jpg)
## Coarse to Fine Pyramidal Model
![image_model](https://github.com/xiaoaoran/PersonReID/blob/master/images/2019/CVPR2019/2_Zheng_Pyramidal_Person_Re-IDentification_via_Multi-Loss_Dynamic_Training.jpg)
First, we divide the feature map into n number of parts according to the spatial height axis and thus each basic part has the size of $C × (H/n) × W$. Suppose that $H$ can be
divisible by $n$. Thus, our pyramidal model is constructed according to the following rules: 1) In the bottom level ($l =1$) of the pyramid, there are n number of branches in which
one corresponds to a basic part. 2) The branches in higher level has one more adjacent basic part than that of previous lower level. 3) The sliding step for all levels is set to one. It
means the number of branches in the current level is just one less than that of previous level. 4) In the top level ($l = n$) of the pyramid, there is only one branch which is just the
original feature map $M$.  
![image](https://github.com/xiaoaoran/PersonReID/blob/master/images/2019/CVPR2019/3_Zheng_Pyramidal_Person_Re-IDentification_via_Multi-Loss_Dynamic_Training.jpg)
