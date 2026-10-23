# Custom Object Inventory

## Parcel
- Parcel ID: Auto Number, format `P-{000}`; field API name cited in Flow: `Parcel_ID__c`.
- Status: Picklist — Booked, In Transit, Out for Delivery, Delivered.
- Weight: Number.
- Estimated Delivery Date: Date.
- Sender: Lookup to Sender.

## Delivery
- Current Location: Geolocation.
- Estimated Delivery Date: Date.
- Sender: Lookup.
- Parcel: Lookup.

## Sender
- Sender Address: Geolocation.
- Sender Contact: Phone.
- Sender Email: Email.

## Receiver
- Receiver Address: Geolocation.
- Receiver Contact: Phone.
- Receiver Email: Email.
- Sender: Lookup.
- Parcel: Lookup.

**Important:** Exact object API names, field API names, relationship names and requiredness must be copied from the Salesforce org. Only `Parcel_ID__c` is explicitly stated in the report as an API name.
