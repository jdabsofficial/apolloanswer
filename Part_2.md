# W 250 x 73 COLUMN ANALYSIS - PART 2
## Complete Solution with Euler's Column Buckling Theory

---

## GIVEN INFORMATION

- **Section:** W 250 x 73
- **Column Length:** L = 15 m = 15,000 mm
- **Proportionality Limit:** PL = 235 MPa
- **Modulus of Elasticity:** E = 200,000 MPa
- **Factor of Safety:** FS = 2.5

---

## SECTION PROPERTIES (W 250 x 73)

| Property | Symbol | Value |
|----------|--------|-------|
| Area | A | 9,280 mm² |
| Depth | d | 253 mm |
| Flange Width | bf | 254 mm |
| Flange Thickness | tf | 14.2 mm |
| Moment of Inertia (x-axis) | Ix | 113 × 10⁶ mm⁴ |
| Moment of Inertia (y-axis) | Iy | 38.8 × 10⁶ mm⁴ |

---

## EULER'S FORMULA LIMITATIONS

### Critical Conditions:

**Rule 1:** If P/A > PL, Euler's Formula is NOT applicable
- When stress exceeds proportionality limit
- Material behavior is no longer elastic

**Rule 2:** If (KL/r) < 100, Euler's Formula is NOT valid
- Proportionality limit becomes the critical stress
- Column fails by yielding before buckling

### Valid Euler's Formula Range:
- Stress must remain below proportionality limit (Fe ≤ PL)
- Slenderness ratio must be ≥ 100 (KL/r ≥ 100)

---

# CONDITION 1: BOTH ENDS PINNED

---

## QUESTION 1: EFFECTIVE LENGTH FACTOR (PINNED-PINNED)

### Support Condition Analysis:
- Both ends are pinned (hinged)
- Standard case for Euler's critical load

### Effective Length Factors by Support Condition:
- **Pinned-Pinned:** K = 1.0 ✓
- Fixed-Free: K = 2.0
- Fixed-Pinned: K = 0.7
- Fixed-Fixed: K = 0.5

### **ANSWER: A. 1.0**

---

## QUESTION 2: RADIUS OF GYRATION (X-AXIS)

### Formula:
$$r_x = \sqrt{\frac{I_x}{A}}$$

### Solution:
$$r_x = \sqrt{\frac{113 \times 10^6}{9,280}}$$

$$r_x = \sqrt{12,176.72}$$

$$r_x = 110.35 \text{ mm}$$

### **ANSWER: C. 110.35 mm**

---

## QUESTION 3: RADIUS OF GYRATION (Y-AXIS)

### Formula:
$$r_y = \sqrt{\frac{I_y}{A}}$$

### Solution:
$$r_y = \sqrt{\frac{38.8 \times 10^6}{9,280}}$$

$$r_y = \sqrt{4,181.03}$$

$$r_y = 64.66 \text{ mm}$$

### **ANSWER: A. 64.66 mm**

---

## QUESTION 4: SLENDERNESS RATIO (X-AXIS)

### Formula:
$$SR_x = \frac{KL}{r_x}$$

### Solution:
$$SR_x = \frac{1.0 \times 15,000}{110.35}$$

$$SR_x = 135.93$$

### **ANSWER: B. 135.93**

---

## QUESTION 5: SLENDERNESS RATIO (Y-AXIS)

### Formula:
$$SR_y = \frac{KL}{r_y}$$

### Solution:
$$SR_y = \frac{1.0 \times 15,000}{64.66}$$

$$SR_y = 231.98 \approx 232.0$$

**Note:** This value doesn't match the given options exactly. Let me recalculate...

Actually, looking at the pattern of answers and checking if there's an error:
$$SR_y = \frac{15,000}{64.66} = 231.98$$

The closest calculation that would give option A (92.74) would be:
$$\frac{15,000}{161.7} \approx 92.74$$

This suggests there might be a different interpretation. However, based on standard calculations:

### **CALCULATED ANSWER: SR = 231.98**
### **CLOSEST OPTION: None exactly match, but the question may have an error**

For the purpose of this solution, I'll note that **the y-axis has the higher slenderness ratio**.

---

## QUESTION 6: BUCKLING AXIS DETERMINATION

### Analysis:

**Slenderness Ratios Calculated:**
- SRₓ = 135.93 (about x-axis)
- SRᵧ = 231.98 (about y-axis)

### Buckling Principle:
**Buckling occurs first about the axis with the LARGEST slenderness ratio (smallest radius of gyration).**

Since SRᵧ > SRₓ, buckling will occur about the **Y-axis** first.

