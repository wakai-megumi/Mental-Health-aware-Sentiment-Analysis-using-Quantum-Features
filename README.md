\# Mental Health–Aware Sentiment Analysis using Quantum-Enhanced Features



This repository contains the implementation and experimental artifacts for the study \*\*“Mental Health–Aware Sentiment Analysis using Quantum-Enhanced Features”\*\*.  

The work investigates a \*\*hybrid quantum–classical learning framework\*\* for large-scale sentiment analysis and its extension to \*\*temporally aware behavioral modeling\*\* using social media data.



The primary goal of this repository is to ensure \*\*transparency, reproducibility, and empirical validation\*\* of the proposed architecture, rather than to provide a production-ready diagnostic system.



---



\## Overview of the Framework



The proposed system integrates three main components:



1\. \*\*Classical Sequential Encoding\*\*  

&nbsp;  A BiLSTM-based encoder learns contextual and temporal dependencies in text sequences.



2\. \*\*Quantum-Enhanced Feature Transformation\*\*  

&nbsp;  A lightweight variational quantum circuit (entanglement with angle encoding) is used as a nonlinear feature transformation layer.  

&nbsp;  This module operates at the \*\*feature level\*\*, not as a full quantum recurrent network, ensuring scalability under NISQ-era constraints.



3\. \*\*Temporal Aggregation for Behavioral Analysis\*\*  

&nbsp;  Model outputs are aggregated over time using recency-weighted sentiment trajectories and volatility metrics to characterize \*\*longitudinal affective behavior\*\* at the user level.



---





---



\## Dataset



\- \*\*Sentiment140\*\* (publicly available)

\- Binary sentiment labels:

&nbsp; - `0`: Negative  

&nbsp; - `1`: Positive (mapped from original label `4`)

\- A balanced subset of \*\*500,000 tweets\*\* is used for large-scale experimentation.



⚠️ \*\*Important Note\*\*  

Sentiment140 provides \*\*sentiment polarity only\*\* and does \*\*not contain clinical mental-health annotations\*\*.  

All mental-state interpretations in this work are \*\*behavioral proxies\*\*, not medical diagnoses.



---



\## Classical Baseline



The classical baseline consists of:



\- Embedding layer  

\- Bidirectional LSTM  

\- Additional LSTM compression  

\- Fully connected classifier  



This baseline is trained under identical data splits, preprocessing, and optimization settings as the hybrid model to ensure a \*\*fair comparison\*\*.



---



\## Hybrid Quantum–Classical Model



The hybrid model augments the classical BiLSTM encoder with:



\- A \*\*shallow variational quantum circuit\*\* (5 qubits)

\- Angle encoding and linear entanglement

\- Expectation-value–based feature extraction

\- Classical–quantum feature fusion prior to classification



The quantum component is designed to:

\- Introduce \*\*nonlinear, correlated feature interactions\*\*

\- Maintain \*\*training stability\*\*

\- Remain \*\*simulation-feasible\*\* under current hardware constraints



---



\## Feature-Space Visualization and Separability Analysis



To empirically support the claim of \*\*quantum-enhanced feature representation\*\*, we provide:



\- t-SNE visualizations of:

&nbsp; - Classical BiLSTM feature space

&nbsp; - Hybrid quantum–classical feature space

\- Quantitative separability metrics:

&nbsp; - \*\*Silhouette score\*\* computed on extracted embeddings



These analyses are performed \*\*without retraining\*\*, using frozen models and identical input samples.



---



\## Temporal Behavioral Analysis



Beyond instance-level sentiment prediction, the repository includes:



\- Recency-weighted sentiment trajectories

\- Emotional volatility estimation

\- Drift and trend analysis

\- Case studies of users exhibiting:

&nbsp; - Stabilization

&nbsp; - Volatile behavior

&nbsp; - Positive-to-negative and negative-to-neutral transitions



This component demonstrates how the model outputs can be integrated into \*\*longitudinal monitoring pipelines\*\*, rather than snapshot-based sentiment classification.



---



\## Statistical Evaluation



\- All models are trained across \*\*five independent runs\*\*

\- Performance is reported as \*\*mean ± standard deviation\*\*

\- A paired t-test is used to assess statistical significance

\- Results confirm \*\*comparable performance\*\* rather than statistically significant gains



The contribution of this work is therefore \*\*architectural and computational\*\*, not metric-level superiority.



---



\## Reproducibility



\- Fixed random seeds

\- Identical train/validation/test splits

\- Saved models, tokenizers, and histories

\- No retraining required for:

&nbsp; - Feature-space visualization

&nbsp; - Temporal analysis

&nbsp; - Case-study evaluation



---



\## Ethical and Practical Considerations



This system is intended for:



\- Exploratory analysis

\- Population-level behavioral studies

\- Decision-support workflows with human oversight



It is \*\*not\*\* intended for autonomous diagnosis or clinical decision-making.  

Human-in-the-loop interpretation and clinically grounded datasets are essential for real-world deployment.



---



\## Requirements



Core dependencies include:



\- Python ≥ 3.9  

\- TensorFlow  

\- NumPy / Pandas  

\- Scikit-learn  

\- PennyLane (for quantum simulation)  

\- Matplotlib / Seaborn  



&nbsp;



--- 

---



\## Citation



If you use this code or build upon this work, please cite the corresponding paper.
"Mental health-aware sentiment analysis using a hybrid quantum–classical approach"



---



\## Contact



For questions related to the implementation or experiments, please either open an issue or contact with the corresponding author.



