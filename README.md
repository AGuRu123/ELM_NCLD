# ELM-NCLD
Online Multi-Label Classification under Noisy and Changing Label Distribution

# Abstract
  There remains two practical yet challenging issues for the task of online multi-label classification (OMC): 1) Existing OMC methods all have limitations in terms of label quality and fail to deal with the case that noisy labels occur in both relevant and irrelevant labels; 2) the ground-truth label distribution may vary with the time changing, which is hidden in the observed noisy label distribution and difficult to track. Motivated by this, we propose an online multi-label classification algorithm establishing robustness to such Noisy and Changing Label Distribution (NCLD). Firstly, an objective is designed to model the OMC framework of label scoring and thresholding. To ensure that the zero threshold can accurately separate the ground-truth positive and negative labels, the local feature graph is used to reconstruct the label scores jointly with the observed labels, and an unbiased _ranking loss_ is derived and applied to constrain relevant label scores to be higher than irrelevant label scores. Thanks to the derived closed-form solution and the sequential updating rule, a major advantage is that the online model can be efficiently updated and achieve competitive performance with respect to the batch ones. In addition, by detecting the difference between two adjacent chunks with the unbiased label cardinality, we identify the change in the ground-truth label distribution and reset the ranking or all information learned from the past to adapt to the new distribution. With all above techniques and advantages, the proposed method establishes stable and robust online classification performance under NCLD. Finally, empirical experimental results validate the effectiveness of our method in classifying instances under NCLD. 

# Main contributions
1. A practical yet challenging task namely Online Multi-label Classification (OMC) under Noisy and Changing Label Distribution (NCLD) is firstly proposed and tackled in this article.

2. We develop an ELM-based objective that incorporates a graph-based thresholding term to reconstruct credible label scores and an unbiased _ranking loss_ regularization term, which help to rationalize the zero thresholding and to give accurate label rankings under NCLD respectively.
  
3. A closed-form solution and the corresponding sequential updating rule is derived to efficiently and accurately update the online model, which firstly demonstrates the technical feasibility of applying the idea of label reconstruction to OMC works.
         
4. Under NCLD, we derive an unbiased statistic with respect to the cardinality of the label to detect ground-truth concept drift, and propose two adaptation strategies to maintain robust performance during concept drift.
 
# Reference
  Zou Y, Hu X, Li P, et al. Online multi-label classification under noisy and changing label distribution[J]. Pattern Recognition, 2025: 112892.
