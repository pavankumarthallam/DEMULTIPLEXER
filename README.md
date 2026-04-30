# 1-to-4 De-multiplexer (DEMUX)

A **1-to-4 De-multiplexer** is a combinational logic circuit designed to route a single input signal to one of four possible output lines based on the configuration of two select lines. It is fundamentally a **data distributor**.

---

## 1. Logic Diagram


---

## 2. Functional Overview
The circuit consists of one data input, two control (select) lines, and four output lines.

| Component | Signal | Description |
| :--- | :--- | :--- |
| **Input** | $I$ | The single data line to be distributed[cite: 1, 2] |
| **Select Lines** | $S_1, S_0$ | Control signals used to choose the destination output[cite: 1, 2] |
| **Outputs** | $Y_0, Y_1, Y_2, Y_3$ | The four possible destination lines[cite: 1, 2] |

---

## 3. Truth Table
The select lines ($S_1, S_0$) determine which output is active. All other outputs remain at logic `0`.

| $S_1$ | $S_0$ | Active Output | Output States |
|:---:|:---:|:---:|:--- |
| 0 | 0 | $Y_0$ | $Y_0 = I; Y_1=0; Y_2=0; Y_3=0$[cite: 1, 2] |
| 0 | 1 | $Y_1$ | $Y_0=0; Y_1 = I; Y_2=0; Y_3=0$[cite: 1, 2] |
| 1 | 0 | $Y_2$ | $Y_0=0; Y_1=0; Y_2 = I; Y_3=0$[cite: 1, 2] |
| 1 | 1 | $Y_3$ | $Y_0=0; Y_1=0; Y_2=0; Y_3 = I$[cite: 1, 2] |

---

## 4. Logical Expressions
The Boolean equations for each output line are derived as follows:

*   **$Y_0 = \bar{S_1} \cdot \bar{S_0} \cdot I$**[cite: 1, 2]
*   **$Y_1 = \bar{S_1} \cdot S_0 \cdot I$**[cite: 1, 2]
*   **$Y_2 = S_1 \cdot \bar{S_0} \cdot I$**[cite: 1, 2]
*   **$Y_3 = S_1 \cdot S_0 \cdot I$**[cite: 1, 2]

---

## 5. Applications
*   **Communication Systems:** Directing data streams to multiple receivers[cite: 1, 2].
*   **Memory Management:** Routing data to specific memory banks or CPU registers[cite: 1, 2].
*   **Serial-to-Parallel Conversion:** Converting bit-streams into parallel data formats[cite: 1, 2].
*   **ALU Routing:** Directing arithmetic results to correct storage locations[cite: 1, 2].
