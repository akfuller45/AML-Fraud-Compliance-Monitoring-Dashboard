# AML-Fraud-Compliance-Monitoring-Dashboard

# AML & Fraud Compliance Monitoring Dashboard

## Executive Summary

This project simulates an enterprise AML and fraud compliance monitoring framework using a financial transaction dataset. The goal of the project is to evaluate transaction activity, identify suspicious behavior, assess fraud detection gaps, and create executive-level compliance reporting.

The project was designed from the perspective of a regulatory compliance, fraud monitoring, or financial crimes analyst. Rather than focusing only on prediction, this project emphasizes governance, risk, compliance controls, alert management, fraud detection effectiveness, and audit readiness.

---

## Business Problem

Financial institutions must monitor transaction activity to detect fraud, suspicious activity, money movement risk, and potential AML concerns. Weak transaction monitoring controls can result in missed fraud, delayed investigations, regulatory exposure, financial loss, and reputational damage.

This project builds a simulated compliance monitoring system that identifies high-risk transactions, flags suspicious activity, evaluates fraud detection performance, and routes alerts for review.

---

## Project Objectives

The objectives of this project are to:

- Identify high-risk transaction activity
- Classify transactions by AML and fraud compliance risk
- Detect full-balance drains and high-value transactions
- Evaluate fraud detection control effectiveness
- Identify missed fraud transactions
- Create an AML/fraud alert register
- Build a suspicious activity review candidate register
- Develop a fraud detection gap analysis
- Create an AML compliance risk matrix
- Build an executive compliance dashboard
- Produce audit-ready monitoring outputs

---

## Dataset Overview

The dataset contains simulated financial transaction activity with the following key fields:

| Field | Description |
|---|---|
| `step` | Time step of the transaction |
| `type` | Transaction type |
| `amount` | Transaction amount |
| `nameOrig` | Origin account |
| `oldbalanceOrg` | Origin account balance before transaction |
| `newbalanceOrig` | Origin account balance after transaction |
| `nameDest` | Destination account |
| `oldbalanceDest` | Destination account balance before transaction |
| `newbalanceDest` | Destination account balance after transaction |
| `isFraud` | Actual fraud indicator |
| `isFlaggedFraud` | System-generated fraud flag |

---

## Methodology

The project follows an enterprise compliance monitoring workflow:

1. Load and inspect transaction data
2. Profile data quality and missing values
3. Create AML and fraud risk flags
4. Develop transaction risk scoring logic
5. Classify transactions into compliance risk levels
6. Perform automated control testing
7. Create an AML/fraud alert register
8. Analyze fraud detection gaps
9. Build a suspicious activity review candidate register
10. Create an AML compliance risk matrix
11. Build an executive monitoring dashboard
12. Export audit-ready tables and dashboard visuals

---

## AML and Fraud Risk Indicators

The project evaluates several transaction risk indicators:

| Risk Indicator | Purpose |
|---|---|
| High-Value Transaction Flag | Identifies unusually large transactions |
| Very High-Value Transaction Flag | Identifies transactions in the highest-value range |
| Full-Balance Drain Flag | Identifies transactions that reduce the origin balance to zero |
| Origin Balance Inconsistency | Detects balance movement irregularities from the origin account |
| Destination Balance Inconsistency | Detects balance movement irregularities from the destination account |
| High-Risk Transaction Type | Flags transfer and cash-out activity for enhanced review |
| Fraud Flag | Identifies confirmed fraudulent transactions |
| System Fraud Flag | Identifies transactions flagged by the monitoring system |

---

## Compliance Risk Scoring

Each transaction was assigned a compliance risk score based on multiple monitoring indicators.

Risk points were assigned for:

- high-value transaction activity
- very high-value transaction activity
- full-balance drains
- origin balance inconsistencies
- destination balance inconsistencies
- high-risk transaction types
- fraud indicators
- system monitoring flags

Transactions were then classified into the following compliance risk levels:

