# Module 1: Packaging Evolution – From Basics to 3D

---

## Slide: Why is Semiconductor Packaging Needed?

### 🔍 Overview

Semiconductor packaging serves as the essential interface between delicate semiconductor dies and the outside world, providing **protection** and **connectivity**.

---

### 🤪 From Protected Environment to Real World

- **Bare Die (Wafer)**
  - Produced in highly controlled environments (foundries like TSMC, Samsung, Micron, SK Hynix, Intel).
  - Extremely fragile and vulnerable to:
    - Corrosion
    - Moisture
    - Physical damage

- **Purpose of Packaging**
  - **Protection:** Shields the semiconductor die from environmental and mechanical threats.
  - **Interconnectivity:** Allows the die to interface with other components and dies on the system.

---

### 🧩 Packaging Structure: Example of BGA (Ball Grid Array)

- **Die Attach** – Fixes the die to the substrate.
- **Molding Compound** – Encases the die to provide protection.
- **Wire Bond** – Electrically connects the die to the substrate.
- **Substrate** – Foundation for signal routing and mechanical support.
- **Traces & Balls** – Serve as pathways to connect the BGA to the PCB (printed circuit board).

---

### 📱 Real-World Example: iPhone 15 Logic Board

- Apple iPhone 15 internal logic board shows multiple packaged components from different semiconductor vendors:
  - **Broadcom** – Wireless charging
  - **Texas Instruments** – USB interface/PMIC
  - **SK Hynix** – 8GB DRAM
  - **Cirrus Logic** – Audio codec and amplifiers
  - **Renesas** – Power management ICs
  - **STMicroelectronics** – Integrated circuits
  - **Bosch** – MEMS sensors (accelerometer, gyroscope)
  - **Apple Silicon (A17 Pro Processor)**

> 📌 *Infographic courtesy of TechInsights.*

---

## Slide: Silicon Lifecycle – Course Plan Overview

### 🔄 The Lifecycle of a Semiconductor Chip

Understanding semiconductor packaging begins with knowing where it fits into the **silicon lifecycle**. This lifecycle captures the journey of a chip from conception to operation in a final product.

---

### 🥩 Lifecycle Stages

1. **Product Requirements**
2. **Design**
3. **Manufacturing**
4. **Test**
5. **Debug/Bring-up**
6. **In-Field Operation**

> 📌 *Source: Semiconductor Engineering*

---

## Slide: Typical Package Structure

### 🛠 Basic Structure of a Semiconductor Package

- Mold Compound
- Die
- Carrier (Substrate)
- PCB (System Board)

### 🔧 Interconnection Types

- Wirebonding
- Bump/Solder

### 🧪 Carrier Options

Leadframe, Laminate, Plastic, Ceramic, Organic RDL, Silicon, Glass

### 🚀 Package Types

Through-Hole (DIP, TO, PGA), SMT (QFN, QFP, PBGA, LGA, CSP, PoP), Advanced (MCM, CoWoS)



---

## Slide: Anatomy of Packages

### 📏 Categories

#### 📄 Leadframe-Based
- **DIP**: Basic package, gold wires connect die to leads.
- **QFN**: Compact surface-mount package.
- **Leadframe-CSP, Leadframe-QFP**: Cost-effective options for moderate pin-counts.

#### 📄 Laminate-Based
- **PBGA, LGA**: Larger I/O and good thermal performance.
- **Wirebond vs. Flip-Chip PBGA**: Flip-chip uses bumps and underfill for performance.

#### 📄 Advanced Substrates
- **2D**: Dies side-by-side
- **2.1D**: With RDL
- **2.3D**: Organic interposer
- **2.5D**: Silicon interposer (CoWoS)
- **3D**: TSV-stacked chips

---

## Slide: Summary – Nomenclature of Packages

### 📜 Hierarchical Stack

- **Semiconductors**: Single chip or multi-chip
- **Package Substrate (Carrier)**: PBGA, fcCSP, 2D, 2.5D, 3D
- **PCB (Printed Circuit Board)**: Final integration layer

### 🔗 Multi-Chip Packaging

| Type | Interposer/TSV Use          | Example              |
| ---- | --------------------------- | -------------------- |
| 2.3D | Organic / thin-film         | Moderate density     |
| 2.5D | Passive Si interposer + TSV | NVIDIA H100 CoWoS    |
| 3D   | Active TSV                  | HBM stacks, chiplets |

> 🗌 *Source: Semiconductor Advanced Packaging by John H. Lau*

---

## Slide: Comparison of IC Package Types

### 📊 Side-by-Side Feature Analysis

