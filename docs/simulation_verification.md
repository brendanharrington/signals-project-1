# Simulation and Verification

## Task 4: Simulink Verification with Transfer Function

### Transfer Function Implementation
The transfer function derived from the theoretical analysis is implemented directly in Simulink:

- Numerator: `[1]`
- Denominator: `[300, 97.2, 0]`

### Input Signal
The rectangular pulse input used:
- Amplitude \( A = 972\,N \)
- Duration: 10 seconds

### Results
Simulation confirms the rover travels exactly 100 m, verifying theoretical predictions.

## Task 5: Direct Physical Model Verification

### Simulink Direct Implementation
Implemented directly using force balance equations:
- Input force \( f_{motor}(t) \)
- Friction force calculated as \( 97.2\dot{x}_1(t) \)
- Rover acceleration integrated twice to obtain position.

### Results
Position output from direct model matches exactly the transfer function implementation, confirming correctness.

## Task 6: Coupled Rover-Trailer Equations
The coupled system equations:

\[
M_1 \ddot{x}_1 = f_{motor} - 97.2 \dot{x}_1 - k(x_1 - x_2)
\]

\[
M_2 \ddot{x}_2 = k(x_1 - x_2) - 97.2 \dot{x}_2
\]

- \( M_1 = 300\,kg \), \( M_2 = 75\,kg \), spring constant \( k = 9000\,N/m \).

## Task 7: Coupled System Simulation

### Implementation
- Coupled equations implemented in Simulink with two interconnected subsystems.
- Rectangular pulse input maintained.

### Results
- Rover travels less than 100 m due to additional load.
- The elastic rod stretching is plotted, confirming it remains within safe operational limits.

## Task 8: Motor Input Voltage and Saturation

### Implementation
- Input converted from voltage \( v(t) \) to force using factor \(100\,N/mV\).
- Force output capped using a saturation block at \(\pm 2000\,N\).

### Results
Simulation reproduces previous results accurately, validating the correct scaling and force limitation in the implementation.

