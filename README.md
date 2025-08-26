<article>
    <h1>Enhanced CSI Estimation in UV MIMO Systems using Deep Learning–based Models</h1>

    <p>
      Channel estimation plays a critical role in wireless communication systems by determining the
      channel coefficients between the transmitter and receiver. These complex-valued coefficients are
      represented in the Channel State Information (CSI) matrix. The accuracy of this CSI matrix directly
      impacts system performance, data throughput, and error rates.
    </p>

    <h2>Why LS/MMSE Are Not Reliable</h2>
    <ul>
      <li><strong>High computational complexity</strong>, especially in large-scale MIMO systems.</li>
      <li><strong>Sensitivity to noise and interference</strong>, leading to unstable or inaccurate CSI values.</li>
      <li><strong>Poor generalization</strong> under varying channel conditions typical of UV links (nonlinear propagation, scattering).</li>
    </ul>

    <h2>Proposed Deep Learning Models</h2>

    <h3>1) CNN + Attention Mechanism (AM)</h3>
    <ul>
      <li>Convolutional Neural Networks (CNNs) efficiently extract spatial features from CSI matrices.</li>
      <li>Attention layers highlight the most critical features while suppressing irrelevant noise.</li>
      <li>Produces more stable and reliable CSI estimates than LS and MMSE.</li>
    </ul>

    <h3>2) CNN + AM + Transformer</h3>
    <ul>
      <li>Extends the CNN + AM model with a Transformer block.</li>
      <li>Captures long-range dependencies and global channel relationships that CNNs may miss.</li>
      <li>Further improves estimation accuracy for highly dynamic UV MIMO channels.</li>
    </ul>

    <h2>Evaluation</h2>
    <p><strong>Dataset:</strong> 20,000 synthetic CSI samples generated via a Poisson-based UV channel model.</p>
    <p><strong>Metric:</strong> Structural Similarity Index (<abbr title="Structural Similarity Index">SSIM</abbr>) on reconstructed CSI.</p>

    <h2>Results</h2>
    <ul>
      <li><strong>LS Estimation:</strong> ≈ 46% SSIM</li>
      <li><strong>MMSE Estimation:</strong> slightly higher than LS, but limited in noisy conditions</li>
      <li><strong>CNN + AM:</strong> > 55% SSIM</li>
      <li><strong>CNN + AM + Transformer:</strong> ≈ 61% SSIM</li>
    </ul>

    <h3>Simulated SSIM Results</h3>
    <figure>
      <img
        src="https://github.com/user-attachments/assets/b19fe7bd-e71f-45b9-b312-bea489e15aba"
        alt="Plot of simulated SSIM results comparing LS, MMSE, CNN+AM, and CNN+AM+Transformer"
        width="767"
        style="max-width:100%;height:auto;"
      />
      <figcaption>Simulated SSIM results across models.</figcaption>
    </figure>

    <h3>Results via Google Colab</h3>
    <figure>
      <img
        src="https://github.com/user-attachments/assets/3197bf75-9aaf-4451-b671-7efa9cff77e1"
        alt="Google Colab training and evaluation logs for the proposed models"
        width="515"
        style="max-width:100%;height:auto;"
      />
      <figcaption>Training/evaluation logs from Google Colab.</figcaption>
    </figure>

    <h2>Conclusion</h2>
    <p>
      Deep learning–based models offer a scalable, computationally efficient, and highly accurate
      alternative to traditional LS and MMSE estimators for CSI estimation in UV MIMO systems. This
      advancement enables more reliable communication in UV wireless networks, with potential applications
      in secure, high-capacity, and non-RF communication environments.
    </p>
  </article>
