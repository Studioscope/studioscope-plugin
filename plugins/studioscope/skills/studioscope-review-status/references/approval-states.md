# Approval states

Each deliverable version has one approval status. History entries (`get_deliverable_status` → `history[].action`) record who moved it and when.

| Status | Meaning | Who moves it next |
|---|---|---|
| `draft` | Uploaded, not sent to the client | Studio sends it for review → `in_review` |
| `in_review` | Waiting on the client's decision | Client (or studio) approves → `approved`, asks for changes → `changes_requested`, or rejects → `rejected` |
| `changes_requested` | Client wants changes | Studio uploads a new version or re-sends → `in_review` |
| `rejected` | Client turned it down | Studio decides next step |
| `approved` | Signed off | Done |

History `action` values: `requested`, `approved`, `changes_requested`, `rejected`.

Clients only see versions the studio has released, so a client asking "where is v3" may be looking at a version the studio has not released yet.
