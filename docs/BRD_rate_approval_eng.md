# Business Requirements Document

## 1. Introduction

In the current logistics and business model of "88 LOGISTICS" LLC, all freight rate confirmations from carriers and clients (cargo owners) are handled through messengers (Viber, Telegram) and/or email. The unstructured nature of this process leads to delays in confirming rates and signing service agreements, information loss, and misunderstandings among managers within the company. As a result, this contributes to client attrition and, at times, to additional costs.

This project aims to improve and automate the rate approval process through a structured system of business requirements and rules.

### Current performance metrics:

| **Period**       | **Client Requests** | **Avg. Carrier Rate Approval Time per Order** | **Successful Deals** | **Conversion Rate** |
|:----------------:|:-------------------:|:---------------------------------------------:|:---------------------:|:--------------------:|
| December 2022    | 492                 | 3h 12m                                        | 37                   | 7.5%                 |
| January 2023     | 255                 | 4h 56m                                        | 18                   | 7%                   |
| February 2023    | 306                 | 3h 45m                                        | 15                   | 4.2%                 |
| March 2023       | 339                 | 4h 21m                                        | 24                   | 7%                   |
| April 2023       | 418                 | 4h 59m                                        | 33                   | 7.9%                 |

---

## 2. Business Objectives

The new system is intended to achieve the following business objectives:

| Objective                                       | Success Metric                                 |
|------------------------------------------------|------------------------------------------------|
| Reduce average carrier rate approval time to under 30 minutes | Report from ERP/CRM system                     |
| Automate ≥70% of rate approvals               | % of requests auto-processed in ERP/CRM report |
| Increase decision-making speed by 50%         | Time from request to decision                  |

---

## 3. Scope

### **In Scope:**
- Development of a structured business process
- Interface for reviewing and approving carrier rate offers

### **Out of Scope:**
- Changes to commercial terms with clients or carriers

---

## 4. Stakeholders

List of all involved stakeholders:

| Role              | Title                          | Interest                                       |
|-------------------|---------------------------------|------------------------------------------------|
| Sponsor           | Head of Logistics Department    | Receive an efficient and structured system     |
| Primary User      | Logistics Manager               | Optimize daily operational workload            |
| Analyst           | Business Analyst                | Formulate clear requirements                   |
| Developer         | IT Specialist                   | Implement the specified functional requirements|

---

## 5. High-Level Business Requirements

| ID    | Requirement                                    | Priority |
|-------|------------------------------------------------|----------|
| BR-01 | The system must automatically process rate offers | High     |
| BR-02 | The user must be able to manually review rates     | Medium   |
| BR-03 | All decisions must be logged for future reference | High     |

---

## 6. Expected Benefits

By implementing this set of business requirements, the company expects to achieve the following:

- Reduction of rate confirmation time by 3–4 hours per request
- Estimated savings of up to €4,500 per month through successfully closed deals enabled by faster processing
- A more transparent and controlled approval process with minimized human error

---

## 7. Constraints / Risks

| ID   | Risk Description                              | Likelihood | Potential Impact               |
|------|-----------------------------------------------|------------|--------------------------------|
| R-01 | Incomplete or inaccurate historical rate data | Medium     | Reduced accuracy of automation |
| R-02 | Low adoption of the new system by logistics staff | High    | Implementation slowdown        |

