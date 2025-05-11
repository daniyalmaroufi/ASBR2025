# Test Results Report

## Test Report for `rotmat2axisangle` Function

### Test Case 1: 90-degree rotation around z-axis
- **Input:**
    $$
    R_1 = \begin{bmatrix}
    0 & -1 & 0 \\
    1 & 0 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_1 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}, \quad \text{angle}_1 = \frac{\pi}{2}
    $$
- **Status:** Passed

### Test Case 2: 60-degree rotation around x-axis
- **Input:**
    $$
    R_2 = \begin{bmatrix}
    1 & 0 & 0 \\
    0 & \cos\left(\frac{\pi}{3}\right) & -\sin\left(\frac{\pi}{3}\right) \\
    0 & \sin\left(\frac{\pi}{3}\right) & \cos\left(\frac{\pi}{3}\right)
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_2 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \quad \text{angle}_2 = \frac{\pi}{3}
    $$
- **Status:** Passed

### Test Case 3: Identity matrix
- **Input:**
    $$
    R_3 = \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_3 = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}, \quad \text{angle}_3 = 0
    $$
- **Status:** Passed

### Test Case 4: 180-degree rotation around x-axis
- **Input:**
    $$
    R_4 = \begin{bmatrix}
    -1 & 0 & 0 \\
    0 & -1 & 0 \\
    0 & 0 & -1
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_4 = \text{NaN}, \quad \text{angle}_4 = \pi
    $$
- **Status:** Passed

### Test Case 5: Zero matrix
- **Input:**
    $$
    R_5 = \begin{bmatrix}
    0 & 0 & 0 \\
    0 & 0 & 0 \\
    0 & 0 & 0
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_5 = \text{NaN}, \quad \text{angle}_5 = 0
    $$
- **Status:** Passed

### Test Case 6: Invalid rotation matrix
- **Input:**
    $$
    R_6 = \begin{bmatrix}
    1 & 2 & 3 \\
    4 & 5 & 6 \\
    7 & 8 & 9
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_6 = \text{NaN}, \quad \text{angle}_6 = 0
    $$
- **Status:** Passed

### Test Case 7: Large rotation angle
- **Input:**
    $$
    R_7 = \begin{bmatrix}
    0 & -1 & 0 \\
    1 & 0 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_7 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}, \quad \text{angle}_7 = \frac{\pi}{2}
    $$
- **Status:** Passed

### Test Case 8: Small rotation angle
- **Input:**
    $$
    R_8 = \begin{bmatrix}
    1 & 0 & 0 \\
    0 & \cos(1 \times 10^{-3}) & -\sin(1 \times 10^{-3}) \\
    0 & \sin(1 \times 10^{-3}) & \cos(1 \times 10^{-3})
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_8 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \quad \text{angle}_8 = 1 \times 10^{-3}
    $$
- **Status:** Passed

### Test Case 9: Negative rotation angle
- **Input:**
    $$
    R_9 = \begin{bmatrix}
    0 & 1 & 0 \\
    -1 & 0 & 0 \\
    0 & 0 & 1
    \end{bmatrix}
    $$
- **Output:**
    $$
    \text{axis}_9 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}, \quad \text{angle}_9 = -\frac{\pi}{2}
    $$
- **Status:** Passed

### Test Case 10: Non-orthogonal matrix
**Input:**
$$
R_{10} = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 2
\end{bmatrix}
$$

**Output:**
$$
\text{axis}_{10} = \text{NaN}, \quad \text{angle}_{10} = 0
$$

**Status:** Passed

### Test Case 11: Matrix with NaN values
**Input:**
$$
R_{11} = \begin{bmatrix}
1 & 0 & 0 \\
0 & \text{NaN} & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Output:**
$$
\text{axis}_{11} = \text{NaN}, \quad \text{angle}_{11} = 0
$$

**Status:** Passed

### Test Case 12: Matrix with Inf values
**Input:**
$$
R_{12} = \begin{bmatrix}
1 & 0 & 0 \\
0 & \infty & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Output:**
$$
\text{axis}_{12} = \text{NaN}, \quad \text{angle}_{12} = 0
$$

**Status:** Passed

### Test Case 13: Matrix with values less than -1
**Input:**
$$
R_{13} = \begin{bmatrix}
1 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Output:**
$$
\text{axis}_{13} = \text{NaN}, \quad \text{angle}_{13} = 0
$$

