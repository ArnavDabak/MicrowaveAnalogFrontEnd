
# FET Model Characterization

This repository contains simulation and analysis results of a Field Effect Transistor (FET), including IV characteristics, DC operating point, S-parameter simulation, frequency response, and stability analysis.

---

## 📁 Contents

- [`Task 1`](#task-1-fet-model-characterization)
  - IV Characteristics
  - DC Operating Point & Transconductance
- [`Task 1.2`](#task-12-s-parameter-simulation)
  - Transit Frequency (ft)
  - Maximum Frequency (fmax)
  - Stability Analysis

---

## Task 1: FET Model Characterization

### 📈 IV Characteristics

- A DC sweep simulation was performed.
- From the resulting \( I_D \) vs \( V_{DS} \) plot, the transistor enters **saturation** for \( V_{DS} > 1\text{V} \).

### ⚙️ DC Operating Point

- The operating point was selected such that:
  - The transistor is in **saturation**.
  - The **transconductance (\( g_m \))** is **maximized**.
  - \( V_{GS} \) is reasonably low.

#### ➕ Transconductance Calculation

- Equation used:  
  \[
  g_m = \frac{d(I_{DS})}{d(V_{GS})}
  \]

- From the plot of \( g_m \) vs \( V_{GS} \), the **maximum transconductance** is observed at:
  - \( V_{GS} = -2.150\text{V} \)
  - \( V_{DS} = 1\text{V} \)

---

## Task 1.2: S-Parameter Simulation

### 🔧 Bias Conditions

- \( V_{GS} = -2.2\text{V} \)
- \( V_{DS} = 1.5\text{V} \)

### 🚀 Transit Frequency (\( f_T \))

#### ➤ What is \( f_T \)?
The maximum frequency at which the transistor can switch and amplify a signal.

#### Approach 1:
- Used `stoh()` function.
- The forward gain does not drop to 1 within the frequency sweep range.

#### Approach 2:
- Approximate \( h_{21} \approx S_{21} \).
- Determine \( f_T \) at the frequency where \( S_{21} = 0\text{ dB} \).

### ⚡ Maximum Frequency (\( f_{max} \))

#### ➤ What is \( f_{max} \)?
The frequency at which the **Maximum Available Gain (MAG)** drops to **0 dB**.

- A simulation block was added to calculate MAG.
- **Result**:  
  \[
  f_{max} = 121\text{GHz}
  \]

---

### 🔒 Stability Analysis

#### Stability Conditions:
- \( K > 1 \)
- \( |\Delta| < 1 \)

#### Steps:
- Added equations for:
  - **Stability factor \( K \)**
  - **Delta (\( \Delta \))**
- Plotted results confirm:
  - ✅ The device is **unconditionally stable**

---

## 📌 Summary

This project characterizes a FET device using both DC and high-frequency simulations. It determines operating points for optimal transconductance, evaluates frequency limits, and ensures device stability under selected bias conditions.

---

## 🧪 Tools Used

- Circuit simulation software (e.g., ADS / Cadence / LTspice)
- S-parameter and AC analysis blocks
- Custom calculation blocks for \( g_m \), \( f_T \), \( f_{max} \), and stability

---

## 📁 Repository Structure (Suggested)

```
📦FET-Characterization
 ┣ 📜README.md
 ┣ 📁docs
 ┃ ┗ 📄Task 1.docx
 ┣ 📁plots
 ┃ ┣ 📊 IV_Characteristics.png
 ┃ ┣ 📊 gm_vs_Vgs.png
 ┃ ┣ 📊 S21_vs_freq.png
 ┃ ┣ 📊 MAG_vs_freq.png
 ┃ ┗ 📊 Stability_Plots.png
 ┗ 📁simulations
    ┣ 📄 DC_Operating_Point.sim
    ┣ 📄 S_Param.sim
    ┗ 📄 Stability_Analysis.sim
```