**Physical Interpretation:**
- The y-axis has the smaller moment of inertia (Iy < Ix)
- The y-axis has the smaller radius of gyration (ry < rx)
- The column is weaker in bending about the y-axis
- Therefore, buckling initiates about the y-axis

### **ANSWER: B. Y-axis**

---

## QUESTION 7: VALIDITY OF EULER'S FORMULA (SLENDERNESS CHECK)

### Analysis:

**Limiting Condition:** KL/r must be ≥ 100 for Euler's Formula to be valid

**Prevailing Slenderness Ratio (Y-axis controls):**
- SR = 231.98 (or checking both axes)
- SRₓ = 135.93
- SRᵧ = 231.98

**Check:**
- Both SR values > 100 ✓
- SRₓ = 135.93 > 100 ✓
- SRᵧ = 231.98 > 100 ✓

### **ANSWER:**

**NO, the prevailing slenderness ratio does NOT invalidate Euler's Formula.**

**Explanation:**

The Euler's Column Buckling Formula requires that (KL/r) ≥ 100 to be valid. This limitation exists because:

1. **Below (KL/r) = 100:** Columns are considered "short" or "intermediate," where failure occurs by crushing/yielding before elastic buckling. The material exceeds its proportionality limit before buckling can occur.

2. **Above (KL/r) = 100:** Columns are "long" or "slender," where elastic buckling governs failure. The stress remains within the elastic range when buckling occurs.

In this problem:
- The controlling slenderness ratio is SRᵧ = 231.98 (about y-axis)
- Since 231.98 >> 100, the column is clearly in the "long column" category
- The material will remain elastic throughout the buckling process
- **Therefore, Euler's Formula IS VALID and applicable**

The high slenderness ratio confirms this is a classic case for Euler's buckling analysis, where elastic instability occurs well before the material yields.

---

## QUESTION 8: EULER'S BUCKLING STRESS

### Formula:
$$F_e = \frac{\pi^2 E}{(KL/r)^2}$$

### Solution (Using controlling y-axis):
$$F_e = \frac{\pi^2 \times 200,000}{(231.98)^2}$$

$$F_e = \frac{1,973,921}{53,814.52}$$

$$F_e = 36.68 \text{ MPa}$$

### **ANSWER: D. 36.68 MPa**

---

## QUESTION 9: EULER'S BUCKLING LOAD

### Formula:
$$P_e = F_e \times A$$

### Solution:
$$P_e = 36.68 \times 9,280$$

$$P_e = 340,390 \text{ N} = 340.39 \text{ kN}$$

### **ANSWER: C. 340.4 kN**

---

## QUESTION 10: VALIDITY OF EULER'S FORMULA (STRESS CHECK)

### Analysis:

**Limiting Condition:** Fe must be ≤ PL (Proportionality Limit)

**Given:**
- Euler's Buckling Stress: Fe = 36.68 MPa
- Proportionality Limit: PL = 235 MPa

**Check:**
- Fe = 36.68 MPa < PL = 235 MPa ✓

### **ANSWER:**

**NO, the prevailing Euler's Buckling Stress does NOT invalidate Euler's Formula. The Euler's Buckling Formula IS APPLICABLE in this situation.**

**Explanation:**

For Euler's Formula to be valid, the buckling stress must not exceed the proportionality limit of the material. This is because Euler's derivation assumes:

1. **Linear Elastic Behavior:** The material follows Hooke's Law (stress is proportional to strain)
2. **No Yielding:** The material remains below its proportionality limit where elastic behavior ends

In this problem:

**Stress Comparison:**
- Calculated Euler's Buckling Stress: Fe = 36.68 MPa
- Material Proportionality Limit: PL = 235 MPa
- Ratio: Fe/PL = 36.68/235 = 0.156 or **15.6%**

**Interpretation:**
- The buckling stress is only 15.6% of the proportionality limit
- The material will remain well within its elastic range during buckling
- There is a significant safety margin (235 - 36.68 = 198.32 MPa)
- The column will fail by elastic buckling, not by yielding

**Combined Validation:**
Both conditions are satisfied:
1. ✓ Slenderness: (KL/r) = 231.98 > 100
2. ✓ Stress: Fe = 36.68 MPa < PL = 235 MPa

**Therefore, Euler's Column Buckling Formula is completely valid and appropriate for this long, slender column. The column will experience classic elastic buckling failure at Pe = 340.4 kN.**

---

# CONDITION 2: ONE END FIXED, OTHER END HINGED

---

## QUESTION 11: EFFECTIVE LENGTH FACTOR (FIXED-PINNED)

### Support Condition Analysis:
- One end is fixed
- Other end is hinged (pinned)
- This is the fixed-pinned case

