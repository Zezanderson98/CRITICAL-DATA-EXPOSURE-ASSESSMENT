# Mediroza General Hospital
# Penetration Testing Report

## Milestone 3 – Critical Data Exposure Assessment

---

# Executive Summary

During the Application Mapping and Reconnaissance phase of the engagement, extensive enumeration activities were performed to identify exposed resources, hidden application content, and potential attack surfaces within the Mediroza General Hospital environment.

This process resulted in the discovery of references to sensitive organizational records that appeared unrelated to normal hospital operations and publicly accessible functionality. Preliminary validation was performed during the Initial Access and Authentication Assessment phase, where evidence suggested the existence of confidential corporate and business records accessible through exposed resources.

As the primary objectives of the earlier milestones focused on obtaining and analyzing protected patient records, the discovery was documented for further investigation at a later stage of the assessment.

During Milestone 3, a dedicated investigation was conducted to determine the full extent of the exposure and assess the associated business impact. Analysis confirmed unauthorized access to highly sensitive organizational information, including employee salary records, staffing information, shareholder ownership details, and equity distribution data.

The exposed information provided detailed insight into both internal personnel records and corporate ownership structures. Such information would typically be restricted to executive management, finance personnel, and authorized stakeholders.

The ability to access these datasets without appropriate authorization represents a critical breakdown in confidentiality controls and exposes the organization to significant financial, operational, regulatory, and reputational risk.

Based on the nature and sensitivity of the exposed information, this finding has been assigned a **Critical** severity rating.

---

# Engagement Information

| Item | Description |
|----------|----------|
| Client | Mediroza General Hospital |
| Assessment Type | Black-Box Penetration Test |
| Milestone | M3 – Critical Data Exposure |
| Risk Category | Sensitive Information Disclosure |
| Severity | Critical |
| Status | Confirmed |

---

# Objective

The objective of this phase was to investigate sensitive resources identified during earlier stages of the engagement, validate the existence of unauthorized information disclosure, and assess the business impact associated with any exposed organizational data.

---

# Finding MED-003

## Critical Exposure of Internal Corporate and Employee Records

### Severity

**CRITICAL**

### Risk Rating

**CRITICAL**

### CWE Classification

**CWE-200 – Exposure of Sensitive Information to an Unauthorized Actor**

---

# Description

During reconnaissance and application mapping activities, sensitive resources containing internal organizational information were discovered.

Subsequent investigation confirmed that these resources exposed confidential corporate and employee data that should not have been accessible through externally discoverable locations.

The exposure included:

- Employee salary records
- Staff employment information
- Departmental staffing data
- Shareholder ownership records
- Equity allocation information
- Corporate governance information

The exposed datasets were accessible without appropriate authorization controls and represented a significant failure in the protection of business-critical information.

---

# Attack Narrative

## Phase 1 – Reconnaissance and Application Mapping

Application mapping activities were conducted to identify publicly accessible resources, hidden files, application endpoints, and sensitive content exposed within the target environment.

During this process, references to internal organizational records were identified. Initial review suggested the presence of confidential shareholder information and non-public business records.

The information was documented and earmarked for further validation during later assessment phases.

---

## Phase 2 – Initial Validation

During the Initial Access and Authentication Assessment phase, limited validation was performed against the identified resources.

This review confirmed that the exposed records appeared to contain legitimate organizational information. However, detailed analysis was deferred in order to prioritize the objectives associated with patient record acquisition and password recovery.

The discovery remained a significant indicator of potential data exposure and was scheduled for comprehensive investigation during Milestone 3.

---

## Phase 3 – Exposure Assessment

A dedicated analysis of the identified resources was conducted.

The investigation confirmed unauthorized access to sensitive internal datasets containing employee salary information and shareholder ownership records.

The exposed information could be accessed after discovering the affected resources and did not require privileged administrative access to retrieve.

Review of the recovered records confirmed the authenticity and sensitivity of the information exposed.

---

# Technical Evidence

## Evidence A – Employee Salary Records

### Description

The exposed dataset contained detailed employee records including names, positions, departments, annual compensation values, and employment information.

### Sample Recovered Records

| Employee | Position | Department | Annual Salary |
|------------|------------|------------|------------|
| Dr. Suresh Moodley | Consultant Radiologist | Radiology | $130,000 |
| Dr. Vikram Chetty | Anaesthetist | Theatre | $135,000 |
| Dr. Fatima Patel | Pediatrician | Pediatrics | $118,000 |
| David Smith | Facilities Manager | Operations | $52,000 |
| Nisha Singh | Physiotherapist | Rehabilitation | $48,000 |
| Radebe | Radiographer | Radiology | $43,000 |
| Deepak Pillay | Lab Technologist | Diagnostics Lab | $41,000 |
| Peter van Wyk | Procurement Officer | Supply Chain | $38,000 |
| Kavitha Govender | Lab Technician | Diagnostics Lab | $35,000 |
| Karen O'Connor | Billing Administrator | Finance | $29,000 |
| James Wilson | Security Supervisor | Operations | $27,000 |
| Andile Mbeki | Ward Clerk | Administration | $21,000 |
| Linda Fourie | Receptionist | Front Office | $19,000 |


