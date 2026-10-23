# Technical Overview — SwiftShip Tracker

## Architecture
1. User asks for parcel details in the SwiftShip Tracker Agentforce agent.
2. `Parcel Details Inquiry` subagent collects the Parcel ID if it was not supplied.
3. Agent action calls the `Parcel Details` autolaunched Flow with `ids`.
4. Flow uses Get Records to find a Parcel where `Parcel_ID__c` equals the supplied ID.
5. Flow invokes the `Retrieve Parcel Details` Prompt Builder template using the retrieved Parcel.
6. Flow assigns the prompt response to `output` and returns it to the agent.
7. Agent presents a conversational update including parcel name, ID, status, weight and estimated delivery date.

## Salesforce components
| Component | Name | Purpose | Report status |
|---|---|---|---|
| Custom object | Parcel | Main parcel record | Created |
| Custom object | Sender | Sender contact/address data | Created |
| Custom object | Receiver | Receiver contact/address data | Created |
| Custom object | Delivery | Delivery and current-location data | Created |
| Prompt Builder | Retrieve Parcel Details | Formats parcel summary | Active |
| Autolaunched Flow | Parcel Details | Finds parcel and returns prompt response | Active |
| Agentforce subagent | Parcel Details Inquiry | Handles parcel-detail questions | Created |
| Agentforce agent | SwiftShip Tracker | Conversational entry point | Active |
| Permission set | Swift Ship | Object/field access | Assigned in org |

## Data model summary
- **Parcel:** Parcel ID (auto-number), Status (picklist), Weight (number), Estimated Delivery Date (date), Sender lookup.
- **Delivery:** Current Location (geolocation), Estimated Delivery Date (date), Sender lookup and Parcel lookup.
- **Sender:** Sender Address (geolocation), Sender Contact (phone), Sender Email (email).
- **Receiver:** Receiver Address (geolocation), Receiver Contact (phone), Receiver Email (email), Sender lookup and Parcel lookup.

Confirm exact API names and all lookup directions in Object Manager before creating metadata files; the report only explicitly gives `Parcel_ID__c` for the Parcel ID field.

## Sample record used in testing
The report records a sample Sender named Rahul, Receiver named Priya and a Laptop Parcel with Parcel ID `P-001`, status `Booked`, and weight `10 kg`, linked to a Delivery record. Treat this as demonstration data, not a real shipment.

## Limits and future scope
The existing implementation retrieves parcel details. Updating parcel status, automatic notifications, reports/dashboards and a public/customer portal are future enhancements, not implemented functions according to the report.
