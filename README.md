<h1>Enhanced CSI Estimation in UV MIMO Systems using Deep Learning Based models</h1>

Channel estimation plays a critical role in wireless communication systems by determining the channel coefficients between the transmitter and receiver. These coefficients, which are complex-valued, are represented in the Channel State Information (CSI) matrix. The accuracy of this CSI matrix directly impacts system performance, data throughput, and error rates.

Conventional estimation techniques such as Least Squares (LS) and Minimum Mean Square Error (MMSE) have long been used for this task. However, these methods suffer from significant drawbacks:
- High computational complexity, especially in large-scale MIMO systems.
- Sensitivity to noise and interference, leading to unstable or inaccurate CSI values.

To address these limitations, we propose deep learning–based channel estimation models designed to improve both the accuracy and robustness of CSI prediction. Our approach uses two architectures:

1. CNN + Attention Mechanism (AM):
- Convolutional Neural Networks (CNNs) efficiently extract spatial features from CSI matrices.
- Attention layers highlight the most critical features, suppressing irrelevant noise.
- This combination produces more stable and reliable CSI estimates than LS and MMSE.

2. CNN + AM + Transformer:
- Builds upon the CNN + AM model by adding a Transformer block.
- The Transformer captures long-range dependencies and global channel relationships that CNNs alone may miss.
- This hybrid model further improves estimation accuracy, making it suitable for highly dynamic UV MIMO channels.

FOR EVALUATION : 
We generated 20,000 synthetic CSI samples using a Poisson model to simulate UV channel conditions. 

The proposed models were trained and validated on this dataset. Results showed that our approach significantly outperforms traditional methods:

- LS Estimation: ~46% Structural Similarity Index (SSIM)
- MMSE Estimation: slightly higher than LS, but still limited in noisy conditions
- CNN + AM: improved SSIM beyond 55%
- CNN + AM + Transformer: achieved ~61% SSIM, representing a substantial gain in estimation accuracy.


#SIMULATED RESULTS OF SSUM WITH MODELS : 
<img width="767" alt="image" src="https://github.com/user-attachments/assets/b19fe7bd-e71f-45b9-b312-bea489e15aba" />



#RESUKTS THROUGH GOOGLE COLAB: 

<img width="515" alt="image" src="https://github.com/user-attachments/assets/3197bf75-9aaf-4451-b671-7efa9cff77e1" />


In summary, our work demonstrates that deep learning–based models provide a scalable, computationally efficient, and highly accurate alternative to traditional LS and MMSE estimators for CSI estimation in UV MIMO systems. This advancement lays the groundwork for more reliable communication in UV wireless networks, with potential applications in secure, high-capacity, and non-RF communication environments.

