# **Quantum AI-Based Compiler for Astronomical Image Processing** 🚀🔭

## **Overview**
This repository contains the implementation of a **Quantum AI-Based Compiler** designed to optimize high-speed image processing for astronomical data. The project leverages a hybrid approach combining **Quantum-Inspired Evolutionary Algorithm (QIEA)** and **Particle Swarm Optimization (PSO)** to enhance telescope images, such as those from the **Hubble Space Telescope (HST)**. The initial focus is on **noise reduction**, with plans to expand to **object detection** and **image enhancement**.

---

## **🚨 Problem Statement**
Modern astronomical telescopes, such as the **Hubble Space Telescope (HST)** and upcoming instruments like the **Vera C. Rubin Observatory**, generate vast amounts of image data (**terabytes per night**). Traditional image-processing methods struggle to keep up, delaying scientific discoveries due to slow processing times.

Key challenges:
- Computationally expensive **noise reduction**, **object detection**, and **feature enhancement**.
- Handling raw **FITS files** with high dynamic ranges and noise from cosmic rays or detectors.
- Ensuring faster **real-time image processing** while maintaining high accuracy.

📌 **This project aims to develop a compiler that:**
✅ **Optimizes image-processing parameters** using quantum-inspired AI.
✅ **Accelerates processing** for near-real-time analysis.
✅ **Matches or exceeds the quality** of existing pipelines (e.g., Hubble’s drizzling process).

---

## **🎯 Project Objective**
This project aims to **build a compiler** that uses **QIEA and PSO** to process raw astronomical images (**FITS files**) **faster and with high accuracy**, using processed science images as benchmarks.

🔹 **Primary Goal:** Reduce noise in raw Hubble images by at least **50% in under 5 seconds per image**.
🔹 **Future Scope:** Extend to broader applications like **object detection and image enhancement**.

---

## **📡 Data Source**
The project uses **FITS files** from the **Hubble Legacy Archive (HLA)**, a public repository hosted by the **Space Telescope Science Institute (STScI).**

🔗 **Website:** [Hubble Legacy Archive](https://hla.stsci.edu/)

### **🗂 Sample Data Used**
- **Processed Science Image:** `hst_mos_0017053_acs_wfc_f555w_sci.fits` (Benchmark for output).
- **Raw Data:** Corresponding `_raw.fits` files (To Be Added).

### **📥 How to Access Data:**
1. Visit [HLA](https://hla.stsci.edu/).
2. Search for a target (e.g., `M51` for the Whirlpool Galaxy).
3. Filter by **instrument** (e.g., ACS), **filter** (e.g., `F555W`).
4. Download `_raw.fits` and `_sci/_drz.fits` files.
5. Store them in the `data/` directory.

---

## **🧠 Algorithms Used**
This project employs a **hybrid optimization approach**:

### **1️⃣ Quantum-Inspired Evolutionary Algorithm (QIEA)**
📌 **Purpose:** Explores a wide solution space using quantum-inspired principles (e.g., superposition-like population states) to find **initial parameter sets** for image processing.

🔗 **Source Code:** [rnowotniak/qopt](https://github.com/rnowotniak/qopt)

📌 **Implementation:**
- Uses **Quantum Rotation Gates** for parameter updates.
- Adapts **quantum probability amplitudes** for better search efficiency.
- Written in **Python/Cython** for performance optimization.

### **2️⃣ Particle Swarm Optimization (PSO)**
📌 **Purpose:** Refines **QIEA solutions** by simulating a **swarm of particles** converging on **optimal parameters** (e.g., filter sigma for noise reduction).

🔗 **Library Used:** [pyswarms](https://pyswarms.readthedocs.io/en/latest/)

📌 **Implementation:**
- Swarm-based optimization to fine-tune filter coefficients.
- Applied after QIEA to improve image enhancement parameters.

### **🛠 Hybrid Approach**
🔹 **QIEA** generates initial solutions.
🔹 **PSO** refines them for optimal image processing performance.

---

## **📚 Libraries Used**
| Library    | Purpose  |
|------------|---------|
| `astropy`  | Handling FITS files |
| `numpy`    | Numerical operations |
| `matplotlib` | Visualization of images |
| `scipy`    | Image-processing filters (e.g., Gaussian blur) |
| `pyswarms` | PSO implementation |
| `cython`   | Performance optimization (for QIEA) |

---

![ChatGPT Image Mar 30, 2025, 08_04_53 PM](https://github.com/user-attachments/assets/ce587989-4096-49f2-a185-3467b707a786)


## **💻 Installation & Setup**
```bash
# Clone the repository
git clone https://github.com/your-username/Quantum-AI-Compiler-Astronomy.git
cd Quantum-AI-Compiler-Astronomy

# Install dependencies
pip install -r requirements.txt
```

---

## **🚀 Usage**
Run the main script to process an image:
```bash
python main.py --input_image="data/raw_image.fits" --output="data/enhanced_image.fits"
```

🔹 **Options:**
- `--input_image`: Path to the raw FITS file.
- `--output`: Path to save the processed image.






