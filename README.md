# Anomaly detection on multivariate time-series

> List of papers & datasets for anomaly detection on multivariate time-series data.

## 1. Papers
| Name | Code | Key word | Year  | Published |
|------|------|----------|-------|---------|
|  A Deep Neural Network for Unsupervised Anomaly Detection and Diagnosis in Multivariate Time Series Data |  [MSCRED](https://github.com/search?q=MSCRED)|correlations  |     |  AAAI'19   |
|  Graph Neural Network-Based Anomaly Detection in Multivariate Time Series |   [GDN](https://github.com/d-ailin/GDN)|  sensor relationships|     |  AAAI'21     |  
|  Multivariate Time-series Anomaly Detection via Graph Attention Network  |  [MTAD_GAT](https://github.com/mangushev/mtad-gat)|     sensor relationships    |      |   ICDM'20      |
|  USAD : UnSupervised Anomaly Detection on Multivariate Time Series   |   [USAD](https://github.com/manigalati/usad)|      adversarial    |      |   KDD'20    |
|  MAD-GAN: Multivariate Anomaly Detection for Time Series Data with Generative Adversarial Networks    |   [MAD_GAN](https://github.com/LiDan456/MAD-GANs) |          |       |    ICANN'19     |
|   Robust anomaly detection for multivariate time series through stochastic recurrent neural network   |  [OmniAnomaly](https://github.com/NetManAIOps/OmniAnomaly) |          |       |    KDD'19     |
|   Deep Autoencoding Gaussian Mixture Model for Unsupervised Anomaly Detection   |  [DAGMM](https://github.com/danieltan07/dagmm) |          |       | ICLR'18  |
|   TranAD: Deep Transformer Networks for Anomaly Detection in Multivariate Time Series Data   |  [TranAD](https://github.com/imperial-qore/TranAD) |          |       |     VLDB'22  |
|    Anomaly Transformer: Time Series Anomaly Detection with Association Discrepancy  |  [Anomaly Transformer](https://github.com/thuml/Anomaly-Transformer)|          |       |    ICLR'22     |
|  Timeseries Anomaly Detection using Temporal Hierarchical One-Class Network Lifeng    |  THOC(None)|          |       |         |
|   Unsupervised Deep Anomaly Detection for Multi-Sensor Time-Series Signals   |  CAE-M(None)|          |       |    TKDE'21     |
|  Learning Graph Structures with Transformer for Multivariate Time Series Anomaly Detection in IoT    |  [GTA](https://github.com/ZEKAICHEN/GTA/tree/main/data)|          |      |     IoTJ'21    |
|  Multivariate Time Series Anomaly Detection and Interpretation using Hierarchical Inter-Metric and Temporal Embedding    |  [InterFusion](https://github.com/zhhlee/InterFusion)|          |       |   KDD'21      |
|   Detecting spacecraft anomalies using lstms and nonparametric dynamic thresholding   |  [LSTM-NDT](https://github.com/khundman/telemanom)|          |       |    KDD'18    |
|  Time Series Anomaly Detection for Cyber-physical Systems via Neural System Identification and Bayesian Filtering   |  [NSIBF](https://github.com/NSIBF/NSIBF)|          |       |    KDD'21    |
|      |  []()|          |       |        |
|      |  []()|          |       |        |
|      |  []()|          |       |        |
|      |  []()|          |       |        |
|      |  []()|          |       |        |

## 2. Datasets
- **SWaT & WaDI:** [SWaT Dataset Download](https://itrust.sutd.edu.sg/itrust-labs_datasets/), [SWaT Dataset Introduce](https://itrust.sutd.edu.sg/itrust-labs-home/itrust-labs_swat/), [WaDI Dataset Introduce](https://itrust.sutd.edu.sg/itrust-labs-home/itrust-labs_wadi/)  | [**data_preprocess**](https://itrust.sutd.edu.sg/itrust-labs_datasets/)
- **MSL & SMAP:** [Dataset Download and Introduction](https://github.com/khundman/telemanom)  | [**data_preprocess**](https://github.com/qiumiao30/time-series-anomaly-detection/blob/main/preprocess.py#:~:text=dataset%20%3D%3D%20%27-,SMAP,-%27%20or%20dataset)
- **SMD:** [Dataset Download and Introduction](https://github.com/NetManAIOps/OmniAnomaly) | [**data_preprocess**](https://github.com/qiumiao30/time-series-anomaly-detection/blob/main/preprocess.py#:~:text=dataset%20%3D%3D%20%27-,SMD,-%27%3A)
- **ASD:** [Dataset Download and Introduction](https://github.com/zhhlee/InterFusion/tree/main/data)
- **PSM:** [Dataset Download and Introduction](https://github.com/eBay/RANSynCoders/tree/main/data)
- **KDDCup99:** [Dataset Download and Introduction](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)
- **MSDS:** [Dataset Download and Introduction](https://zenodo.org/record/3484801#.Yo7P9e5ByEI)
- **MIT-BIH:** [Dataset Download and Introduction](https://physionet.org/content/svdb/1.0.0/)
- **KDDCup21:** [Dataset Download and Introduction](https://compete.hexagon-ml.com/practice/competition/39/)
- **Wind Turbines:** [Dataset Download and Introduction](https://github.com/zhanjun717/STGAT/tree/main/data/WT)
- **Others:**
  - [Numenta's NAB](https://github.com/numenta/NAB)
  - [Yahoo's Webscope S5---Download Harder](https://webscope.sandbox.yahoo.com/catalog.php?datatype=s&did=70)
  - [2020 Skoltech's SKAB](https://github.com/waico/SkAB)
  - [2018 AIOps's KPI-Anomaly-Detection](https://github.com/NetManAIOps/KPI-Anomaly-Detection)
## 3. Evaluate
### 3.1 Metrics
|     Ground truth    |     Predict      |   Predict      |
|:-----------------:|:-----------------:|:-------------:|
|                 |     Abnormal        |    Normal    |
|     Abnormal        |     TP          |     FN      |
|     Normal        |     FP          |     TN      |
- **Precision:** $P=\frac{TP}{TP+FP}$

- **Recall:** $R=\frac{TP}{TP+FN}$

- **F1:** $F1=\frac{2\times P\times R}{P+R}$

- **AUC:** $\mathrm{TPR}=\frac{TP}{TP+FN}$, $\mathrm{FPR}=\frac{FP}{TN+FP}$

### 3.2 Threshold 
#### 3.2.1 Label-Based Threshold Search
- Best F1
#### 3.2.2 Thresholds Search without labels
- Val_max(Train_max) F1

 $$Max(|groundtruth - predict/reconstruction|)$$
 
- Pot F1
- Epsilon F1

## 4. Point Adjust & Point Adjust %K & Original
- Point Adjust

![point adjust](https://github.com/qiumiao30/time-series-anomaly-detection/blob/main/image/point%20adjust.png)