**Status:** Passed

## Test Report for `rotmat2quaternion` Function

### Test Case 1: 90-degree rotation around z-axis
- **Input:**
  $$
  R_1 = \begin{bmatrix}
  0 & -1 & 0 \\
  1 & 0 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_1 = \begin{bmatrix} \frac{\sqrt{2}}{2} \\ 0 \\ 0 \\ \frac{\sqrt{2}}{2} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 2: 60-degree rotation around x-axis
- **Input:**
  $$
  R_2 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & \cos\left(\frac{\pi}{3}\right) & -\sin\left(\frac{\pi}{3}\right) \\
  0 & \sin\left(\frac{\pi}{3}\right) & \cos\left(\frac{\pi}{3}\right)
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_2 = \begin{bmatrix} \cos\left(\frac{\pi}{6}\right) \\ \sin\left(\frac{\pi}{6}\right) \\ 0 \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 3: Identity matrix
- **Input:**
  $$
  R_3 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & 1 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_3 = \begin{bmatrix} 1 \\ 0 \\ 0 \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 4: 180-degree rotation around x-axis
- **Input:**
  $$
  R_4 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & -1 & 0 \\
  0 & 0 & -1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_4 = \begin{bmatrix} 0 \\ 1 \\ 0 \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 5: Zero matrix
- **Input:**
  $$
  R_5 = \begin{bmatrix}
  0 & 0 & 0 \\
  0 & 0 & 0 \\
  0 & 0 & 0
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_5 = \begin{bmatrix} \text{NaN} \\ \text{NaN} \\ \text{NaN} \\ \text{NaN} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 6: Invalid rotation matrix
- **Input:**
  $$
  R_6 = \begin{bmatrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 9
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_6 = \begin{bmatrix} \text{NaN} \\ \text{NaN} \\ \text{NaN} \\ \text{NaN} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 7: Large rotation angle
- **Input:**
  $$
  R_7 = \begin{bmatrix}
  0 & -1 & 0 \\
  1 & 0 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_7 = \begin{bmatrix} \frac{\sqrt{2}}{2} \\ 0 \\ 0 \\ \frac{\sqrt{2}}{2} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 8: Small rotation angle
- **Input:**
  $$
  R_8 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & \cos(1 \times 10^{-3}) & -\sin(1 \times 10^{-3}) \\
  0 & \sin(1 \times 10^{-3}) & \cos(1 \times 10^{-3})
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_8 = \begin{bmatrix} \cos\left(\frac{1 \times 10^{-3}}{2}\right) \\ \sin\left(\frac{1 \times 10^{-3}}{2}\right) \\ 0 \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 9: Negative rotation angle around x-axis
- **Input:**
  $$
  R_9 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & \cos\left(-\frac{\pi}{3}\right) & -\sin\left(-\frac{\pi}{3}\right) \\
  0 & \sin\left(-\frac{\pi}{3}\right) & \cos\left(-\frac{\pi}{3}\right)
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_9 = \begin{bmatrix} \cos\left(-\frac{\pi}{6}\right) \\ \sin\left(-\frac{\pi}{6}\right) \\ 0 \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 10: Negative rotation angle around y-axis
- **Input:**
  $$
  R_{10} = \begin{bmatrix}
  \cos\left(-\frac{\pi}{3}\right) & 0 & \sin\left(-\frac{\pi}{3}\right) \\
  0 & 1 & 0 \\
  -\sin\left(-\frac{\pi}{3}\right) & 0 & \cos\left(-\frac{\pi}{3}\right)
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_{10} = \begin{bmatrix} \cos\left(-\frac{\pi}{6}\right) \\ 0 \\ \sin\left(-\frac{\pi}{6}\right) \\ 0 \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 11: Negative rotation angle around z-axis
- **Input:**
  $$
  R_{11} = \begin{bmatrix}
  \cos\left(-\frac{\pi}{3}\right) & -\sin\left(-\frac{\pi}{3}\right) & 0 \\
  \sin\left(-\frac{\pi}{3}\right) & \cos\left(-\frac{\pi}{3}\right) & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_{11} = \begin{bmatrix} \cos\left(-\frac{\pi}{6}\right) \\ 0 \\ 0 \\ \sin\left(-\frac{\pi}{6}\right) \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 12: Matrix with NaN values
- **Input:**
  $$
  R_{12} = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & \text{NaN} & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_{12} = \begin{bmatrix} \text{NaN} \\ \text{NaN} \\ \text{NaN} \\ \text{NaN} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 13: Matrix with Inf values
- **Input:**
  $$
  R_{13} = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & \infty & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_{13} = \begin{bmatrix} \text{NaN} \\ \text{NaN} \\ \text{NaN} \\ \text{NaN} \end{bmatrix}
  $$
- **Status:** Passed

### Test Case 14: Matrix with values less than -1
- **Input:**
  $$
  R_{14} = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & -2 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  q_{14} = \begin{bmatrix} \text{NaN} \\ \text{NaN} \\ \text{NaN} \\ \text{NaN} \end{bmatrix}
  $$
- **Status:** Passed

## Test Report for `rotmat2zyz` Function

### Test Case 1: 90-degree Rotation Around y-axis
- **Input:**
  $$
  R_1 = \begin{bmatrix}
  0 & 0 & 1 \\
  0 & 1 & 0 \\
  -1 & 0 & 0
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_1, \theta_1, \psi_1) = (0, \frac{\pi}{2}, 0)
  $$
