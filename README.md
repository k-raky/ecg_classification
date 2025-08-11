# ecg_classification
Classify heartbeat electrocardiogram (ECG) data from the PhysioNet 2017 Challenge using deep learning and signal processing.

This notebook demonstrates how to detect Atrial Fibrillation (AFib) from Electrocardiogram (ECG) recordings using a Long Short-Term Memory (LSTM) neural network. AFib is a common heart rhythm disorder that produces irregular electrical patterns in the heart, which can be identified from ECG waveforms.


The data from https://physionet.org/content/challenge-2017/1.0.0/ consists of ECG signals stored in .mat files with corresponding labels. Noisy recordings are removed, and abnormal rhythms are grouped under a single category for classification. The signals are first filtered to remove noise, then divided into shorter segments so the model can analyze patterns over time.


The core of the method is an LSTM-based neural network, chosen because it excels at capturing temporal dependencies in sequential data such as ECGs. The LSTM layers process the extracted features in their natural time order, allowing the network to learn patterns that unfold across multiple heartbeats. A final dense layer outputs the probability of AFib versus normal rhythm. The model is trained for 150 epochs using binary cross-entropy loss and optimized with Adam.


<img width="707" height="468" alt="image" src="https://github.com/user-attachments/assets/4b0e4b4c-65b6-4ad3-b2cf-3aeb3b4c4f22" /> 

<img width="583" height="453" alt="image" src="https://github.com/user-attachments/assets/5a59b9bf-14f8-43d6-88d2-302e2e07e8cf" />

<img width="1512" height="822" alt="Capture d’écran 2025-08-11 à 20 03 08" src="https://github.com/user-attachments/assets/c5c7ce89-0ec6-45df-b9d3-42a42e8c23e3" />
