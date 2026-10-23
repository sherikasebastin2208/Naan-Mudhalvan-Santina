# Flow Specification — Parcel Details

**Type:** Autolaunched Flow  
**Status in report:** Active  
**Input:** `ids` (Parcel ID supplied by user)  
**Output:** `output` (prompt response)

## Logic
1. Get Records: find Parcel where `Parcel_ID__c` equals `ids`.
2. Action: invoke Prompt Builder template `Retrieve Parcel Details`, passing the retrieved Parcel as the record to summarize.
3. Assignment: set `output` to the Prompt Response.
4. Return the output to the Agentforce action.

## Validation checklist
- `ids` is configured as an input variable with correct data type.
- Get Records returns the intended Parcel record.
- Prompt action references the retrieved record.
- Assignment maps the prompt response to `output`.
- Flow is Active and invoked by the correct agent action.

This is a written specification, not an exported Flow metadata XML file.
