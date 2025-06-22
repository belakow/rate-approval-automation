## 1. Introduction

This document defines the system requirements for the automated carrier rate approval module within the logistics operations of "88 Logistics" LLC. The module will support both automatic and manual decision-making for incoming freight rate proposals from carriers.

## 2. Overall Description

The module will receive proposals from multiple carriers through an internal form or API, process them using a business rules engine, and return a decision. If automated rules cannot make a confident decision, the system will flag the offer for manual review by a logistics manager.

## 3. Functional Requirements

| ID    | Requirement                                                             | Priority  |
|-------|-------------------------------------------------------------------------|-----------|
| FR-01 | The system shall automatically evaluate each rate offer                | High      |
| FR-02 | The user shall be able to manually override automatic decisions         | Medium    |
| FR-03 | All decisions shall be saved with timestamps and user identifiers       | High      |
| FR-04 | The system shall allow filtering of rate offers by status and date      | Low       |

## 4. Non-Functional Requirements

| ID     | Requirement                                                             | Type        |
|--------|--------------------------------------------------------------------------|-------------|
| NFR-01 | The system must process each rate offer within ≤ 3 seconds               | Performance |
| NFR-02 | The system must be available at least 99.5% of the time each calendar month | Availability |
| NFR-03 | All user actions must be logged                                          | Security    |

## 5. Interfaces

**UI — User Interface**

The system must provide a dashboard interface that allows the logistics manager to:
- View incoming rate proposals (with filters: carrier name, offer date, status)
- Manually approve or reject each offer
- View decision history logs (with timestamps and status)
- Override automatic decisions

## 6. Database Requirements

| Entity         | Field             | Type     | Description                                  |
|----------------|------------------|----------|----------------------------------------------|
| `RateProposal` | `id`             | UUID     | Unique identifier of the rate offer          |
|                | `carrier_name`   | Text     | Name of the carrier                          |
|                | `rate_value`     | Decimal  | Proposed freight rate                        |
|                | `cargo_type`     | Text     | Type of cargo                                |
|                | `decision_status`| Enum     | auto-approved / rejected / pending / manual  |
|                | `decision_time`  | DateTime | Date and time of decision                    |
|                | `reviewer_id`    | UUID     | Identifier of the user who made the decision |