| **Type**         | DIP                        | QFN                           | QFP                               | PBGA                         | CSP                          | 2D                          | 2.1D                | 2.5D                  |
| ---------------- | -------------------------- | ----------------------------- | --------------------------------- | ---------------------------- | ---------------------------- | --------------------------- | ------------------- | --------------------- |
| **Pros**         | Low cost, easy to assemble | Compact, lightweight          | Good pin density, easy to inspect | High pin count, good thermal | Small size, good performance | High integration, low power | Dense I/O, low cost | High I/O, low latency |
| **Cons**         | Bulky, low pin count       | Repairability, small I/O pins | Pins bend easily                  | Limited rework, shelf life   | Reliability (warpage)        | Long die-to-die distance    | RDL reliability     | High cost             |
| **Applications** | Legacy, industrial         | Smartphones, telecom          | ASICs, controllers                | High-performance ICs         | IoT, wearables               | RF, datacenters             | HPC                 | AI GPUs               |

---

✅ *This concludes Module 1: From traditional to 3D packaging.*

---

# Module 2: From Wafer to Package – Assembly and Manufacturing Essentials

---

## Slide: Introduction of a Package Manufacturing Unit

### 🏭 ATMP: Assembly, Testing, Marking, and Packaging

- The **ATMP** process involves converting tested silicon wafers into robust, tested packages ready for final product assembly.
- **OSAT** (Outsourced Semiconductor Assembly and Test) companies such as ASE, Amkor, and TATA specialize in this.
- Many IDMs like Intel, TSMC, Micron, and Samsung perform ATMP **in-house**.

> Example: **Micron ATMP facility**, Sanand, Gujarat  
> - Total area: 1.4 million sq. ft.  
> - Cleanroom class 1000/10000: 500,000 sq. ft.  
> - 📌 *Source: Forbes India*

---

### 🗺 Layout of a Typical ATMP Unit

- **Material Preparation & Storage**
- **Processing Zone (Cleanroom - ISO Class 6 & 7)**:
  - Die bonding
  - Wire or flip-chip bonding
  - Encapsulation
  - RDL (Redistribution Layer)
- **Testing Area**: Electrical, burn-in, and stress screening
- **Warehouse**: Packaged ICs
- **Office & Utility Zones**

> 🧼 Cleanroom standards are crucial to avoid yield loss due to microscopic contamination.

---

## Slide: Review of the Supply Chain

### 🔁 Complete Semiconductor Manufacturing & Packaging Pipeline

1. **Design House**
   - Uses EDA tools and foundry PDKs to produce IC designs (GDSII format).
   - Output: Logical design + test program

2. **Wafer Fabrication**
   - Inputs: Silicon wafers, photolithography tools, gases, chemicals, materials
   - Output: Wafer populated with fabricated ICs

3. **Package Assembly and Test**
   - Inputs: Substrates, bonding tools, molding compounds, chemicals
   - Output: Packaged and tested ICs (e.g., Apple A15 chip)

4. **Board Assembly and Test**
   - Inputs: PCBs, pick-and-place tools, soldering equipment
   - Output: Multiple IC packages mounted and tested on system boards (e.g., phone motherboard)

5. **Product Assembly and Test**
   - Inputs: Final enclosure components, mechanical assembly tools
   - Output: Complete consumer/industrial product (e.g., iPhone)

> 🧠 *Each step adds functional integration, reliability, and value to the final product.*

---

## Slide: Steps Inside the Cleanroom Area

### 🧽 Wafer Preparation in ISO Class 7 Environment

1. **Incoming Wafer Carrier** – Holds multiple fabricated wafers
2. **Wafer Inspection** – Optical/automated surface scan
3. **Wafer Front Tape Lamination** – Protective film applied
4. **Wafer Backside Grinding** – Reduces thickness for thermal & size needs
5. **Tape Frame Mounting** – Fixed to adhesive tape on ring frame
6. **Two-step Wafer Dicing**:
   - Laser Grooving
   - Blade Dicing

> 🔬 Ensures safe handling of thinned wafers in ultra-clean conditions

---

## Slide: Activities Inside the Cleanroom – Wire Bond Packaging

### 🧼 Post-Dicing to Packaging Flow (Wire Bond Approach)

1. **Die Attach**
   - Epoxy dispensing or DAF + precision die placement

2. **Curing**
   - Thermally hardens the adhesive for mechanical strength

3. **Wire Bonding**
   - Free Air Ball (FAB) formation
   - Ball/crescent bonding + looping using gold/copper wire

4. **Molding (Transfer Mold)**
   - Resin encapsulation for protection

5. **Marking**
   - Laser ID or lot trace marking on package surface

> 🧠 *Wire bonding remains dominant due to maturity and cost efficiency.*

---

