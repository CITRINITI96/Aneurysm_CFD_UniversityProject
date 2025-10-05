# 🧠 CFD Analysis of Blood Flow in Simplified Aneurysm Models

### 📄 Project Overview
This project reproduces the computational fluid dynamics (CFD) analysis presented in the paper:

> **Lim Sheh Hong, Mohd Azrul Hisham Mohd Adib, et al.**  
> *Modeling and Simulation of Blood Flow Analysis on Simplified Aneurysm Models*  
> *IOP Conference Series: Materials Science and Engineering, Vol. 917 (2020), 012067.*  
> DOI: [10.1088/1757-899X/917/1/012067](https://doi.org/10.1088/1757-899X/917/1/012067)

The goal is to replicate the hemodynamic behavior of blood flow through simplified aneurysm geometries using CFD.  
The analysis focuses on **Wall Shear Stress (WSS)**, **velocity distribution**, and **pressure fields**, as influenced by geometric variations.

---

## 🧩 Methodology

### 1. Modeling
- 3D aneurysm geometries (Models A, B, and C) were designed in **SolidWorks 2019**, following the dimensions reported in the paper.  
- Each model includes one inlet and one/two outlets, with different aneurysm sizes.

### 2. Meshing
- **Tetrahedral mesh** was generated for each geometry, with refined elements at the aneurysm neck.
- Typical mesh statistics:
  - Model A → 149,342 elements  
  - Model B → 205,778 elements  
  - Model C → 293,344 elements

### 3. CFD Setup
Simulations were performed using **ANSYS Fluent 15.0**.

| Property | Value |
|-----------|-------|
| Fluid Type | Incompressible Newtonian |
| Density (ρ) | 1050 kg/m³ |
| Dynamic Viscosity (μ) | 3.5 × 10⁻³ Pa·s |
| Inlet Velocity | 0.348 m/s (systolic) |
| Outlet Condition | P-fixed (0 Pa) |
| Wall Condition | No-slip, rigid walls |

Governing equations:
- **Navier–Stokes (steady-state)**  
- **Continuity equation**

### 4. Post-Processing
Results obtained:
- Wall Shear Stress (WSS) maps  
- Velocity and pressure contours  
- Velocity field distributions for cutting angles (30°, 45°, 90°)

---

## 📊 Results Summary

| Model | Max WSS (Pa) | WSS Hotspot Location |
|--------|---------------|----------------------|
| A | 28.7 | Artery outlet |
| B | 29.5 | Aneurysm neck |
| C | 15.8 | Parent artery |

🩸 **Observations**
- WSS is lowest at the aneurysm dome and highest at the neck.
- WSS increases with inlet velocity.
- Cutting angle affects local velocity field stability.

---

## 🧠 Discussion

This analysis demonstrates that **aneurysm geometry has a direct impact on local hemodynamics**, particularly on WSS distribution and flow direction.  
Even simplified models can offer valuable insight into **rupture-prone regions**.

**Potential extensions:**
- Non-Newtonian blood model  
- Transient (pulsatile) simulations  
- Patient-specific arterial geometries  
- Polyhedral mesh comparison  

---

## 🧰 Tools and Skills

| Tool | Purpose |
|------|----------|
| Comsol Multiphysics |
| Paraview / Fluent Post | Post-processing visualization |
| Python / MATLAB | Data extraction and plotting (optional) |

---

## 📂 Repository Structure
```
CFD_Aneurysm_Replication/
│
├── models/                 # CAD and meshed geometries
├── paper_reference/        # Original article and notes
└── README.md               # Project documentation
```


## 📚 Reference

> Lim Sheh Hong, Mohd Azrul Hisham Mohd Adib, et al.  
> *Modeling and Simulation of Blood Flow Analysis on Simplified Aneurysm Models*  
> IOP Conference Series: Materials Science and Engineering, 917 (2020), 012067.  
> DOI: [10.1088/1757-899X/917/1/012067](https://doi.org/10.1088/1757-899X/917/1/012067)

If you reuse or extend this project, please cite both the paper and this repository:

```bibtex
@article{lim2020aneurysm,
  title={Modeling and Simulation of Blood Flow Analysis on Simplified Aneurysm Models},
  author={Lim, Sheh Hong and Mohd Adib, Mohd Azrul Hisham and others},
  journal={IOP Conference Series: Materials Science and Engineering},
  volume={917},
  pages={012067},
  year={2020},
  doi={10.1088/1757-899X/917/1/012067}
}
```

---

## 👤 Author

**Salvatore Citriniti**  
*Engineer Biomedical & Informatic*  
📧 [salvatorecitriniti@hotmail.it]  
🔗 [GitHub Profile](https://github.com/yourusername)

---

## 🧾 License
This project is shared for **academic and educational purposes only**.  
The original research paper is © IOP Publishing (CC BY 3.0 license).  
All reproduction work and simulation setup in this repository are my own.
