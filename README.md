# 🦿 CNN-Based Estimation of Lower-Limb Gait Biomechanics

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-PyTorch-orange)
![Biomechanics](https://img.shields.io/badge/Biomechanics-IMU-blueviolet)
![Musculoskeletal Simulation](https://img.shields.io/badge/OpenSim-Musculoskeletal%20Modeling-red)
![Physics-Informed Learning](https://img.shields.io/badge/Physics--Informed-Learning-blue)
![FAU](https://img.shields.io/badge/FAU-MLMA%20Seminar-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 🚀 Description
This project was developed as part of the **Machine Learning in Movement Analysis (MLMA)** seminar at Friedrich-Alexander-Universität Erlangen-Nürnberg (FAU).

The objective is to estimate **sagittal-plane lower-limb biomechanics** — including **joint angles, joint moments, and ground reaction forces (GRFs)** — from wearable **inertial measurement unit (IMU)** data using **Convolutional Neural Networks (CNNs)**.

To overcome the **small-dataset problem in biomechanics**, the project combines **measured IMU data** with **physics-based musculoskeletal simulated data** to improve model generalization.

**Supervisor**: Prof. Anne Koelewijn, BioMAC – Biomechanical Motion Analysis and Creation Group, FAU.

---

## 📖 Academic Context

This project is based on the paper:

**Dorschky et al. (2020)**  
*CNN-Based Estimation of Sagittal Plane Walking and Running Biomechanics From Measured and Simulated Inertial Sensor Data*  
Frontiers in Bioengineering and Biotechnology  
DOI: https://doi.org/10.3389/fbioe.2020.00604

### 🎓 Project Components
This repository includes:

- 📊 **Seminar Presentation**  
  A structured presentation summarizing the paper and proposing an extension to the original methodology.

- 🧠 **Project Proposal**  
  A proposed improvement investigating the effect of simulated data scaling and CNN architecture variations.

- 📄 **Implementation Report**  
  A full academic report describing:
  - CNN architecture and implementation
  - Data preprocessing pipeline
  - Training and evaluation procedures
  - Comparison between real-only and real + simulated training
  - Discussion of limitations and future work

---

## 🌟 Key Features
- **Physics-informed Data Augmentation**  
  Integration of musculoskeletal simulation data to address limited experimental datasets.

- **Deep Learning Architecture**
  - 2D Convolutional Neural Networks
  - Separate models for 8 biomechanical outputs
  - Temporal–sensor feature extraction

- **Biomechanical Outputs**
  - Hip, Knee, Ankle Angles
  - Hip, Knee, Ankle Joint Moments
  - Anterior–Posterior GRF
  - Vertical GRF

- **Model Evaluation**
  - RMSE comparison
  - Generalization analysis
  - Simulation scale impact study

---

## 🤔 Why This Project?
Biomechanical variables such as joint moments and muscle-related forces are difficult to measure directly outside laboratory environments.

This project demonstrates how **physics-based simulation and deep learning** can be combined to:

- Reduce dependence on expensive motion capture systems
- Improve wearable-based biomechanics estimation
- Enable real-world movement analysis applications

It provides hands-on experience in **biomechanics, deep learning, and physics-informed modeling**, making it highly relevant for research and applied AI in healthcare and human movement science.

---

## ⚙️ Technologies Used
- **Python**
- **PyTorch**
- `NumPy`
- `Pandas`
- `Matplotlib`
- `Scikit-learn`
- **OpenSim musculoskeletal models**
- Physics-based biomechanical simulation framework

---

## 📁 Repository Structure
```bash

|-- data and models             # The IK models and data
|-- report/                     # Final academic project report
|   |-- MLMA_Project_Report.pdf
|
|-- presentation/               # Seminar presentation
|   |-- MLMA_Presentation.pdf
|
|-- code/                       # Implementation files
|   |-- imu_dataset_subject01.csv
|   |-- imu_dataset_subject01_lag.csv
|   |-- MLMA_project.ipynb
|   |-- trained_model_ridge.pkl
|
|-- results/                    # Plots and evaluation metrics
|
|-- README.md
```


---

## 🧪 OpenSim + CNN Workflow

The project integrates **physics-based musculoskeletal simulation** with deep learning:

1. 📡 Collect real IMU, motion capture, and force plate data  
2. 🦴 Generate simulated kinematics and kinetics using **OpenSim musculoskeletal models**  
3. 🔄 Create virtual IMU signals from simulated movements  
4. 🧠 Train 2D CNN models using:
   - Real-only data  
   - Real + simulated augmented data  
5. 📊 Evaluate performance using RMSE across biomechanical variables  

This hybrid pipeline combines **biomechanical modeling** and **data-driven learning** to enhance generalization.

---

## 📊 Results & Insights

- Significant improvement in **joint angle estimation** when combining simulated data.
- Moderate improvements in **joint moment estimation**.
- Performance degradation observed when excessive simulated data was used (**overfitting risk**).
- Demonstrated the importance of balancing **physics-based augmentation** with measured data.

---

## 🙏 Acknowledgment

I would like to sincerely thank **Prof. Dr. Anne Koelewijn** for her guidance, support, and valuable feedback throughout the MLMA seminar, both for the presentation and the implementation report.

Her assistance was essential to the successful completion of this project.

---

## 🌍 Final Thoughts

This project bridges **biomechanics, physics-based modeling, and deep learning**, showcasing how simulation-enhanced training can improve wearable motion analysis systems.

It highlights the potential of:
- Physics-informed neural networks  
- Simulation-based data augmentation  
- Real-world wearable biomechanics estimation  
- Research applications in rehabilitation and assistive technologies  
