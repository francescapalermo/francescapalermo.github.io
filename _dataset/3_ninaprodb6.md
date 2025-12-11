---
title: "NinaPro DB6 Dataset"
collection: datasets
type: "Dataset"
permalink: /dataset/ninaprodb6
excerpt: "A multi-session sEMG dataset designed to evaluate the repeatability of hand movement classification for prosthetic control, featuring data from 10 subjects across 100 acquisitions. DB6 supports research on robustness, cross-session adaptation, and sEMG-based hand gesture recognition."
venue: ""
location: ""
---

The **NinaPro DB6 dataset** is part of the NinaPro initiative, supporting research in **surface electromyography (sEMG)**, motor intention decoding, and prosthetic control.

DB6 focuses on the **repeatability of hand movement classification**. It contains multi-session sEMG recordings collected from **10 subjects** performing a set of functional grasps across multiple days and sessions. This structure allows researchers to explore **inter-session variability**, domain adaptation, and the robustness of machine learning models applied to sEMG signals.

I directly contributed to the acquisition of DB6 (100 total acquisitions), which is openly available to the research community.

### Information

The dataset includes:

- **10 subjects**, each completing multiple daily sessions  
- **7 grasp types**, repeated **12 times**, twice per day, across **5 days**  
- High-quality sEMG recordings suitable for:  
  - Pattern recognition  
  - Repeatability analysis  
  - Domain adaptation  
  - Robust cross-session training  
  - Benchmarking sEMG-based machine learning algorithms  

DB6 documentation and instructions:  
🔗 https://ninapro.hevs.ch/instructions/DB6.html

### Data Structure

- Raw and processed sEMG recordings  
- Labels describing hand movements  
- Session identifiers for longitudinal analysis  
- Metadata for subject and session tracking  

The dataset is suitable for supervised learning, time-series modelling, deep learning, and robustness evaluation of prosthetic control systems.

### Download Links

👉 **Official DB6 dataset:**  
https://ninapro.hevs.ch/instructions/DB6.html

### Info and Queries

For enquiries related to this dataset or associated research, please contact  
**Francesca Palermo** – [palermo.francesca21@gmail.com](mailto:palermo.francesca21@gmail.com)

---

### Acknowledgments

If you use this dataset, please cite the following [paper](https://ieeexplore.ieee.org/abstract/document/8009405), which introduced DB6 and analysed repeatability:

**Palermo, F., Cognolato, M., Gijsberts, A., Müller, H., Caputo, B., Atzori, M.**  
*Repeatability of grasp recognition for robotic hand prosthesis control based on sEMG data.*  
In **2017 International Conference on Rehabilitation Robotics (ICORR)**, pp. 1154–1159. IEEE.