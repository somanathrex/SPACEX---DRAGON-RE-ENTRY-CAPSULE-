# Atmospheric Re-Entry Capsule — Aerodynamic & CFD Analysis

## 📌 Project Overview

This project presents the **CAD design and computational fluid dynamics (CFD) analysis of an atmospheric re-entry capsule** developed to investigate the aerodynamic behaviour of a blunt-body spacecraft during high-speed atmospheric re-entry.

The project focuses on the interaction between the re-entry vehicle and the surrounding atmosphere at high Mach numbers. A representative capsule geometry was developed in **SolidWorks** and subsequently analysed using **ANSYS Fluent** to study the resulting compressible flow field.

The CFD investigation focuses on the formation of the **bow shock**, pressure distribution over the capsule surface, velocity and Mach-number variations, temperature distribution, wake development, and aerodynamic forces generated during re-entry.

The overall workflow combines:

**Conceptual Design → CAD Modelling → Computational Domain → Meshing → CFD Setup → Hypersonic Flow Simulation → Post-Processing → Aerodynamic Analysis**

---

# 🎯 Objectives

The primary objectives of this project are:

* To develop a representative **atmospheric re-entry capsule geometry**.
* To create a computational domain suitable for high-speed external aerodynamics.
* To generate an appropriate CFD mesh around the capsule.
* To simulate compressible atmospheric flow around the re-entry vehicle.
* To investigate **shock-wave formation and propagation**.
* To analyse surface pressure distribution over the capsule.
* To study velocity and Mach-number variations around the vehicle.
* To investigate temperature variations within the flow field.
* To evaluate the aerodynamic forces acting on the capsule.
* To understand the influence of a **blunt-body configuration** on re-entry aerodynamics.
* To establish a CFD workflow that can be extended to more advanced re-entry vehicle studies.

---

# 🚀 Re-Entry Vehicle Concept

Atmospheric re-entry vehicles encounter extremely high aerodynamic loads as they transition from space into the atmosphere.

The capsule uses a **blunt-body configuration**, which is commonly associated with atmospheric re-entry vehicles because it produces a strong detached bow shock ahead of the vehicle.

The shock wave causes a significant increase in pressure and temperature in the flow immediately ahead of the capsule. This creates the characteristic high-temperature and high-pressure environment associated with atmospheric re-entry.

The simulation therefore focuses on understanding the interaction between:

**Freestream Flow → Bow Shock → Stagnation Region → Capsule Surface → Separated/Wake Flow**

---

# 🧩 CAD Modelling

The re-entry capsule geometry was developed using **SolidWorks**.

The CAD model was prepared with CFD considerations in mind, including:

* Smooth external aerodynamic surfaces
* Blunt nose configuration
* Defined capsule forebody
* Controlled geometric transitions
* Simplified geometry suitable for CFD
* Fluid-domain compatibility
* Clean surfaces for meshing

The final geometry was imported into the ANSYS environment for computational-domain creation and meshing.

---

# 🌐 Computational Domain

An external flow domain was created around the capsule to represent the surrounding atmosphere.

The computational domain consists of:

* Freestream/inlet region
* Capsule wall
* Downstream outlet region
* Far-field boundaries
* Fluid volume surrounding the vehicle

The domain was designed to provide sufficient distance between the capsule and the outer boundaries so that the boundaries do not unnecessarily interfere with the shock structure and wake development.

---

# 🔲 Mesh Generation

The computational domain was discretized into finite-volume cells using **ANSYS Meshing**.

Particular attention was given to the regions where large flow gradients were expected.

### Important regions for mesh refinement

* Capsule nose
* Stagnation region
* Bow-shock region
* Capsule surface
* High-pressure-gradient regions
* Wake region
* Boundary-layer region

A finer mesh is particularly important around the nose because the flow experiences strong gradients in:

**Pressure + Temperature + Density + Velocity**

across the shock and stagnation region.

---

# ⚙️ CFD Setup

The aerodynamic analysis was performed using **ANSYS Fluent**.

The simulation was configured as a high-speed compressible external-flow problem.

### Solver Considerations

* Solver: **ANSYS Fluent**
* Flow: Compressible external aerodynamics
* Regime: Supersonic/Hypersonic
* Gas model: Air
* Density: Compressible
* Energy equation: Enabled
* Turbulence modelling: Applied according to the simulation case
* Steady-state approach: Used for the aerodynamic analysis