- **Status:** Passed

### Test Case 2: Identity Matrix
- **Input:**
  $$
  R_2 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & 1 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_2, \theta_2, \psi_2) = (\text{NaN}, \text{NaN}, \text{NaN})
  $$
- **Status:** Passed

### Test Case 3: Zero Matrix
- **Input:**
  $$
  R_3 = \begin{bmatrix}
  0 & 0 & 0 \\
  0 & 0 & 0 \\
  0 & 0 & 0
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_3, \theta_3, \psi_3) = (\text{NaN}, \text{NaN}, \text{NaN})
  $$
- **Status:** Passed

### Test Case 4: Invalid Rotation Matrix
- **Input:**
  $$
  R_4 = \begin{bmatrix}
  1 & 2 & 3 \\
  4 & 5 & 6 \\
  7 & 8 & 9
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_4, \theta_4, \psi_4) = (\text{NaN}, \text{NaN}, \text{NaN})
  $$
- **Status:** Passed

### Test Case 5: Small Rotation Angle Around y-axis
- **Input:**
  $$
  R_5 = \begin{bmatrix}
  \cos(1 \times 10^{-3}) & 0 & \sin(1 \times 10^{-3}) \\
  0 & 1 & 0 \\
  -\sin(1 \times 10^{-3}) & 0 & \cos(1 \times 10^{-3})
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_5, \theta_5, \psi_5) = (0, 1 \times 10^{-3}, 0)
  $$
- **Status:** Passed

### Test Case 6: A Rotation Matrix with a Set of Angles
- **Input:**
    $$
    R_6 = \text{eul2rotm}((\frac{\pi}{3}, \frac{\pi}{6}, -\frac{\pi}{3}), ZYZ) = \begin{bmatrix}
    0.9665 & -0.0580 & 0.2500 \\
    -0.0580 & 0.8995 & 0.4330 \\
    -0.2500 & -0.4330 & 0.8660
    \end{bmatrix}
    $$
- **Output:**
    $$
    (\phi_6, \theta_6, \psi_6) = \text{rotm2eul}(R_6, ZYZ) = (-2.0944, -0.5236, 2.0944)
    $$
- **Status:** Passed

### Test Case 7: Singular Case: $\theta = \pi/2$
- **Input:**
  $$
  R_7 = \begin{bmatrix}
  1 & 0 & 0 \\
  0 & 0 & -1 \\
  0 & 1 & 0
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_7, \theta_7, \psi_7) = (0, \frac{\pi}{2}, 0)
  $$
- **Status:** Passed

### Test Case 8: Rotation Around z-axis with $\theta = 0$
- **Input:**
  $$
  R_8 = \begin{bmatrix}
  0 & -1 & 0 \\
  1 & 0 & 0 \\
  0 & 0 & 1
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_8, \theta_8, \psi_8) = (0, 0, \frac{\pi}{2})
  $$
- **Status:** Passed

### Test Case 9: Rotation Around z-axis with $\theta = \pi$
- **Input:**
  $$
  R_9 = \begin{bmatrix}
  0 & -1 & 0 \\
  1 & 0 & 0 \\
  0 & 0 & -1
  \end{bmatrix}
  $$
