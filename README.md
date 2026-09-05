# Reinforced Concrete Structural Joint Verification & Stirrup Design Tool

A dedicated structural engineering application for stress verification of beam-column joints under combined shear-tension and shear-compression, along with Eurocode 8 compliant transverse reinforcement design.

---

## 📌 Repository Description (For GitHub Setup)

> **Short Description / Tagline:**
> *A structural engineering tool for stress verification of concrete joints under shear-tension/compression and transverse reinforcement design per Eurocode 8.*

---

## 🚀 Key Features

* **Stress Verification:** Computes principal tensile and compressive stresses within the joint core panel based on user-defined geometry, material strengths, and applied axial/shear forces.
* **Material Limit Checking:** Direct comparison of calculated principal stresses against ultimate concrete tensile and compressive limit states.
* **Eurocode 8 Reinforcement Design:** Evaluates pre-cracking and post-cracking mechanisms according to EC8 formulas to calculate the required minimum transverse reinforcement (stirrups) inside the joint panel.
* **Built-in Examples:** Includes two ready-to-use sample verification files accessible via context menu (right-click anywhere in the interface).

---

## ⚙️ Technical Methodology

### 1. Joint Core Stress State
The principal stresses ($\sigma_1, \sigma_2$) in the joint core are calculated based on the horizontal shear force $V_{jh}$ and normal stresses $\sigma_n$ acting on the joint panel:

$$\sigma_{1,2} = \frac{\sigma_n}{2} \pm \sqrt{\left(\frac{\sigma_n}{2}\right)^2 + \tau^2}$$

where:
* $\tau = \frac{V_{jh}}{b_j \cdot h_{jc}}$ is the nominal shear stress in the joint core.
* $\sigma_n$ is the average axial stress on the column above/within the joint.

### 2. Limit Stress Comparisons
Calculated principal stresses are verified against Eurocode 8 performance limits:
* **Principal Tensile Stress ($\sigma_1$):** Checked against concrete tensile strength $f_{ctd}$.
* **Principal Compressive Stress ($\sigma_2$):** Checked against reduced concrete compressive strength $f_{cd}^* = \eta f_{cd}$.

### 3. Eurocode 8 Transverse Reinforcement (Stirrup Design)
To prevent joint core shear failure after diagonal cracking, the required total area of horizontal stirrups $A_{sh}$ is determined according to Eurocode 8 (EN 1998-1):

$$A_{sh} \cdot f_{yw} \ge \frac{(V_{jh})^2}{b_j \cdot h_{jc} \cdot f_{ctd}} - N_d$$

or via post-cracking strut-and-tie mechanism formulation:

$$A_{sh} = \frac{V_{jh} - \gamma \cdot N_d}{f_{ywd}}$$

---

## 💡 Quick Start

1. **Load Example Files:** Right-click anywhere on the interface to open one of the two pre-loaded example configurations.
2. **Define Joint Geometry:** Enter column and beam dimensions ($b_c, h_c, b_b, h_b$) to establish the effective joint width $b_j$ and depth $h_{jc}$.
3. **Set Material Properties:** Specify concrete compressive strength ($f_{ck}$) and rebar yield strength ($f_{yk}$).
4. **Input Internal Forces:** Enter applied axial force ($N_d$) and horizontal joint shear ($V_{jh}$).
5. **Run Verification & Design:** Review principal stress checks and output the required area and distribution of joint stirrups.

---

## 🏷️ Suggested GitHub Topics

`structural-engineering` `eurocode-8` `concrete-design` `beam-column-joint` `shear-verification` `reinforcement-design` `stirrup-design` `civil-engineering`
