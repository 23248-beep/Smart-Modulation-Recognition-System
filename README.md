# Smart-Modulation-Recognition-System
📡 Smart Modulation Recognition System (OTFS-Based)
🚀 Overview

This project presents a deep learning-based modulation classification system designed for OTFS (Orthogonal Time Frequency Space) signals. The model leverages a dual-stream CNN architecture to accurately identify multiple digital modulation schemes under varying noise conditions.

The system is built to simulate real-world wireless environments and improve robustness in low SNR scenarios, making it relevant for 5G/6G communication systems.

🎯 Key Features

🧠 Dual-stream CNN architecture for feature extraction and classification

📊 Supports classification of 6 modulation schemes:
BPSK, QPSK, 8-PSK
16-QAM, 32-QAM, 64-QAM
📡 Works on OTFS delay-Doppler domain signals
🔊 Robust to noise (AWGN + phase noise)
⚡ Fast convergence within < 40 epochs

📈 Performance Highlights
✅ 81.7% accuracy at SNR = 20 dB
📉 Handles wide SNR range: –5 dB to 25 dB
🔍 Extracted 128-point delay-Doppler features
📊 Improved accuracy by ~11% over time-domain baseline
🧪 Trained on 50,000+ synthetic signal samples

🏗️ System Architecture
Dual-Stream CNN:
Stream 1: Extracts spatial features from delay-Doppler representation
Stream 2: Captures complementary signal characteristics

🔗 Feature fusion layer combines both streams

🎯 Final dense layers perform classification

📊 Dataset Generation
Generated 50,000+ M-QAM samples
Channel impairments included:
Additive White Gaussian Noise (AWGN)
Phase noise
Configurable SNR range: –5 dB to 25 dB
Signals mapped to delay-Doppler domain

🧪 Training Details
Loss Function: Cross-Entropy
Optimizer: (e.g., Adam — update if needed)
Evaluation Metrics:
Accuracy
Confusion Matrix
Mean Squared Error (MSE)

📉 Results & Evaluation
Strong classification performance across modulation schemes
Confusion matrix shows clear separation at higher SNR
Stable training with fast convergence

🛠️ Tech Stack
Python
TensorFlow / Keras
NumPy, Matplotlib
Signal Processing (OTFS framework)

📂 Project Structure
├── data/                # Generated dataset
├── models/              # CNN architecture
├── training/            # Training scripts
├── evaluation/          # Metrics & plots
├── utils/               # Signal generation functions
└── README.md

🔮 Future Improvements
Extend to real-world RF datasets
Integrate transformer-based architectures
Improve performance in ultra-low SNR (< -10 dB)
Deploy on SDR hardware for real-time testing

📌 Applications
Cognitive Radio
5G/6G Wireless Systems
Spectrum Monitoring
Military Communication Systems
