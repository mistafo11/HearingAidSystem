# Enhanced Hearing Aid System for Clear Audio Perception with Deep Neural Networks (DNNs)

## Overview
This project develops a smart hearing aid system that leverages deep neural networks (DNNs) and digital signal processing (DSP) techniques to enhance speech clarity. The system classifies audio into "Wanted" and "Unwanted" categories using YAMNet as a feature extractor, then applies DSP (low-pass filtering and amplification) to suppress noise and enhance desired speech. It is deployed on a Raspberry Pi 3 Model B+ for real-time processing.

## Features
- **Real-Time Audio Classification:** Utilizes YAMNet to distinguish between "Wanted" and "Unwanted" audio.
- **DSP-Based Enhancement:** Applies a low-pass filter (400 Hz cutoff) and amplification (gain 1.2) for noise reduction and speech enhancement.
- **Edge Deployment:** Designed to run efficiently on a Raspberry Pi 3, demonstrating low-latency, real-time performance.
- **Scalable Dataset:** Trained and evaluated using the Microsoft Scalable Noisy Speech Dataset (MS-SNSD).

## Project Structure
- **data/:** Instructions or scripts for downloading/preprocessing the MS-SNSD dataset.
- **src/:** Contains source code including: <br>
    train.py: Model training script. <br>
    inference.py: Inference and testing script. <br>
    dsp.py: DSP functions (filtering and amplification). <br>
    model.py: Model architecture and transfer learning integration. <br>
    main.py: Main script for real-time deployment on Raspberry Pi. <br>
- **docs/:** Documentation, including the thesis and poster files. 
- **models/:** Saved models and TensorFlow Lite converted models.

## Results & Evaluation
- **Model Performance:** <br>
The fine-tuned model achieved high classification accuracy with training and validation accuracy exceeding 96%. Training and validation loss graphs illustrate the model's learning progress. <br>
- **DSP Effectiveness:** <br>
Waveform and spectrogram comparisons show that the low-pass filter effectively reduces noise while amplification enhances speech clarity.<br>
- **System Processing:** <br>
The integrated system processes 0.4-second audio chunks in real time on a Raspberry Pi, though minor processing delays were observed in complex audio scenarios. <br>

## Commercialization Potential & Future Work 
This system has potential as a component in commercial hearing aids and assistive listening devices. Future work will explore adaptive DSP techniques, further optimizations for real-time performance, and the use of lighter DNN architectures or TensorFlow Micro for more constrained devices. 

## License
This project is licensed under the MIT License – see the LICENSE file for details.

## Acknowledgements
Supervisor: Prof. Goh Chin Hock, Prof. Madya Ir. Dr. <br>
Dataset: Microsoft Scalable Noisy Speech Dataset (MS-SNSD) which can be found here https://github.com/microsoft/MS-SNSD <br>
Special thanks to all contributors and open-source communities whose tools and frameworks made this project possible. <br>