---

### Security Impact

Disclosure of employee compensation records may facilitate:

- Targeted social engineering attacks
- Internal employee disputes
- Privacy violations
- Financial profiling
- Spear-phishing campaigns
- Reputational damage

---

## Evidence B – Shareholder Ownership Records

### Description

Further investigation revealed access to internal shareholder records detailing ownership percentages, allocated shares, and share classifications.

### Recovered Shareholder Information

| Shareholder | Ownership % | Shares Held | Share Class |
|-------------|-------------|-------------|-------------|
| Dr. Rajesh Naidoo | 18.0% | 180,000 | Ordinary |
| Cedar Health Holdings (Pty) Ltd | 15.0% | 150,000 | Ordinary |
| Dr. Johan van der Merwe | 12.0% | 120,000 | Ordinary |
| Reddy Family Trust | 11.0% | 110,000 | Ordinary |
| Thabo Molefe | 10.0% | 100,000 | Ordinary |
| Sarah Botha | 9.0% | 90,000 | Ordinary |
| Dr. Ahmed Kara | 8.0% | 80,000 | Preferential |
| Naledi Zulu | 7.0% | 70,000 | Ordinary |
| Michael Roberts | 6.0% | 60,000 | Ordinary |
| Dr. Vikram Chetty | 4.0% | 40,000 | Preferential |


---

### Security Impact

Exposure of shareholder information enables unauthorized parties to obtain intelligence regarding:

- Corporate ownership structures
- Investor relationships
- Strategic business interests
- Financial influence
- Governance arrangements

This information is highly sensitive and should not be publicly accessible.

---

# Business Impact Assessment

The exposed information extends far beyond patient confidentiality concerns and affects critical business operations.

## Employee Data Impact

Exposure of employee compensation records may result in:

- Internal workplace conflict
- Loss of employee trust
- Targeted fraud attempts
- Privacy complaints
- Increased social engineering risk

---

## Corporate Data Impact

Exposure of shareholder information may result in:

- Unauthorized corporate intelligence gathering
- Investor targeting
- Competitive disadvantage
- Confidentiality concerns
- Reputational harm

---

## Regulatory Impact

Exposure of employee information may create compliance obligations under applicable privacy and employment regulations.

The organization may also face legal and contractual obligations related to the protection of confidential corporate information.

---

# Root Cause

The assessment identified sensitive business information accessible through discoverable resources identified during application mapping activities.

The exposure indicates deficiencies in:

- Access control implementation
- Sensitive data segregation
- Information classification controls
- Protection of business-critical assets

These weaknesses enabled unauthorized access to organizational records that should have been restricted to authorized personnel.

---

# Risk Assessment

| Metric | Rating |
|----------|----------|
| Likelihood | High |
| Confidentiality Impact | Critical |
| Integrity Impact | Low |
| Availability Impact | None |
| Ease of Discovery | Medium |
| Business Impact | Critical |
| Overall Severity | Critical |

---

# Recommendations

## Immediate Actions

1. Remove public access to exposed datasets immediately.
2. Restrict access to employee and shareholder records.
3. Review permissions associated with affected resources.
4. Validate all exposed storage locations for additional sensitive information.

---

## Short-Term Improvements

1. Conduct a complete audit of publicly accessible resources.
2. Implement least-privilege access controls.
3. Classify and inventory sensitive business information.
4. Restrict direct access to internal records.

---

## Long-Term Improvements

1. Implement centralized document governance controls.
2. Establish formal data classification procedures.
3. Deploy continuous monitoring for sensitive information exposure.
4. Conduct periodic penetration testing and exposure assessments.
5. Implement data loss prevention (DLP) technologies.

---

# Conclusion

A critical information disclosure vulnerability was identified during the assessment.

Resources discovered during application mapping activities exposed highly sensitive organizational information that remained accessible throughout subsequent phases of testing.

The exposure resulted in unauthorized access to employee salary records, staffing information, shareholder ownership data, and corporate governance information.

Given the sensitivity of the recovered information and the potential business impact associated with unauthorized disclosure, this finding has been assigned a **Critical** severity rating and should be remediated as a priority.

---

# Assessment Outcome

| Objective | Status |
|------------|------------|
| Identify Additional Sensitive Resources | ✅ Complete |
| Validate Information Exposure | ✅ Complete |
| Recover Employee Salary Information | ✅ Complete |
| Recover Shareholder Information | ✅ Complete |
| Assess Business Impact | ✅ Complete |
| Collect Supporting Evidence | ✅ Complete |
| Complete Milestone 3 | ✅ Complete |

---

**Pentester:** Your Name  
**Client:** Mediroza General Hospital  
**Assessment Type:** Black-Box Penetration Test  
**Milestone:** M3 – Critical Data Exposure Assessment  
**Finding ID:** MED-003
