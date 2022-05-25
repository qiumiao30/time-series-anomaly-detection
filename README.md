# Anomaly detection on multivariate time-series

> List of papers & datasets for anomaly detection on multivariate time-series data.

## 1. Papers
|   | Name | Code | Key word | Year  | Published |
|---|------|------|----------|-------|---------|
|   |  A Deep Neural Network for Unsupervised Anomaly Detection and Diagnosis in Multivariate Time Series Data |  [MSCRED](https://github.com/search?q=MSCRED)|correlations， R  |   2019  |  AAAI   |
|   |  Graph Neural Network-Based Anomaly Detection in Multivariate Time Series |   [GDN](https://github.com/d-ailin/GDN)|  sensor relationships, P |  2021   |  AAAI     |  
|   |  Multivariate Time-series Anomaly Detection via Graph Attention Network  |  [MTAD_GAT]()|     sensor relationships    |    2020   |   ICDM      |
|   |  USAD : UnSupervised Anomaly Detection on Multivariate Time Series   |   [USAD](https://github.com/manigalati/usad)|      adversarial, R    |   2020    |   2020      |
|   |      |   [MAD_GAN]() |          |       |         |
|   |      |  [OmniAnomaly]() |          |       |         |
|   |      |  [DAGMM]() |          |       |         |
|   |      |  [TKDE]() |          |       |         |
|   |      |  [Anomaly Transformer]()|          |       |         |
|   |      |  [THOC]()|          |       |         |
|   |      |  [DAGMM]()|          |       |         |
|   |      |  [DAGMM]()|          |       |         |
|   |      |  [DAGMM]()|          |       |         |

## 2. Datasets
- **SWaT & WaDI:** [SWaT Dataset Download](https://itrust.sutd.edu.sg/itrust-labs_datasets/), [SWaT Dataset Introduce](https://itrust.sutd.edu.sg/itrust-labs-home/itrust-labs_swat/), [WaDI Dataset Introduce](https://itrust.sutd.edu.sg/itrust-labs-home/itrust-labs_wadi/)
- **MSL & SMAP:** [Dataset Download and Introduction](https://github.com/khundman/telemanom)
- **SMD:** [Dataset Download and Introduction](https://github.com/NetManAIOps/OmniAnomaly)
- **ASD:** [Dataset Download and Introduction](https://github.com/zhhlee/InterFusion/tree/main/data)
- **PSM:** [Dataset Download and Introduction](https://github.com/eBay/RANSynCoders/tree/main/data)
- **Wind Turbines:** [Dataset Download and Introduction](https://github.com/zhanjun717/STGAT/tree/main/data/WT)
- **Others:**
  - [Numenta's NAB](https://github.com/numenta/NAB)
  - [Yahoo's Webscope S5---Download Harder](https://webscope.sandbox.yahoo.com/catalog.php?datatype=s&did=70)
  - [2020 Skoltech's SKAB](https://github.com/waico/SkAB)
  - [2018 AIOps's KPI-Anomaly-Detection](https://github.com/NetManAIOps/KPI-Anomaly-Detection)
## 3. Evaluate
### 3.1 Metrics
|     Ground truth    |     Predict      |           |
|:-----------------:|:-----------------:|:-------------:|
|                 |     Abnormal        |    Normal    |
|     Abnormal        |     TP          |     FN      |
|     Normal        |     FP          |     TN      |
- Precision

 $P=\frac{TP}{TP+FP}$
 
- Recall
- F1
- AUC
### 3.2 
#### 3.2.1 Label-Based Threshold Search
- Best F1
#### 3.2.2 Thresholds Search without labels
- Val_max(Train_max) F1
- Pot F1
- Epsilon F1

## 4. Point Adjust & Point Adjust %K & Original
- Point Adjust

![point adjust](https://github.com/qiumiao30/time-series-anomaly-detection/blob/main/image/point%20adjust.png)
