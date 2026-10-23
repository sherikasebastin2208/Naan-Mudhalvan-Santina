# Phase 2 — Requirements and Data Model

## Functional requirements
| ID | Requirement | Status per report |
|---|---|---|
| FR-01 | Create parcel booking/record | Implemented |
| FR-02 | Track parcel status | Implemented |
| FR-03 | Store parcel weight | Implemented |
| FR-04 | Store estimated delivery date | Implemented |
| FR-05 | Maintain sender information | Implemented |
| FR-06 | Maintain receiver information | Implemented |
| FR-07 | Store delivery/current location | Implemented (Delivery object and geolocation field) |
| FR-08 | Allow agent to update parcel status | Planned |
| FR-09 | Send automatic customer notifications | Planned |
| FR-10 | AI-powered parcel inquiry | Implemented (Agentforce + Prompt Builder + Flow) |
| FR-11 | Reports and dashboards | Planned |
| FR-12 | Customer access through Experience Cloud | Planned |

## Non-functional requirements
Usability, access control, reliable/accurate data, cloud availability, maintainability, scalability, data integrity and response within a few seconds.

## Object/field inventory
| Object | Fields identified in report |
|---|---|
| Parcel | Parcel ID: Auto Number `P-{000}`; Status: Picklist; Weight: Number; Estimated Delivery Date: Date; Sender: Lookup |
| Delivery | Current Location: Geolocation; Estimated Delivery Date: Date; Sender: Lookup; Parcel: Lookup |
| Sender | Sender Address: Geolocation; Sender Contact: Phone; Sender Email: Email |
| Receiver | Receiver Address: Geolocation; Receiver Contact: Phone; Receiver Email: Email; Sender: Lookup; Parcel: Lookup |

The report does not state every field or all API names. Verify these in the Salesforce org before writing deployment metadata.

## Main data flow
Customer question → SwiftShip Tracker agent → Parcel Details Inquiry subagent → Parcel Details Flow → Get Records by Parcel ID → Retrieve Parcel Details prompt → formatted response to user.
