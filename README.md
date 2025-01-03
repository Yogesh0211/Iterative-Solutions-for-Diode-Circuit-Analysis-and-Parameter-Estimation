# Iterative-Solutions-for-Diode-Circuit-Analysis-and-Parameter-Estimation

### Description:  
This project focuses on analyzing the current-voltage behavior of a diode circuit using iterative solvers, extracting diode parameters to fit given data, and applying advanced numerical optimization techniques. The project is divided into two interconnected problems:

---

#### **Problem 1: Current Analysis in a Diode Circuit**  
The task involves calculating the current (\( I \)) and voltage across a diode (\( V_d \)) in a circuit where the diode is connected in series with a resistor (\( R \)). The analysis includes:
- Applying nodal analysis to model the circuit.
- Using the diode equation to iteratively solve for \( V_d \) and \( I \) using the `scipy.optimize.fsolve` method.  
- Plotting:
  - Logarithmic diode current (\( \log I \)) versus source voltage (\( V_s \)).
  - Logarithmic diode current (\( \log I \)) versus diode voltage (\( V_d \)).  
Parameters: \( I_s = 1 \times 10^{-9}, n = 1.7, R = 11k \Omega, T = 350 \, K \), and \( V_s \) ranging from 0.1 V to 2.5 V with 0.1 V increments.

---

#### **Problem 2: Parameter Estimation for a Non-Standard Diode**  
This problem extends the analysis to estimate unknown parameters (\( n \), \( \phi \), \( R \)) of a diode with unconventional characteristics:
- The diode equation includes temperature (\( T \)) and cross-sectional area (\( A \)), where \( A = 1 \times 10^{-8} \, m^2 \) and \( T = 375 \, K \).
- Provided dataset: **`DiodeIV.txt`**, containing source voltage (\( V_s \)) and measured diode current (\( I \)).
- Using `scipy.optimize.leastsq` to iteratively optimize:
  1. Ideality factor (\( n \)),
  2. Barrier height (\( \phi \)),
  3. Resistor (\( R \)).  
- Plotting the measured and predicted logarithmic diode current (\( \log I \)) versus source voltage (\( V_s \)) on the same graph for comparison.

---

#### **Key Deliverables**:
1. A single Python script (`project3.py`) containing:
   - Well-organized and documented code for both problems.
   - Common reusable functions.
2. **Plots**:
   - For Problem 1:  
     - \( \log(I) \) vs. \( V_s \).  
     - \( \log(I) \) vs. \( V_d \).  
   - For Problem 2:  
     - \( \log(I) \) vs. \( V_s \) for both measured data and the model's predictions.  
3. Iterative optimization progress: Print the updated parameter values (\( n, \phi, R \)) at each iteration.
4. Final parameter values for the diode.
5. A summary of residual errors and stopping criteria.

This project applies numerical techniques to real-world diode behavior, demonstrating the use of iterative solvers, nonlinear equations, and parameter extraction in electronic circuit design.
