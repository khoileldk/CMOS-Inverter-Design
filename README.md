# CMOS-Inverter-Design
CMOS inverter design from schematic to layout with DRC/LVS verification and post-layout analysis.

## 📌 Overview

This project implements a **CMOS Inverter** from schematic to layout, including verification steps:

* Schematic design
* Pre-layout simulation
* Layout design
* DRC / LVS verification
* Post-layout extraction (LPE)

---

## 🎯 Objectives

* Design a functional CMOS inverter
* Balance rise time and fall time
* Verify correctness using DRC and LVS
* Analyze parasitic effects after layout

---

## 🧠 Theory

A CMOS inverter consists of:

* PMOS (pull-up network)
* NMOS (pull-down network)

To balance switching characteristics:

* $$ W_p \approx 2 \sim 3 \times W_n $$
  (due to lower mobility of holes)

---

## 🔌 Schematic Design

![schematic](images/schematic.png)

**Parameters:**

* NMOS: W = ..., L = ...
* PMOS: W = ..., L = ...

---

## 📊 Pre-Layout Simulation

![waveform](images/prelayout_waveform.png)

**Measured:**

* Propagation delay: ...
* Rise time: ...
* Fall time: ...

**Observation:**

* Output is inverted correctly
* Rise/Fall time (balanced / unbalanced)

---

## 🧱 Layout Design

![layout](images/layout.png)

**Notes:**

* PMOS placed in N-well
* NMOS placed in P-substrate
* Shared diffusion used to reduce area
* Routing optimized to reduce parasitic capacitance

---

## ✅ Verification

### DRC (Design Rule Check)

✔ Passed

![drc](images/drc.png)

---

### LVS (Layout vs Schematic)

✔ Matched

![lvs](images/lvs.png)

---

## ⚡ Post-Layout Simulation (LPE)

![postlayout](images/postlayout_waveform.png)

**Comparison:**

| Metric    | Pre-layout | Post-layout |
| --------- | ---------- | ----------- |
| Delay     | ...        | ...         |
| Rise time | ...        | ...         |
| Fall time | ...        | ...         |

**Observation:**

* Delay increased due to parasitic capacitance
* Signal degraded slightly

---

## 📂 Project Structure

```
Lab01_Inverter_Design/
├── schematic/
├── layout/
├── simulation/
├── drc_lvs/
├── images/
└── README.md
```

---

## 🛠 Tools Used

* Cadence Virtuoso / Custom Designer
* LTspice (if used)
* PDK: ...

---

## 📌 Key Learnings

* Understanding CMOS operation
* Layout affects performance significantly
* Importance of DRC/LVS in IC design flow
* Parasitic extraction impact on timing

---

## 🚀 Future Improvements

* Optimize layout for lower delay
* Try different Wp/Wn ratios
* Compare with transmission gate inverter