- **Output:**
  $$
  (\phi_9, \theta_9, \psi_9) = (0, \pi, \frac{\pi}{2})
  $$
- **Status:** Passed

## Test Report for `rotmat2rollpitchyaw` Function

### Test Case 1: 90-degree rotation around y-axis
**Input:**
$$
R_1 = \begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
-1 & 0 & 0
\end{bmatrix}
$$

**Output:**
$$
\phi_1 = 0, \quad \theta_1 = \frac{\pi}{2}, \quad \psi_1 = 0
$$

**Status:** Passed

### Test Case 2: Identity matrix
**Input:**
$$
R_2 = I_3
$$

**Output:**
$$
\phi_2 = \text{NaN}, \quad \theta_2 = \text{NaN}, \quad \psi_2 = \text{NaN}
$$

**Status:** Passed

### Test Case 3: Zero matrix
**Input:**
$$
R_3 = \begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$

**Output:**
$$
\phi_3 = \text{NaN}, \quad \theta_3 = \text{NaN}, \quad \psi_3 = \text{NaN}
$$

**Status:** Passed

### Test Case 4: Invalid rotation matrix
**Input:**
$$
R_4 = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
$$

**Output:**
$$
\phi_4 = \text{NaN}, \quad \theta_4 = \text{NaN}, \quad \psi_4 = \text{NaN}
$$

**Status:** Passed

### Test Case 5: Small rotation angle around y-axis
**Input:**
$$
R_5 = \begin{bmatrix}
\cos(10^{-3}) & 0 & \sin(10^{-3}) \\
0 & 1 & 0 \\
-\sin(10^{-3}) & 0 & \cos(10^{-3})
\end{bmatrix}
$$

**Output:**
$$
\phi_5 = 0, \quad \theta_5 = 10^{-3}, \quad \psi_5 = 0
$$

**Status:** Passed

### Test Case 6: 90-degree rotation around x-axis
**Input:**
$$
R_6 = \begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & -1 \\
0 & 1 & 0
\end{bmatrix}
$$

**Output:**
$$
\phi_6 = 0, \quad \theta_6 = 0, \quad \psi_6 = \frac{\pi}{2}
$$

**Status:** Passed

### Test Case 7: Singular case: 90-degree rotation around y-axis
**Input:**
$$
R_7 = \begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
-1 & 0 & 0
\end{bmatrix}
$$

**Output:**
$$
\phi_7 = 0, \quad \theta_7 = \frac{\pi}{2}, \quad \psi_7 = 0
$$

**Status:** Passed

### Test Case 8: 60-degree rotation around x-axis
**Input:**
$$
R_8 = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos\left(\frac{\pi}{3}\right) & -\sin\left(\frac{\pi}{3}\right) \\
0 & \sin\left(\frac{\pi}{3}\right) & \cos\left(\frac{\pi}{3}\right)
\end{bmatrix}
$$

**Output:**
$$
\phi_8 = 0, \quad \theta_8 = 0, \quad \psi_8 = \frac{\pi}{3}
$$

**Status:** Passed

### Test Case 9: 180-degree rotation around z-axis
**Input:**
$$
R_9 = \begin{bmatrix}
-1 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Output:**
$$
\phi_9 = \pi, \quad \theta_9 = 0, \quad \psi_9 = 0
$$

**Status:** Passed

## Test Report for `axisangle2rotmat` Function

### Test Case 1: 90-degree rotation around z-axis
**Input:**
- Axis: $[0; 0; 1]$
- Angle: $\frac{\pi}{2}$