The CFD setup was selected to capture the strong density, pressure, and temperature variations associated with high-speed atmospheric flow.

---

# 🌬️ Boundary Conditions

The external flow was defined using atmospheric freestream conditions corresponding to the selected re-entry flight condition.

The major boundary conditions included:

### Freestream / Inlet

The freestream boundary defines the atmospheric conditions approaching the capsule.

Parameters include:

* Freestream velocity
* Mach number
* Static temperature
* Static pressure
* Air density
* Flow direction

### Capsule Surface

The capsule surface was defined as a:

**No-Slip Wall**

This allows the simulation to resolve the interaction between the atmospheric flow and the vehicle surface.

### Outlet / Far-Field

The downstream and external boundaries were defined to allow the disturbed flow to leave the computational domain without creating significant artificial reflections.

---

# 💨 Hypersonic Flow Physics

One of the most important features observed during the simulation is the formation of a **detached bow shock** ahead of the capsule.

Because the vehicle has a blunt leading surface, the incoming high-speed flow cannot turn around the body without first being strongly compressed.

This produces a shock structure in front of the capsule.

The flow undergoes significant changes across the shock:

| Parameter   | Upstream | Behind Shock |
| ----------- | -------- | ------------ |
| Velocity    | High     | Reduced      |
| Mach Number | High     | Reduced      |
| Pressure    | Low      | Increased    |
| Temperature | Lower    | Increased    |
| Density     | Lower    | Increased    |

The strongest thermal and pressure effects occur near the **stagnation region** at the front of the capsule.

---

# 📊 CFD Results

The simulation results were post-processed to investigate the aerodynamic flow field around the capsule.

## 1. Mach Number Distribution

The Mach-number contour provides an overview of the flow acceleration and deceleration around the vehicle.

Important features include:

* High-Mach freestream region
* Detached bow shock
* Rapid Mach-number reduction across the shock
* Low-velocity/stagnation region
* Flow expansion around the capsule
* Wake-region development

---

## 2. Pressure Distribution

The pressure contour demonstrates the strong compression of the flow at the front of the vehicle.

The highest pressure occurs near the **stagnation region**, where the incoming flow is brought to very low velocity.

Pressure progressively decreases as the flow moves away from the stagnation point and around the capsule.

The surface-pressure distribution is particularly important for determining the **pressure drag** acting on the vehicle.

---

## 3. Temperature Distribution

The temperature field provides insight into the severe thermal environment generated during atmospheric re-entry.

The flow temperature increases significantly across the bow shock due to the conversion of kinetic energy into internal energy.

The highest temperatures are expected near the shock and stagnation regions.

This makes the nose region particularly important when considering:

* Thermal protection systems
* Ablative materials
* Heat shields
* Structural thermal limits

---

## 4. Velocity Distribution

The velocity contour illustrates the deceleration of the atmospheric flow as it interacts with the capsule.

The major velocity regions include:

**High-Speed Freestream → Shock Deceleration → Stagnation → Surface Flow → Wake**

The wake behind the capsule contains a region of disturbed and lower-speed flow.

---

## 5. Shock-Wave Structure

The bow shock is one of the most significant flow structures observed in the simulation.

The shock separates the relatively undisturbed freestream from the highly compressed flow surrounding the vehicle.

The shock location and strength are influenced by:

* Mach number
* Capsule geometry
* Nose radius
* Atmospheric properties
* Angle of attack
* Flow conditions

---

# 🛰️ Aerodynamic Characteristics

The simulation can be used to evaluate the aerodynamic behaviour of the capsule through parameters such as:

### Drag

The blunt-body configuration generates significant pressure drag because of the large pressure difference between the forward and aft regions of the vehicle.

### Lift

For a symmetric capsule at zero angle of attack, the lift contribution is expected to be comparatively small.

At non-zero angle of attack, the pressure distribution becomes asymmetric and can generate aerodynamic lift.

### Pressure Drag

Pressure drag is strongly influenced by:

* Forebody pressure
* Base pressure
* Shock structure
* Flow separation
* Wake characteristics

---

# 🔥 Thermal Environment

Although the primary focus of the project is CFD-based aerodynamic analysis, the simulation also provides information about the thermal environment around the vehicle.

During atmospheric re-entry, the vehicle's kinetic energy is converted into thermal energy through aerodynamic compression.

The most critical regions are generally:

* Nose/stagnation point
* Bow-shock region
* Leading surfaces
* High-curvature regions

