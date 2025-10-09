# Output Characteristics of BJT (BC547) — LabVIEW & NI USB-6001

This repository contains my **Measurement & Instrumentation (M.Sc.)** project: a LabVIEW system that measures and plots the **output characteristics (IC vs UCE)** of a **BC547** NPN transistor using an **NI USB-6001** DAQ.

## 🚀 Overview
- Plot **IC–UCE** families for several **IB** values to observe **cut-off**, **active**, and **saturation** regions.
- Live numeric indicators for **UB, UBE, IB, UC, UCE, IC** (plus temperature if enabled).
- Helper analog stage (LM324) with gain ≈ **4.03** on the UC path.

## 🧰 Requirements
- LabVIEW 2023+  
- NI-DAQmx  
- NI USB-6001 (or adapt DAQ channels)

## 🔧 How to Run (quick)
1. Wire the circuit per `images/schematic_*`.
2. Open `labview/Transistor_Characteristics_NikhilSanga_Dipto_Group4.vi`.
3. Sweep **UB** (~0.8–1.3 V) and record **IC vs UCE** for each **IB**.
4. View the plotted **IC–UCE** curves on the LabVIEW front panel.

### Key equations
- `IB = (UB − UBE) / RB` with `RB ≈ 2.35 kΩ`
- `IC = (UC − UCE) / RC` with `RC ≈ 0.05 kΩ` (4 × 200 Ω ∥)
- UC gain ≈ `1 + 10k / 3.3k = 4.03`

## 📚 Documentation
See `/report` for complete reports and `/docs` for setup, theory, and results.

## 📎 Citation
Please cite via `CITATION.cff`.

## 📝 License
MIT — see `LICENSE`.

## 📁 Repository Structure
