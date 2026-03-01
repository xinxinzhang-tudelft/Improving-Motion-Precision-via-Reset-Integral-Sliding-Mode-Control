# Experimental Video Description

The video **"Experimental Video-Fig8 & Fig 10.mp4"** illustrates the experimental validation of the manuscript:

## Improving Motion Precision Through Reset-Integral Sliding Mode Control

**Xinxin Zhang, Member, IEEE**  
**Leonid Freidovich, Senior Member, IEEE**  

Department of Applied Physics and Electronics  
Umeå University, Umeå, Sweden  

---

## Abstract

This work addresses the performance limitations of reset controllers in motion control applications. Although reset controllers effectively circumvent fundamental linear gain-phase trade-offs, their nonlinear nature induces undesirable steady-state behaviors, notably limit cycle oscillations and sensitivity to external disturbances.

To mitigate these drawbacks, we propose a control architecture that integrates a reset controller with an Integral Sliding Mode Control (ISMC) mechanism for Linear Time-Invariant (LTI) systems. Within this framework:

- The nominal reset system governs the transient response and trajectory tracking.
- The ISMC component is explicitly designed to eliminate limit cycles and enhance robust disturbance rejection.

A stability analysis and systematic design procedure for the Reset-ISMC framework are developed to guarantee perturbation suppression. The efficacy of the proposed approach is validated experimentally on a servo motion stage. The results demonstrate that the Reset-ISMC strategy successfully suppresses steady-state limit-cycle oscillations and provides superior disturbance rejection compared to both linear benchmarks and conventional reset control systems.

---

# Experimental Case Studies Presented in the Video

The video presents two experimental case studies corresponding to **Fig. 8** and **Fig. 10** in the manuscript.

---

## Case Study 1 — Fig. 8  
### Simultaneous Trajectory Tracking and Disturbance Rejection

To evaluate the effectiveness of the Reset-ISMC architecture, the system is subjected to simultaneous trajectory tracking and disturbance rejection.

### Reference Signal
\[
r(t) = 0.04\sin(4\pi t)
\]

### Disturbance Signal
\[
d_2(t) = 0.017\sin(0.2\pi t) + 0.085\sin(0.6\pi t) + 0.136\sin(\pi t)
\]

- The disturbance amplitude is deliberately chosen to exceed the reference amplitude.
- The disturbance bound is quantified as:
  \[
  \Delta = 0.22
  \]

### ISMC Design Parameters

Following the proposed design algorithm:

- Boundary layer thickness:  
  \[
  \delta = 0.25
  \]
- Switching gain:  
  \[
  \rho = 28.34
  \]

The reachability condition is satisfied:
\[
\rho > |CB|\Delta
\]

### Experimental Observations

The video shows:

- Time evolution of the tracking error.
- Control input signals for four comparative controllers:
  - PID
  - PCID
  - PID-ISMC
  - PCID-ISMC

### Performance Highlights

- **PCID vs PID**:  
  Maximum steady-state error reduced from 2.512 to 0.970 (61.4% improvement).

- **PCID-ISMC vs PCID**:  
  Maximum steady-state error reduced from 0.970 to 0.280 (71.1% improvement).

- PID-ISMC and PCID-ISMC exhibit comparable steady-state precision, indicating that ISMC dominates the steady-state error dynamics.

- PCID-ISMC achieves improved accuracy with reduced control effort compared to standalone PCID.

---

## Case Study 2 — Fig. 10  
### Limit Cycle Suppression

The second experiment demonstrates the suppression of limit cycles in the velocity control system.

### Key Observations

- The baseline PCI controller exhibits steady-state limit cycle oscillations.
- The proposed PCI-ISMC architecture:
  - Completely suppresses limit cycles.
  - Preserves transient response characteristics.
  - Does not compromise dynamic performance.

### Significance

Unlike many established limit-cycle mitigation techniques, which often introduce trade-offs in transient or steady-state performance, the proposed ISMC-based approach:

- Eliminates steady-state oscillations,
- Maintains transient performance,
- Enhances robustness against external disturbances.

---

# Summary

The experimental video clearly demonstrates that:

- The Reset-ISMC architecture eliminates steady-state limit cycles.
- It significantly improves disturbance rejection capability.
- It enhances steady-state precision.
- It maintains desirable transient response.
- It reduces control effort compared to conventional reset control strategies.

These results validate the theoretical developments and confirm the practical effectiveness of the proposed control framework.