The CFD temperature field can therefore provide an initial understanding of the locations that would require greater thermal protection.

---

# 📈 Post-Processing

The following CFD quantities were investigated using ANSYS Fluent post-processing:

* Mach number
* Static pressure
* Static temperature
* Velocity magnitude
* Density
* Wall pressure
* Surface temperature
* Aerodynamic forces
* Flow-field contours
* Shock structure
* Wake behaviour

The results were visualized using contour plots, vectors, streamlines, and surface distributions.

---

# 🛠️ Software & Tools

| Tool                                  | Application                         |
| ------------------------------------- | ----------------------------------- |
| **SolidWorks**                        | Capsule CAD modelling               |
| **ANSYS SpaceClaim/DesignModeler**    | Geometry preparation                |
| **ANSYS Meshing**                     | Computational mesh generation       |
| **ANSYS Fluent**                      | CFD simulation                      |
| **CFD-Post / Fluent Post-Processing** | Flow-field and aerodynamic analysis |

---

# 🔬 Engineering Concepts Applied

This project combines several areas of mechanical and aerospace engineering:

* Compressible Fluid Mechanics
* Hypersonic Aerodynamics
* Atmospheric Re-entry
* External Aerodynamics
* Shock-Wave Theory
* Boundary-Layer Flow
* Aerodynamic Drag
* Heat Transfer
* Computational Fluid Dynamics
* Finite-Volume Method
* CAD Modelling
* Numerical Simulation

---

# 📁 Repository Structure

```text
Re-Entry-Capsule-CFD/
│
├── README.md
│
├── CAD/
│   ├── Capsule_Model.SLDPRT
│   └── Capsule_Geometry.STEP
│
├── Geometry/
│   └── Computational_Domain/
│
├── Mesh/
│   ├── Mesh_Files/
│   └── Mesh_Statistics/
│
├── ANSYS/
│   ├── Fluent_Case/
│   ├── Fluent_Data/
│   └── Setup/
│
├── Results/
│   ├── Mach_Contours/
│   ├── Pressure_Contours/
│   ├── Temperature_Contours/
│   ├── Velocity_Contours/
│   └── Streamlines/
│
├── Reports/
│   └── Project_Report.pdf
│
└── Images/
    ├── CAD_Model.png
    ├── Mesh.png
    ├── Mach_Contour.png
    ├── Pressure_Contour.png
    └── Temperature_Contour.png
```

---

# 📌 Key Outcomes

The CFD investigation provides an understanding of:

* Formation of the detached bow shock
* Compression of high-speed atmospheric flow
* Pressure rise across the shock
* Flow deceleration near the capsule nose
* Development of the stagnation region
* Temperature increase caused by aerodynamic compression
* Pressure distribution over the capsule
* Wake formation behind the vehicle
* Aerodynamic drag characteristics
* Influence of capsule geometry on the surrounding flow field

---

# 🚀 Future Improvements

The current analysis can be extended to develop a more comprehensive re-entry simulation.

Potential improvements include:

* Mesh independence study
* Validation against published experimental/numerical data
* Multiple Mach-number cases
* Multiple altitude conditions
* Angle-of-attack studies
* Transient re-entry trajectory simulation
* Real-gas thermodynamic models
* High-temperature air chemistry
* Species transport
* Chemical nonequilibrium
* Radiation modelling
* Conjugate heat-transfer analysis
* Thermal protection system modelling
* Ablation modelling
* Aerodynamic coefficient comparison
* Coupled trajectory and CFD analysis

---

# 🎓 Project Significance

This project demonstrates the application of **computational fluid dynamics to atmospheric re-entry vehicle analysis**, combining CAD modelling, compressible-flow physics, numerical simulation, and aerodynamic post-processing.

The workflow provides a foundation for more advanced studies involving **hypersonic aerodynamics, aero-thermodynamics, thermal protection systems, and re-entry trajectory analysis**.

---

## 👨‍💻 Technologies

`ANSYS Fluent` `ANSYS Meshing` `SolidWorks` `CFD` `Hypersonic Aerodynamics` `Compressible Flow` `Re-Entry Aerodynamics` `Aerospace Engineering`

---

## 📜 Disclaimer

This repository represents an **academic/engineering simulation study**. The results are dependent on the selected geometry, atmospheric conditions, numerical models, mesh resolution, and CFD assumptions. They should not be interpreted as flight-qualified or experimentally validated re-entry vehicle performance data.