| Risk Level | Description |
|---|---|
| Low | Minimal compliance concern |
| Medium | Moderate monitoring concern |
| High | Elevated risk requiring review |
| Critical | Severe risk requiring escalation |

---

## Automated Compliance Control Testing

The project includes an automated control testing summary to evaluate whether key transaction monitoring fields are complete and valid.

Controls tested include:

| Control ID | Control Name |
|---|---|
| CTRL-001 | Transaction Type Present |
| CTRL-002 | Positive Transaction Amount |
| CTRL-003 | Origin Account Present |
| CTRL-004 | Destination Account Present |
| CTRL-005 | Origin Balance Fields Present |
| CTRL-006 | Destination Balance Fields Present |
| CTRL-007 | Fraud Label Present |
| CTRL-008 | System Fraud Flag Present |

Each control was evaluated using:

- total records tested
- records passed
- records failed
- pass rate
- control effectiveness rating

---

## AML/Fraud Alert Register

An alert register was created to simulate an enterprise compliance review workflow.

Transactions were routed into the alert register when they met one or more high-risk criteria, including:

- actual fraud
- system fraud flag
- high or critical compliance risk
- very high transaction value
- full-balance drain
- balance inconsistencies
- high-risk transaction type

Each alert was assigned:

- alert type
- alert priority
- alert owner
- alert status
- recommended review action

This mirrors how AML and fraud compliance teams route suspicious activity for investigation and escalation.

---

## Fraud Detection Gap Analysis

A fraud detection gap analysis was performed by comparing actual fraud transactions against system-generated fraud flags.

Each transaction was classified into one of four monitoring outcomes:

| Outcome | Description |
|---|---|
| True Positive | Actual fraud correctly flagged by the system |
| Missed Fraud | Actual fraud not flagged by the system |
| False Positive | Non-fraud transaction incorrectly flagged by the system |
| True Negative | Non-fraud transaction correctly not flagged |

The analysis calculated:

- actual fraud rate
- system flag rate
- detection rate
- missed fraud rate
- false positive rate
- missed fraud exposure
- missed fraud exposure by transaction type

Missed fraud transactions represent potential monitoring control gaps because fraudulent activity occurred without system escalation.

---

## AML/Fraud Compliance Risk Matrix

An AML compliance risk matrix was developed using impact and likelihood scoring.

| Score Component | Description |
|---|---|
| Impact Score | Based on transaction amount and high-value activity |
| Likelihood Score | Based on transaction type, balance drain activity, and balance inconsistencies |
| Matrix Score | Impact Score multiplied by Likelihood Score |

Transactions were classified into matrix risk levels:

- Low
- Medium
- High
- Critical

This matrix supports compliance prioritization, suspicious activity review, and executive risk reporting.

---

## Suspicious Activity Review Candidate Register

A suspicious activity review candidate register was created to identify transactions requiring enhanced compliance review.

Transactions were included when they met criteria such as:

- actual fraud
- critical alert priority
- high or critical AML matrix classification
- elevated compliance risk score
- suspicious transaction behavior

This register simulates how AML teams may prioritize transactions for additional investigation or potential regulatory review.

---

## Executive Dashboard

The executive dashboard provides a consolidated view of AML and fraud monitoring performance.

Dashboard components include:

- total transactions
- total fraud transactions
- system-flagged transactions
- missed fraud transactions
- fraud detection rate
- missed fraud exposure
- critical alerts
- suspicious activity review candidates
- fraud detection outcome summary
- AML/fraud compliance risk matrix
- alert priority distribution
- top alert types
- alert ownership by compliance function
- missed fraud exposure by transaction type
- failed compliance monitoring controls

![AML Fraud Compliance Dashboard](outputs/charts/aml_fraud_compliance_dashboard_clean.png)

---

## Key Findings

### Finding 1 — Low System Fraud Detection Rate

The fraud detection gap analysis identified actual fraudulent transactions that were not flagged by the system. These missed fraud transactions represent potential monitoring control weaknesses and may require rule enhancement, threshold recalibration, or additional fraud typology review.

