# Counter

To design a counter with the sequence 0, 1, 2, 4, 7, 0, 1, 2..., we need to break down the task into manageable steps: designing the counter logic, implementing the design in Deeds Digital Simulator, and generating the timing diagram. Here’s a step-by-step guide:

### Step 1: Design the Counter Logic

#### State Diagram and State Table
1. **Identify States**: 
   - State 0: 000
   - State 1: 001
   - State 2: 010
   - State 4: 100
   - State 7: 111

2. **State Transitions**:
   - 000 (0) → 001 (1)
   - 001 (1) → 010 (2)
   - 010 (2) → 100 (4)
   - 100 (4) → 111 (7)
   - 111 (7) → 000 (0)

3. **State Table**:
   | Present State (Q2 Q1 Q0) | Next State (D2 D1 D0) |
   |--------------------------|-----------------------|
   | 000                      | 001                   |
   | 001                      | 010                   |
   | 010                      | 100                   |
   | 100                      | 111                   |
   | 111                      | 000                   |

#### Derive Next State Logic
Use the Karnaugh maps (K-maps) to simplify the next-state logic equations for \(D2\), \(D1\), and \(D0\):

1. **K-map for \(D2\)**:
   ```
   Q2 Q1 Q0 | D2
   -----------------
   0  0  0  | 0
   0  0  1  | 0
   0  1  0  | 1
   0  1  1  | -
   1  0  0  | 1
   1  0  1  | -
   1  1  0  | -
   1  1  1  | 0
   ```
   Simplified: \(D2 = Q1\)

2. **K-map for \(D1\)**:
   ```
   Q2 Q1 Q0 | D1
   -----------------
   0  0  0  | 0
   0  0  1  | 1
   0  1  0  | 0
   0  1  1  | -
   1  0  0  | 0
   1  0  1  | -
   1  1  0  | -
   1  1  1  | 0
   ```
   Simplified: \(D1 = Q0'\)

3. **K-map for \(D0\)**:
   ```
   Q2 Q1 Q0 | D0
   -----------------
   0  0  0  | 1
   0  0  1  | 0
   0  1  0  | 0
   0  1  1  | -
   1  0  0  | 1
   1  0  1  | -
   1  1  0  | -
   1  1  1  | 0
   ```
   Simplified: \(D0 = Q2'Q1 + Q0'\)

### Step 2: Implement the Design in Deeds Digital Simulator

1. **Create a new project in Deeds Digital Simulator**.
2. **Add three D Flip-Flops** to represent the states \(Q2\), \(Q1\), and \(Q0\).
3. **Implement the logic equations** for \(D2\), \(D1\), and \(D0\) using logic gates:
   - \(D2 = Q1\)
   - \(D1 = Q0'\)
   - \(D0 = Q2'Q1 + Q0'\)
4. **Connect the outputs of the Flip-Flops** to the inputs according to the derived logic equations.
5. **Connect a clock signal** to all the Flip-Flops.
6. **Add reset logic** if necessary to start from the state 000.

### Step 3: Simulate and Generate Timing Diagram

1. **Run the simulation** in Deeds Digital Simulator.
2. **Observe the state transitions** and ensure the counter follows the sequence: 0, 1, 2, 4, 7, 0...
3. **Generate the timing diagram** to visualize the states over time.

### Example of the Timing Diagram
```
Clk:  |‾‾|_|‾‾|_|‾‾|_|‾‾|_|‾‾|_|‾‾|_|
Q2:   |0 ‾‾‾‾|0   1‾‾‾‾|1   0‾‾‾‾|0|
Q1:   |0   1‾‾‾‾|1   0‾‾‾‾|0   1‾‾‾‾|
Q0:   |0‾‾‾‾|1   0‾‾‾‾|0   1‾‾‾‾|0|
```

### Final Notes
- The initial state should be set to 000.
- Ensure all connections and logic gates are correctly implemented in the simulator.

By following these steps, you can design, simulate, and verify the counter with the required sequence.