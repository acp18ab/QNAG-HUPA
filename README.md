# QNAG-HUPA: External Validation of ACTIVE-GLU on the HUPA-UCM Dataset

## Overview
This repository contains the external validation results of the **ACTIVE-GLU** 
personalised blood glucose prediction framework applied to the independent 
**HUPA-UCM diabetes dataset**. The validation was conducted to assess the 
generalisability of ACTIVE-GLU beyond the original study cohort.

## Related Paper
**ACTIVE-GLU: Personalised Modelling of Physical Activity-Driven Glucose 
Dynamics in Type 1 Diabetes under Free-Living Conditions**  
Ahmad Bilal, Hood Thabit, Paul W. Nutter, Simon Harper  
*Journal Title* (2025) — Under Review

## External Dataset
**HUPA-UCM Diabetes Dataset**  
Hidalgo et al., *Data in Brief*, 2024  
- 25 participants with T1DM  
- Abbott FreeStyle Libre 2 CGM (15-min intervals)  
- Fitbit Ionic smartwatch (steps, heart rate)  
- Free-living conditions, Hospital Príncipe de Asturias, Spain  
- Dataset: https://data.mendeley.com/datasets/3hbcscwz44/1

## Validation Summary
Of 25 HUPA-UCM participants, **10 met the minimum data requirements** 
(≥10 consecutive days of synchronised PA and BG data) to apply the 
ACTIVE-GLU rolling-window framework.

| PA Level  | Accuracy (%) | MAE (mmol/L) | RMSE (mmol/L) |
|-----------|-------------|--------------|---------------|
| Low       | 81.55       | 0.27         | 0.34          |
| Medium    | 81.72       | 0.29         | 0.34          |
| High      | 83.33       | 0.33         | 0.40          |
| Very High | 81.64       | 0.29         | 0.36          |

ACTIVE-GLU maintained >81% accuracy across all PA intensity levels on 
this fully independent dataset, without any retraining or parameter modification.

## Key Notes
- Composite PA score adapted from `steps × maxMotion` (original) 
  to `steps × heart rate` (HUPA), as Fitbit does not expose 
  epoch-level peak acceleration
- All other pipeline parameters identical to the primary study
- Validation conducted in accordance with the original ACTIVE-GLU methodology

## Contact
**Ahmad Bilal**  
University of Manchester, Department of Computer Science  
ahmad.bilal@manchester.ac.uk
ahmad-bilals@hotmail.com
