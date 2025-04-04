# Machine Learning-Based Attack Detection for Electric Vehicle Charging Infrastructure Security

## **Contributors**
- Kevin Nguyen (@KonKrazy)  
  General Engineering, College of Engineering, Texas A&M University
  Email: kevin.nguyen@tamu.edu

- Brady Nguyen (@jhoang3)  
  Computer Science, College of Engineering, Texas A&M University
  Email: bn6687@tamu.edu

## **Introduction**
The increasing reliance on Electric Vehicle Supply Equipment (EVSE) for electric vehicle charging has made these systems a critical infrastructure component, yet vulnerable to a variety of cyberattacks. This project aims to identify network and host-based attack scenarios on EV chargers from three distinct perspectives: network traffic, host events, and power consumption.  

The EV charging systems are susceptible to threats like Reconnaissance and Denial-of-Service attacks from the network side, as well as host-based threats, including backdoor vulnerabilities and cryptojacking. As the adoption of electric vehicles grows, securing EVSE from these attacks is imperative to ensure both the stability of the charging infrastructure and the broader network. This proposal briefly outlines the experiments, methods, and datasets to evaluate the effectiveness of machine learning for the security of EV charging stations.

## **Dataset Description**
The CIC EV Charger Attack Dataset 2024 (CICEVSE2024)[1] serves as the primary dataset for this project. It offers a comprehensive view of both benign and attack scenarios involving EV chargers. This dataset captures key metrics such as power consumption, network traffic, and host-based events like Hardware Performance Counter (HPC) and Kernel Events. The structure of the dataset consists of three main subdirectories:

- **Network Traffic**, which includes pcap files and extracted CSV files for two types of chargers, EVSE-A and EVSE-B.  
- **Host Events**, which contain CSV files detailing HPC and Kernel Events for EVSE-B under both normal and attack conditions.  
- **Power Consumption**, which includes data showing power consumption patterns for EVSE-B in both benign and compromised environments.  

This dataset is essential for tasks such as behavioural profiling, anomaly detection, and system performance analysis. It supports both statistical and machine learning-based analysis and is a vital resource for identifying security vulnerabilities in EVSE systems.

## **Methodologies**
To analyze the data and build an anomaly detection system, we plan to implement a transformer model[3] for multiclass classification tasks. Unlike traditional Recurrent Neural Networks (RNNs)[4], transformers use an attention mechanism that enables them to process long-term dependencies more efficiently. This makes transformers particularly well-suited for large temporal datasets like the ones found in the EVSE 2024 dataset. The project will also include comparisons with baseline models like RNNs to evaluate performance differences across various metrics.

## **Experiment Design and Analysis**
In the experimental phase, the focus will be on evaluating the model’s prediction accuracy, precision, and F-score. The following experiments are planned:

- **Experiment 1: Comparison of Prediction Accuracy**  
  *Objective:* Compare the classification accuracy of the transformer model against a baseline RNN model.  
  In this experiment, we aim to detect anomalies in a mixed dataset containing both normal and abnormal traffic. This will help assess the model's generalization ability across different traffic patterns.

- **Experiment 2: Performance on Skewed Datasets**  
  *Objective:* Evaluate the model’s ability to detect anomalies when only a small portion of the data contains attack scenarios, as is common in real-world settings, and how well the model performs in detecting outliers in a skewed dataset.

## **Timeline**
The project will be executed in the following phases:

- **Literature Survey:** Oct.7 - Oct.13  
- **Data Cleaning and Preprocessing:** Oct.14 - Oct.21  
- **Model Training and Tuning:** Oct. 22 - Nov.3  
- **Experiments, Analysis, and Report Writing:** Nov.3 - Nov.24

## **References**
1. "ML Network Attack Detection." *GitHub*, 2023, [https://github.com/CrashedBboy/ML-NetworkAttack-Detection/blob/main/README.md](https://github.com/CrashedBboy/ML-NetworkAttack-Detection/blob/main/README.md).

2. ChatGPT. "Personal Assistant and AI Model." *OpenAI*, 2025.

3. Wang, Haomin, et al. "DDosTC: A Transformer-Based Network Attack Detection Hybrid Mechanism in SDN." *ResearchSquare*, 2024, [https://assets-eu.researchsquare.com/files/rs-4046330/v1_covered_373111ae-352a-4ce6-8092-55218a3588d2.pdf?c=1710133419](https://assets-eu.researchsquare.com/files/rs-4046330/v1_covered_373111ae-352a
