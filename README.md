# Stability Analysis of RK2 for Convection–Diffusion Equation

## 📌 Project Overview
This project (AE703: Computational Methods, Term Paper) investigates the **stability and behaviour of the second-order Runge–Kutta (RK2) method** applied to the **1D convection–diffusion equation**.  
The work emphasizes the **stability function, order of accuracy, and numerical behaviour** using **Discrete Fourier Transform (DFT)** and its inverse (IDFT), implemented manually in MATLAB.

## 🛠️ Methods
- **Stability Function Analysis**  
  - Derived the RK2 stability function and applied the criterion \|ξ\| ≤ 1.  
  - Computed maximum allowable time step Δtₘₐₓ for a range of wavenumbers (k).  

- **Numerical Experiments**  
  - Implemented three MATLAB programs:  
    1. Plotting stability function vs Δt for multiple wavenumbers.  
    2. Simulating stable (0.9Δtₘₐₓ), critical (Δtₘₐₓ), and unstable (1.1Δtₘₐₓ) cases.  
    3. Comparing overlapping solutions for Δtₘₐₓ and 0.9Δtₘₐₓ.  

- **Role of DFT/IDFT**  
  - Manual coding of DFT/IDFT for frequency-domain analysis.  
  - Observed effects of numerical parameters on wavenumbers directly.  
  - Validated reconstruction accuracy of solutions in spatial domain.  

## 📊 Key Results
- Stability is maintained (\|ξ\| ≤ 1) for low wavenumbers at larger Δt, but Δtₘₐₓ decreases as k increases.  
- Solutions for **Δt = 0.9Δtₘₐₓ** are smooth and stable.  
- At **Δt = Δtₘₐₓ**, marginal instabilities appear.  
- At **Δt = 1.1Δtₘₐₓ**, oscillations and divergence occur, demonstrating instability.  
- Overlapping plots confirm smoother results at 0.9Δtₘₐₓ compared to Δtₘₐₓ.  

## 🔬 Comparison with Higher-Order Methods
- **RK3 / RK4** allow larger stable time steps than RK2.  
- **RK4** provides fourth-order accuracy, reducing truncation error significantly.  
- Although computationally costlier, higher-order schemes are more efficient for larger Δt.  
