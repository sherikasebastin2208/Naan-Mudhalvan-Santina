# Phase 1 — Planning and Design

## Project title
SwiftShip Tracker — Salesforce Parcel Tracking with Agentforce AI

## Problem
Customers can experience delays and confusion when parcel status is difficult to find and they need to contact support or switch between systems.

## Objective
Centralize parcel and contact data in Salesforce and provide conversational retrieval of parcel details by Parcel ID.

## Target users
- Customer/sender: wants parcel status and delivery estimate.
- Receiver: needs delivery information.
- Delivery agent: needs parcel and delivery details.
- Support staff: responds to parcel enquiries.
- Administrator: manages records, access and configuration.

## Scope
**Included:** Parcel records, sender and receiver data, delivery details, status and weight fields, estimated delivery date, Agentforce parcel inquiry, Flow and Prompt Builder, permission set.

**Not included in current implementation:** automatic customer notifications, status changes through the agent, dashboards/reports, Experience Cloud customer portal and external carrier integration.

## Proposed solution
Use Salesforce custom objects for structured records, an autolaunched Flow to retrieve a Parcel, Prompt Builder to format a summary, and Agentforce to conduct the conversation.

## Success criteria
A user can provide `P-001` to the active agent and receive a response with parcel name, ID, status, weight and estimated delivery date from the Salesforce record.
