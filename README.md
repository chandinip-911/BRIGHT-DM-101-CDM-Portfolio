# BRIGHT-DM-101-CDM-Portfolio
Clinical Data Management portfolio project using a simulated Type 2 Diabetes clinical trial.

# 1. CLINICAL TRIAL STUDY SYNOPSIS

## Study Identification

Study ID: BRIGHT-DM-101

Study Title: A Simulated Phase II Study to Evaluate the Efficacy and Safety of Study Drug X Compared with Placebo in Adults with Type 2 Diabetes Mellitus.

Therapeutic Area: Endocrinology / Diabetes

Study Phase: Phase II

Study Duration: 12 Weeks

Number of Participants: 12 (fictional)

## 2. Study Objectives

### Primary Objective
To evaluate the effect of Study Drug X on change in HbA1c from baseline to Week 12.

### Secondary Objectives
- Evaluate changes in fasting blood glucose.
- Review changes in body weight.
- Assess the occurrence of adverse events.
- Evaluate the safety and tolerability of Study Drug X.

## 3. Study Design

Study Type: Interventional

Design: Randomized, placebo-controlled, parallel-group simulation.

Treatment Groups:
- Group A: Study Drug X
- Group B: Placebo

Allocation: 1:1

## 4. Study Population

Adults diagnosed with Type 2 Diabetes Mellitus.

### Inclusion Criteria
- Age 18–65 years.
- Documented diagnosis of Type 2 Diabetes Mellitus.
- Able to provide informed consent.

### Exclusion Criteria
- Type 1 Diabetes Mellitus.
- Pregnancy.
- Serious uncontrolled medical conditions.
- Participation in another clinical trial.

## 5. Study Visit Schedule

- Visit 1: Screening
- Visit 2: Baseline / Randomization
- Visit 3: Week 4
- Visit 4: Week 8
- Visit 5: Week 12 / End of Study

## 6. Clinical Data to Be Collected

- Demographics
- Medical history
- Diabetes history
- Concomitant medications
- Vital signs
- Laboratory investigations
- Adverse events
- Treatment compliance
- Study completion status

## 7. Primary Endpoint

Change in HbA1c (%) from baseline to Week 12.

## 8. Secondary Endpoints

- Change in fasting blood glucose.
- Change in body weight.
- Number and type of adverse events.

## 9. Clinical Data Management Activities

- CRF development
- Data dictionary preparation
- Data entry and review
- Edit check development
- Data discrepancy identification
- Query generation and resolution
- SAE and laboratory reconciliation
- Data cleaning
- Database lock readiness

## 10. Project Disclaimer

This is a fictional educational CDM portfolio project. All study details and participant data are simulated. This is not an actual clinical trial.


# 2. CRF DESIGN

## CRF 01 – DEMOGRAPHICS FORM

### Purpose
To collect basic demographic information of participants enrolled in the BRIGHT-DM-101 simulated clinical trial.

### Form Details
- Form Name: Demographics
- Form ID: DEMO
- Form Type: Non-repeating
- Data Collection: Screening / Baseline

### CRF Fields

| Field Label | Variable Name | Data Type |
|---|---|---|
| Participant ID | SUBJID | Text |
| Screening Number | SCREENID | Text |
| Age | AGE | Integer |
| Sex | SEX | Coded choice |
| Visit Name | VISIT | Coded choice |
| Assessment Date | ASSESSDT | Date |

### Response Options

SEX:
- 1 = Male
- 2 = Female
- 3 = Other / Not specified, if permitted by the protocol

VISIT:
- 1 = Screening
- 2 = Baseline

### Data Entry Instructions
1. Enter the assigned participant ID.
2. Enter the screening number.
3. Record age in completed years.
4. Select the appropriate sex category.
5. Select the applicable study visit.
6. Record the assessment date.

### Data Quality Considerations
- Participant ID must not be blank.
- Age must be between 18 and 65 years.
- Screening number must be unique.
- Assessment date must be a valid date.
- Visit must be selected from the permitted options.

### Important Note
All participant details in this project are fictional and intended only for educational practice.


### Field-Level Specifications

| Variable | Required? | Allowed Values | Edit Check |
|---|---|---|---|
| SUBJID | Yes | BR001 to BR012 | Must be unique |
| SCREENID | Yes | SCR001 to SCR012 | Must be unique |
| AGE | Yes | Integer 18–65 | Reject values below 18 or above 65 |
| SEX | Yes | Protocol-defined categories | Must be an allowed value |
| VISIT | Yes | Screening, Baseline | Must be an allowed visit |
| ASSESSDT | Yes | Valid date | Must not be a future date |

### Form Design Notes
- Each participant must have a unique participant ID.
- Demographics should be collected at the Screening visit.
- Baseline information should be reviewed before randomization.
- All required fields must be completed or have an appropriate documented missing-data status.
- Any correction must maintain an audit trail in an actual EDC system.
