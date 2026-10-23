# Salesforce Source and Configuration

The supplied report documents configuration performed in a Salesforce Developer Edition org, but the actual metadata export was not included in the uploaded files. Therefore, this folder contains a component inventory and export instructions, not a complete deployable package.

## Components to retrieve from the real org
- Custom objects and fields: Parcel, Delivery, Sender, Receiver
- Tabs and permission set `Swift Ship`
- Autolaunched Flow `Parcel Details`
- Prompt Builder template `Retrieve Parcel Details`
- Agentforce agent `SwiftShip Tracker`, subagent `Parcel Details Inquiry` and its action, where supported by the org's metadata tooling

Use Salesforce CLI/Metadata API and your org's supported retrieval process. Confirm exact API names and retrieve dependencies. Some Agentforce/Prompt Builder metadata may have feature/API-version-specific retrieval requirements. Do not commit authentication files or secrets.