### Finding 2 — Missed Fraud Exposure

Missed fraud transactions created significant financial exposure. This indicates that confirmed fraudulent activity bypassed system escalation and may not have been reviewed in a timely manner.

### Finding 3 — High-Risk Transaction Types

Transfer and cash-out transactions represented elevated risk categories. These transaction types were heavily associated with suspicious movement patterns, full-balance drains, and fraud exposure.

### Finding 4 — Alert Ownership Concentration

A large portion of alerts were routed to financial crime monitoring and AML review teams. This may indicate workload concentration and the need for alert prioritization or additional investigation resources.

### Finding 5 — Compliance Control Testing Results

Automated control testing identified whether required transaction monitoring fields were complete and suitable for compliance review. Failed control counts highlight areas where data quality or monitoring readiness may require improvement.

---

## Recommendations

### Fraud Monitoring Improvements

- Enhance fraud detection rules for transfer and cash-out transactions
- Review missed fraud patterns and update monitoring thresholds
- Add additional alert triggers for full-balance drain behavior
- Perform recurring monitoring rule effectiveness reviews

### AML Compliance Improvements

- Prioritize high and critical alert investigations
- Maintain a suspicious activity candidate register
- Create escalation workflows for critical transactions
- Monitor high-value and very high-value transactions more closely

### Governance Improvements

- Continue automated control testing
- Track monitoring rule effectiveness over time
- Assign alert ownership by compliance function
- Maintain audit-ready alert and remediation registers

### Audit Readiness Improvements

- Export alert registers for compliance review
- Document fraud detection gaps and remediation actions
- Maintain evidence of monitoring rule reviews
- Create formal audit findings for missed fraud exposure

---

## Project Outputs

The project produces the following outputs:

| Output | Description |
|---|---|
| `aml_fraud_alert_register.csv` | Full register of triggered AML/fraud alerts |
| `missed_fraud_register.csv` | Transactions where actual fraud was not system-flagged |
| `fraud_detection_gap_summary.csv` | Summary of fraud monitoring performance |
| `sar_candidate_register.csv` | Suspicious activity review candidates |
| `monitoring_rule_effectiveness.csv` | Effectiveness of monitoring rules |
| `aml_audit_finding.csv` | Simulated audit finding for fraud monitoring gap |
| `aml_fraud_compliance_dashboard_clean.png` | Executive dashboard visual |

---

## Technology Stack

- Python
- pandas
- numpy
- matplotlib
- Jupyter Notebook
- CSV data processing
- GitHub

---

## Project Structure

```text
aml-fraud-compliance-monitoring-dashboard/

│
├── data/
│   ├── raw/
│   ├── cleaned/
│
├── notebooks/
│   └── aml_fraud_compliance_monitoring.ipynb
│
├── outputs/
│   ├── charts/
│   │   └── aml_fraud_compliance_dashboard_clean.png
│   ├── tables/
│   │   ├── aml_fraud_alert_register.csv
│   │   ├── missed_fraud_register.csv
│   │   ├── fraud_detection_gap_summary.csv
│   │   ├── sar_candidate_register.csv
│   │   ├── monitoring_rule_effectiveness.csv
│   │   └── aml_audit_finding.csv
│   └── reports/
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

## Portfolio Value

This project demonstrates skills relevant to:

- AML compliance monitoring
- fraud risk analytics
- transaction monitoring
- regulatory compliance reporting
- operational risk analysis
- control testing
- audit readiness
- suspicious activity review
- governance reporting
- executive dashboarding

---

## Future Enhancements

Potential future improvements include:

- Power BI interactive dashboard
- fraud typology segmentation
- machine learning fraud detection model
- alert aging and SLA tracking
- remediation tracker
- case management workflow simulation
- transaction network analysis
- customer-level repeat activity monitoring
- automated PDF executive report

---

## Author

Amiranda Fuller

Governance Analytics | AML Compliance | Fraud Risk Monitoring | Data Governance | Business Intelligence