**Output:**
$$
R_1 = \begin{bmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Status:** Passed

### Test Case 2: 60-degree rotation around x-axis
**Input:**
- Axis: $[1; 0; 0]$
- Angle: $\frac{\pi}{3}$

**Output:**
$$
R_2 = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(\frac{\pi}{3}) & -\sin(\frac{\pi}{3}) \\
0 & \sin(\frac{\pi}{3}) & \cos(\frac{\pi}{3})
\end{bmatrix}
$$

**Status:** Passed

### Test Case 3: Identity matrix
**Input:**
- Axis: $[1; 0; 0]$
- Angle: $0$

**Output:**
$$
R_3 = I_3
$$

**Status:** Passed

### Test Case 4: 180-degree rotation around x-axis
**Input:**
- Axis: $[1; 0; 0]$
- Angle: $\pi$

**Output:**
$$
R_4 = \begin{bmatrix}
1 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & -1
\end{bmatrix}
$$

**Status:** Passed

### Test Case 5: Zero axis and zero angle
**Input:**
- Axis: $[0; 0; 0]$
- Angle: $0$

**Output:**
$$
R_5 = I_3
$$

**Status:** Passed

### Test Case 6: Invalid axis
**Input:**
- Axis: $[1; 3; 4]$
- Angle: $\frac{\pi}{2}$

**Output:**
$$
R_6 = \text{NaN}(3)
$$

**Status:** Passed

### Test Case 7: Large rotation angle
**Input:**
- Axis: $[0; 0; 1]$
- Angle: $\frac{\pi}{2}$

**Output:**
$$
R_7 = \begin{bmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Status:** Passed

### Test Case 8: Small rotation angle
**Input:**
- Axis: $[1; 0; 0]$
- Angle: $1 \times 10^{-3}$

**Output:**
$$
R_8 = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(1 \times 10^{-3}) & -\sin(1 \times 10^{-3}) \\
0 & \sin(1 \times 10^{-3}) & \cos(1 \times 10^{-3})
\end{bmatrix}
$$

**Status:** Passed

### Test Case 9: Negative rotation angle
**Input:**
- Axis: $[0; 0; 1]$
- Angle: $\frac{3\pi}{2}$

**Output:**
$$
R_9 = \begin{bmatrix}
0 & 1 & 0 \\
-1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Status:** Passed

### Test Case 10: Negative rotation axis
**Input:**
- Axis: $[0; 0; -1]$
- Angle: $\frac{\pi}{2}$

**Output:**
$$
R_{10} = \begin{bmatrix}
0 & 1 & 0 \\
-1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

**Status:** Passed

### Test Case 11: Axis with NaN values
**Input:**
- Axis: $[\text{NaN}; 1; 0]$
- Angle: $\pi$

**Output:**
$$
R_{11} = \text{NaN}(3)
$$

**Status:** Passed

### Test Case 12: Axis with Inf values
**Input:**
- Axis: $[\text{Inf}; 1; 0]$
- Angle: $\pi$

**Output:**
$$
R_{12} = \text{NaN}(3)
$$

**Status:** Passed

### Test Case 13: Axis with values less than -1
**Input:**
- Axis: $[1; -2; 0]$
- Angle: $\frac{\pi}{2}$

**Output:**
$$
R_{13} = \text{NaN}(3)
$$

**Status:** Passed

**Summary:** All tests passed.

## Test Report for `quaternion2rotmat` Function

### Test Case 1: 90-degree rotation around z-axis
- **Input**: 
  $$ q_1 = \left[\frac{\sqrt{2}}{2}, 0, 0, \frac{\sqrt{2}}{2}\right] $$
- **Expected Output**: 
  $$ R_1 = \begin{bmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} $$
- **Status**: Passed

### Test Case 2: 60-degree rotation around x-axis
- **Input**: 
  $$ q_2 = \left[\cos\left(\frac{\pi}{6}\right), \sin\left(\frac{\pi}{6}\right), 0, 0\right] $$
- **Expected Output**: 
  $$ R_2 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & \cos\left(\frac{\pi}{3}\right) & -\sin\left(\frac{\pi}{3}\right) \\ 0 & \sin\left(\frac{\pi}{3}\right) & \cos\left(\frac{\pi}{3}\right) \end{bmatrix} $$
- **Status**: Passed

### Test Case 3: Identity matrix
- **Input**: 
  $$ q_3 = [1, 0, 0, 0] $$
- **Expected Output**: 
  $$ R_3 = I_3 $$
- **Status**: Passed

### Test Case 4: 180-degree rotation around x-axis
- **Input**: 
  $$ q_4 = [0, 1, 0, 0] $$
- **Expected Output**: 
  $$ R_4 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & -1 \end{bmatrix} $$
- **Status**: Passed

### Test Case 5: Zero quaternion
- **Input**: 
  $$ q_5 = [0, 0, 0, 0] $$
- **Expected Output**: 
  $$ R_5 = \text{NaN}(3) $$
- **Status**: Passed

### Test Case 6: Invalid quaternion
- **Input**: 
  $$ q_6 = [1, 2, 3, 4] $$
- **Expected Output**: 
  $$ R_6 = \text{NaN}(3) $$
- **Status**: Passed

### Test Case 7: Large rotation angle
- **Input**: 
  $$ q_7 = \left[\frac{\sqrt{2}}{2}, 0, 0, \frac{\sqrt{2}}{2}\right] $$
- **Expected Output**: 
  $$ R_7 = \begin{bmatrix} 0 & -1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} $$
- **Status**: Passed

### Test Case 8: Small rotation angle
- **Input**: 
  $$ q_8 = \left[\cos\left(\frac{1 \times 10^{-3}}{2}\right), \sin\left(\frac{1 \times 10^{-3}}{2}\right), 0, 0\right] $$
- **Expected Output**: 
  $$ R_8 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & \cos(1 \times 10^{-3}) & -\sin(1 \times 10^{-3}) \\ 0 & \sin(1 \times 10^{-3}) & \cos(1 \times 10^{-3}) \end{bmatrix} $$
- **Status**: Passed

### Test Case 9: Negative rotation angle around x-axis
- **Input**: 
  $$ q_9 = \left[\cos\left(\frac{\pi}{6}\right), \sin\left(-\frac{\pi}{6}\right), 0, 0\right] $$
- **Expected Output**: 
  $$ R_9 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & \cos\left(-\frac{\pi}{3}\right) & -\sin\left(-\frac{\pi}{3}\right) \\ 0 & \sin\left(-\frac{\pi}{3}\right) & \cos\left(-\frac{\pi}{3}\right) \end{bmatrix} $$
- **Status**: Passed

### Test Case 10: 180-degree rotation around z-axis
- **Input**: 
  $$ q_{10} = [0, 0, 0, 1] $$
- **Expected Output**: 
  $$ R_{10} = \begin{bmatrix} -1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 1 \end{bmatrix} $$
- **Status**: Passed

### Test Case 11: Non-unit Quaternion
- **Input**: 
  $$ q_{11} = [1, 2, 5, 7] $$
- **Expected Output**: 
  $$ R_{11} = \text{NaN}(3) $$
- **Status**: Passed

### Test Case 12: Quaternion with NaN values
- **Input**: 
  $$ q_{12} = [1, \text{NaN}, 0, 1] $$
- **Expected Output**: 
  $$ R_{12} = \text{NaN}(3) $$
- **Status**: Passed

### Test Case 13: Quaternion with Inf values
- **Input**: 
  $$ q_{13} = [1, \text{Inf}, 1, 0] $$
- **Expected Output**: 
  $$ R_{13} = \text{NaN}(3) $$
- **Status**: Passed

### Test Case 14: Quaternion with values less than -1
- **Input**: 
  $$ q_{14} = [1, -2, 1, 0] $$
- **Expected Output**: 
  $$ R_{14} = \text{NaN}(3) $$
- **Status**: Passed

**Summary**: All test cases passed.

## Test Report for `test_inputTransfmatScrew`

### Test Case 1: Screw Axis Transformation Based on Inputs

**Title:** Screw Axis Transformation Based on Inputs

**Input:**
- $T_{\text{initial}} = \begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix}$
- $p = \begin{bmatrix} 0 & 2 & 0 \end{bmatrix}$
- $\hat{s} = \begin{bmatrix} 0 & 0 & 1 \end{bmatrix}$
- $h = 2$
- $\theta = \pi$

**Output:**
- $T_{\text{final}}$: Transformation matrix after applying the screw transformation.
- $T_{\text{intermediate}}$: Intermediate transformation matrix.
- $point$: Point after transformation.
- $s_{\text{axis}}$: Screw axis.
- $pitch$: Pitch of the screw.
- $angle$: Angle of rotation.

**Status:** Passed

### Test Case 2: Screw Axis Transformation Back to Origin

**Title:** Screw Axis Transformation Back to Origin

**Input:**
- $T_{\text{final}}$: Transformation matrix after applying the screw transformation.
- $point$: Point after transformation.
- $s_{\text{axis}}$: Screw axis.
- $pitch$: Pitch of the screw.
- $angle$: Angle of rotation.

**Output:**
- $T_{\text{origin}}$: Transformation matrix back to the origin.
- Other outputs are not used in this test case.

**Status:** Passed

