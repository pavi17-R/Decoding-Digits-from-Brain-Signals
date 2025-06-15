
# 🧠 EEG-Based Imagined Digit Recognition using Deep Learning

This repository contains the implementation of a two-stage deep learning framework for recognizing imagined digits from EEG signals recorded using the low-cost Interaxon Muse headset. The objective is to decode spontaneous digit-related thoughts using only four EEG channels and convert them into time–frequency representations for classification using pretrained ResNet models.

---

## 🧪 Abstract

The integration of brain–computer interface (BCI) technologies with deep learning architectures has opened new avenues in cognitive signal decoding and mental state classification. This study presents a digit-based mind reading system using EEG signals from the publicly available MindBigData-Muse dataset, recorded with the Interaxon Muse device.

Unlike previous studies that rely on stimulus-driven tasks and high-resolution EEG systems, this work focuses on decoding spontaneous digit-related thoughts using affordable, non-invasive hardware. A two-stage deep learning model is introduced, where:

- **Stage 1**: ResNet-34 classifies EEG input as *digit* or *non-digit* (Accuracy: **84.92%**)
- **Stage 2**: ResNet-18 identifies the specific digit (0–9) from digit-classified EEG data (Accuracy: **64.00%**)

---

## 🧠 Methodology

1. **Bandpass Filtering**: EEG signals are filtered in the 1–40 Hz frequency range.
2. **Resampling**: EEG samples are resampled to ensure a uniform length.
3. **Scalogram Generation**: Complex Morlet wavelet transforms are used to convert 1D EEG data into 2D time–frequency images.
4. **Model Training**:
   - ResNet-34 for binary classification (digit vs non-digit)
   - ResNet-18 for multi-class classification (digits 0–9)

---

## 📊 Results

| Stage         | Model      | Task                   | Accuracy |
|---------------|------------|------------------------|----------|
| Stage 1       | ResNet-34  | Digit vs Non-Digit     | 84.92%   |
| Stage 2       | ResNet-18  | Digit Identification   | 64.00%   |

---


---

## 💾 Dataset

- **Name**: MindBigData - Muse EEG Dataset  
- **Source**: [http://mindbigdata.com/opendb/](https://mindbigdata.com/opendb/)  
- **Device Used**: Interaxon Muse (4-channel EEG)

---


## 📈 Future Work

- 🔍 **Improving Classification Accuracy**: Explore advanced CNN architectures such as EfficientNet, DenseNet, or hybrid attention models to enhance the system's prediction capabilities.
- 🧠 **Real-time Digit Prediction**: Implement real-time EEG streaming and classification for live mental state decoding.
- 🗣️ **Extended Command Set**: Extend the system to support classification of multiple imagined commands or words beyond just digits (e.g., directional thoughts, simple tasks).



