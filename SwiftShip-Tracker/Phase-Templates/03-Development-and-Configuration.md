# Phase 3 — Development and Configuration

## Environment
Salesforce Developer Edition.

## Configuration work documented
1. Created custom objects Parcel, Delivery, Sender and Receiver; enabled reporting/search/field history tracking.
2. Created tabs for the objects.
3. Added fields and lookup relationships listed in the data-model template.
4. Added sample linked records (Sender Rahul, Receiver Priya, Laptop Parcel P-001, Delivery record).
5. Created active Record Summary prompt template `Retrieve Parcel Details` (`Retrieve_Parcel_Details`).
6. Created active autolaunched Flow `Parcel Details`: input variable `ids`, output variable `output`; Get Records → prompt action → Assignment.
7. Created permission set `Swift Ship` with Read, Create and Edit access for the four objects and visible field permissions; assigned it to the user used by the agent.
8. Enabled the org settings needed for Agentforce as documented in the report.
9. Created `Parcel Details Inquiry` subagent and a Flow-backed action; activated agent `SwiftShip Tracker`.

## Source export note
This document is a configuration inventory, not a substitute for actual Salesforce metadata. Retrieve source from the actual org with Salesforce CLI or Setup/metadata export, then add the resulting metadata files. Verify API names first. Do not create fake screenshots or claim an export happened if it did not.