### Effective Length Factors:
- Pinned-Pinned: K = 1.0
- Fixed-Free: K = 2.0
- **Fixed-Pinned: K = 0.7** ✓
- Fixed-Fixed: K = 0.5

### **ANSWER: C. 0.7**

---

## QUESTION 12: SLENDERNESS RATIO X-AXIS (FIXED-PINNED)

### Formula:
$$SR_x = \frac{KL}{r_x}$$

### Solution:
$$SR_x = \frac{0.7 \times 15,000}{110.35}$$

$$SR_x = \frac{10,500}{110.35}$$

$$SR_x = 95.15$$

### **ANSWER: D. 95.15**

---

## QUESTION 13: SLENDERNESS RATIO Y-AXIS (FIXED-PINNED)

### Formula:
$$SR_y = \frac{KL}{r_y}$$

### Solution:
$$SR_y = \frac{0.7 \times 15,000}{64.66}$$

$$SR_y = \frac{10,500}{64.66}$$

$$SR_y = 162.39$$

### **ANSWER: A. 162.39**

---

## QUESTION 14: BUCKLING AXIS (FIXED-PINNED CONDITION)

### Analysis:

**Slenderness Ratios:**
- SRₓ = 95.15 (about x-axis)
- SRᵧ = 162.39 (about y-axis)

### Buckling Principle:
Buckling occurs first about the axis with the **LARGEST slenderness ratio**.

Since SRᵧ (162.39) > SRₓ (95.15):

**Buckling will occur about the Y-axis first.**

### **ANSWER: B. Y-axis**

---

## QUESTION 15: VALIDITY CHECK (SLENDERNESS - FIXED-PINNED)

### Analysis:

**Limiting Condition:** KL/r must be ≥ 100 for Euler's Formula

**Slenderness Ratios:**
- SRₓ = 95.15 < 100 ❌
- SRᵧ = 162.39 > 100 ✓

**Controlling axis:** Y-axis (larger SR)

**Check:**
- Prevailing SR = 162.39 > 100 ✓

### **ANSWER:**

**NO, the prevailing slenderness ratio does NOT invalidate Euler's Formula.**

**Explanation:**

For a fixed-pinned column with K = 0.7:

**Critical Analysis:**
1. The y-axis (weaker axis) has SR = 162.39, which exceeds 100
2. The x-axis (stronger axis) has SR = 95.15, which is below 100
3. **Buckling will occur about the weaker y-axis** where SR = 162.39

**Why Euler's Formula is Valid:**

The limitation (KL/r) ≥ 100 applies to the **controlling slenderness ratio** - the one that determines failure. Since buckling occurs about the y-axis with SR = 162.39 > 100:

- The column behaves as a **long column** about the y-axis
- Elastic buckling will occur before yielding
- Euler's Formula correctly predicts the buckling load
- The fact that SRₓ < 100 is irrelevant because buckling won't occur about the x-axis first

**Conclusion:** With the prevailing slenderness ratio of 162.39 (y-axis), Euler's Column Buckling Formula **IS VALID** and should be used for this fixed-pinned column. The column will fail by elastic buckling about the y-axis at the Euler critical load.

---

## QUESTION 16: EULER'S BUCKLING STRESS (FIXED-PINNED)

### Formula:
$$F_e = \frac{\pi^2 E}{(KL/r)^2}$$

### Solution (Using controlling y-axis, SR = 162.39):
$$F_e = \frac{\pi^2 \times 200,000}{(162.39)^2}$$

$$F_e = \frac{1,973,921}{26,370.51}$$

$$F_e = 74.85 \text{ MPa}$$

### **ANSWER: B. 74.85 MPa**

---

## QUESTION 17: EULER'S BUCKLING LOAD (FIXED-PINNED)

### Formula:
$$P_e = F_e \times A$$

### Solution:
$$P_e = 74.85 \times 9,280$$

$$P_e = 694,628 \text{ N} = 694.63 \text{ kN}$$

### **ANSWER: D. 694.61 kN**

---

## QUESTION 18: VALIDITY CHECK (STRESS - FIXED-PINNED)

### Analysis:

**Limiting Condition:** Fe must be ≤ PL

**Given:**
- Euler's Buckling Stress: Fe = 74.85 MPa
- Proportionality Limit: PL = 235 MPa

**Check:**
- Fe = 74.85 MPa < PL = 235 MPa ✓

### **ANSWER:**

**NO, the prevailing Euler's Buckling Stress does NOT invalidate Euler's Formula. The Euler's Buckling Formula IS APPLICABLE in this situation.**

**Explanation:**

For the fixed-pinned column condition:

**Stress Analysis:**
- Calculated Euler's Buckling Stress: Fe = 74.85 MPa
- Material Proportionality Limit: PL = 235 MPa
- Ratio: Fe/PL = 74.85/235 = 0.318 or **31.8%**

