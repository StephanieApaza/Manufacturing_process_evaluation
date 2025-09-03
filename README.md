# Evaluate a manufacturing process

## 🎯Objective
Analyze the manufacturing_parts table and create an alert that flags whether the height of a product is within the control limits for each operator.

## 🧩Analysis
- In this project, I applied statistical process control (SPC) to monitor product height variations for each operator.
- A sliding window of length 5 (ROWS BETWEEN 4 PRECEDING AND CURRENT ROW) was used to calculate the moving average (avg_height) and standard deviation (stddev_height).
- The upper control limit (UCL) and lower control limit (LCL) were calculated with the formula.
- Incomplete windows (rows < 5) were filtered out to ensure valid calculations.
- An alert flag (TRUE/FALSE) was created to identify whether each part’s height is within or outside the control limits.

## 🧭Conclusion
This analysis helps detect potential quality issues by flagging products that fall outside the expected statistical range, **ensuring early detection of process deviations**.

**True** in the column alert indicates that the product falls outside the acceptable range.

**False** means the product is in the acceptable range.
