# Phase 4 — Testing and Security

## Test cases reported
| ID | Test | Expected result | Reported result |
|---|---|---|---|
| TC-01 | Create four custom objects | Objects appear in Object Manager | Pass |
| TC-02 | Create Parcel record | Parcel ID auto-numbers as P-001 | Pass |
| TC-03 | Link Sender, Receiver and Delivery | Lookup relationships save/display | Pass |
| TC-04 | Preview prompt with Laptop Parcel | Formatted parcel update returned | Pass |
| TC-05 | Activate Flow | Flow shows Active | Pass |
| TC-06 | Ask agent for parcel details | Agent asks for Parcel ID | Pass |
| TC-07 | Provide P-001 | Name, ID, status, weight and date returned | Pass |
| TC-08 | Assign permission set | Assignment listed on user | Pass |

These outcomes are transcribed from the project report; rerun them in your own org before final submission.

## Security checks
- Confirm only appropriate users have Read/Create/Edit access.
- Verify field-level visibility for sender/receiver contact details.
- Use demo data in screenshots and redact private contact information.
- Never commit passwords, access tokens, session IDs, `.env` files or org credentials.

## Reported performance observation
The report's test trace says subagent/action selection took about 0.5 seconds each and the Flow action about 4 seconds. This is a recorded test observation, not a performance guarantee.