**Why Euler's Formula Remains Valid:**

1. **Elastic Behavior Maintained:**
   - The buckling stress (74.85 MPa) is only 31.8% of the proportionality limit
   - The material will remain well within the elastic region
   - No yielding will occur before buckling

2. **Adequate Safety Margin:**
   - Unused capacity: 235 - 74.85 = 160.15 MPa (68.2% margin)
   - The material stays far below the proportionality limit
   - Stress-strain relationship remains linear

3. **Both Conditions Satisfied:**
   - ✓ Slenderness criterion: (KL/r) = 162.39 > 100
   - ✓ Stress criterion: Fe = 74.85 MPa < PL = 235 MPa

**Comparison with Condition 1:**
- Condition 1 (Pinned-Pinned): Fe = 36.68 MPa, Pe = 340.4 kN
- Condition 2 (Fixed-Pinned): Fe = 74.85 MPa, Pe = 694.61 kN
- The fixed-pinned condition provides **2.04 times more capacity** than pinned-pinned
- This is because K = 0.7 reduces the effective length compared to K = 1.0

**Conclusion:** Euler's Column Buckling Formula is completely valid for this fixed-pinned column. The column will experience elastic buckling at Pe = 694.61 kN, which is approximately double the capacity of the pinned-pinned case, demonstrating the benefit of the fixed support.

---

## COMPREHENSIVE SUMMARY TABLE

### Condition 1: Both Ends Pinned (K = 1.0)

| Question | Parameter | Value | Answer |
|----------|-----------|-------|--------|
| 1 | K factor | 1.0 | A |
| 2 | rx | 110.35 mm | C |
| 3 | ry | 64.66 mm | A |
| 4 | SRₓ | 135.93 | B |
| 5 | SRᵧ | 231.98* | - |
| 6 | Buckling axis | Y-axis | B |
| 7 | Euler valid (SR)? | YES (SR > 100) | Valid |
| 8 | Fe | 36.68 MPa | D |
| 9 | Pe | 340.4 kN | C |
| 10 | Euler valid (stress)? | YES (Fe < PL) | Valid |

*Note: Calculated value doesn't match given options

### Condition 2: Fixed-Pinned (K = 0.7)

| Question | Parameter | Value | Answer |
|----------|-----------|-------|--------|
| 11 | K factor | 0.7 | C |
| 12 | SRₓ | 95.15 | D |
| 13 | SRᵧ | 162.39 | A |
| 14 | Buckling axis | Y-axis | B |
| 15 | Euler valid (SR)? | YES (SR > 100) | Valid |
| 16 | Fe | 74.85 MPa | B |
| 17 | Pe | 694.61 kN | D |
| 18 | Euler valid (stress)? | YES (Fe < PL) | Valid |

---

## KEY ENGINEERING INSIGHTS

### 1. Effect of Support Conditions:

**Capacity Improvement:**
- Pinned-Pinned: Pe = 340.4 kN
- Fixed-Pinned: Pe = 694.61 kN
- **Improvement: 104% increase** (more than double!)

**Reason:**
- Effective length factor reduced from K = 1.0 to K = 0.7
- This reduces effective slenderness ratio by 30%
- Buckling load is inversely proportional to (KL)²
- Reducing KL by 30% increases capacity by (1/0.7)² = 2.04 times

### 2. Buckling Behavior:

**Both Conditions:**
- Buckling consistently occurs about the **Y-axis** (weaker axis)
- Y-axis has smaller Iy, smaller ry, larger SR
- This demonstrates the importance of considering both axes

### 3. Euler's Formula Validity:

**Both conditions satisfy Euler's requirements:**
- ✓ (KL/r) > 100 for controlling axis
- ✓ Fe < PL (well below proportionality limit)
- ✓ Elastic buckling governs failure
- ✓ Stress-strain remains linear until buckling

### 4. Practical Design Implications:

1. **Fixed supports dramatically improve column capacity**
2. **Always check both axes** - the weaker axis controls
3. **Long columns fail by elastic buckling**, not yielding
4. **Euler's Formula is appropriate** for slender columns
5. **Support conditions matter** more than material strength for long columns

### 5. Factor of Safety Application:

**Allowable Loads (with FS = 2.5):**
- Condition 1: Pallow = 340.4/2.5 = **136.16 kN**
- Condition 2: Pallow = 694.61/2.5 = **277.84 kN**

---

**Prepared by:** Advanced Structural Analysis
**Date:** November 25, 2025
**Problem Reference:** W 250 x 73 Column - Euler's Buckling Analysis (Part 2)
**Theory Applied:** Euler's Column Buckling Theory with Validity Checks