# SwiftShip Tracker — Salesforce Developer Project

**Project type:** Salesforce parcel booking and tracking with conversational AI  
**Team Leader:** Santina T  
**Team Members:** Sherika Sebastin S, Dishma R R, Deyon Michaela F

## 1. Project overview
SwiftShip Tracker centralizes parcel, sender, receiver and delivery information in Salesforce. A customer/support user can ask the SwiftShip Tracker Agentforce agent for parcel details by providing a Parcel ID. The agent invokes the `Parcel Details` autolaunched Flow, which finds the Parcel record and uses the `Retrieve Parcel Details` Prompt Builder template to return a formatted update.

## 2. Problem statement
Parcel information may be scattered across records or apps, and customers may need to contact support to get status updates. The project provides a single Salesforce data model and a conversational way to retrieve parcel status, weight and estimated delivery date.

## 3. Implemented in the project report
- Four custom objects: Parcel, Delivery, Sender and Receiver.
- Parcel status values: Booked, In Transit, Out for Delivery, Delivered.
- Parcel ID auto-number format `P-{000}` (example: P-001), weight and estimated delivery date.
- Lookup relationships connecting parcel, sender, receiver and delivery information.
- Delivery current-location geolocation field.
- Active Prompt Builder template: `Retrieve Parcel Details` (`Retrieve_Parcel_Details`).
- Active autolaunched Flow: `Parcel Details` (input `ids`, output `output`).
- Active Agentforce agent: `SwiftShip Tracker`, with `Parcel Details Inquiry` subagent and a Flow-backed action.
- `Swift Ship` permission set with Read, Create and Edit access for the four objects.

## 4. Not yet implemented / future scope (do not describe as completed)
Automatic email notifications, record-triggered automation, Apex triggers/Batch Apex, reports and dashboards, customer Experience Cloud portal, status-updating agent actions, external logistics integrations and CI/CD deployment are listed as future scope in the report.

## 5. Repository map
- `Documentation/` — final project report and technical notes.
- `Phase-Templates/` — project phases and editable phase-wise submission templates.
- `Salesforce-Source/` — configuration inventory and metadata capture guidance. Salesforce org metadata must be retrieved from the actual org before claiming this is a complete deployable source package.
- `Screenshots/` — screenshot checklist and evidence register. Add actual screenshots from your Salesforce org; examples are not fabricated here.
- `Testing/` — test cases and acceptance checklist.

## 6. Important note
This repository contains project documentation and a source-capture guide. It does **not** automatically contain a complete deployable Salesforce org or actual org screenshots. Export actual metadata from your Salesforce Developer Edition org and add the required phase templates supplied by your course. Never commit passwords, access tokens, session IDs or secrets.
