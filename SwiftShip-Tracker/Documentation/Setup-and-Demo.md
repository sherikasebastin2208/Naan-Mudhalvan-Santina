# Setup and Demo Guide

## Prerequisites
- Access to the Salesforce Developer Edition org used for the project.
- Permission to view Object Manager, Flow Builder, Prompt Builder and Agentforce.
- Use a test/demo org and demonstration records only.

## Verify configuration in Salesforce
1. In Setup → Object Manager, confirm Parcel, Delivery, Sender and Receiver objects and their fields.
2. Confirm Parcel ID auto-number format `P-{000}` and status values Booked, In Transit, Out for Delivery, Delivered.
3. Confirm lookup relationships and that the sample records are linked.
4. In Prompt Builder, open `Retrieve Parcel Details` and verify it returns parcel name, ID, status, weight and estimated delivery date.
5. In Flow Builder, open `Parcel Details`; verify Get Records filters Parcel by `Parcel_ID__c` = `ids`, the prompt action is connected, and output is assigned to `output`. Confirm it is Active.
6. In Agentforce, verify `SwiftShip Tracker` is Active and its `Parcel Details Inquiry` subagent uses the Flow-backed action.
7. Verify `Swift Ship` permission-set access for the user running the agent.

## Demo script
1. Open the SwiftShip Tracker agent test preview.
2. Ask: “Can you check my parcel status?”
3. When asked, enter `P-001`.
4. Confirm the response refers to Laptop Parcel and shows status `Booked`, weight `10 kg`, and the available estimated delivery date.
5. Capture screenshots of the agent conversation and action trace, masking personal/contact data where appropriate.

## Troubleshooting
- No parcel returned: check that `P-001` exists and the exact field API name and Flow input match.
- Agent cannot invoke Flow: check the action is added to the correct subagent, Flow is Active, and the running user has permissions.
- Prompt response misses fields: inspect the prompt template input and retrieved Parcel record.
- Do not claim live GPS tracking or customer notifications unless separately implemented and tested.
