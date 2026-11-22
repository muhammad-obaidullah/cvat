# Definition of Done

This checklist is written before feature coding starts. Each completed item must have recorded evidence beside it.

- [ ] Plan is the first commit on `dev-test01`; evidence: commit hash.
- [ ] All three documents exist under `docs/`; evidence: [PLAN.md](PLAN.md), [OBJECTIVES.md](OBJECTIVES.md), [DEFINITION_OF_DONE.md](DEFINITION_OF_DONE.md).
- [ ] Endpoint returns correct per-class counts for a known task; evidence: task ID, database result, API result.
- [ ] Endpoint reads label names and counts from CVAT database models; evidence: file and method.
- [ ] Endpoint refuses an unauthenticated request; evidence: HTTP status and raw response.
- [ ] Endpoint refuses a user without task access; evidence: test setup, user, HTTP status and raw response.
- [ ] Page calls the endpoint and renders a graph; evidence: running screen capture or screenshot.
- [ ] Page handles no data clearly; evidence: known empty task and result.
- [ ] Page handles a failed request clearly; evidence: forced failure and result.
- [ ] One speed objective is defined in `OBJECTIVES.md` with target, conditions and method; evidence: five real runs, median and spread.
- [ ] Speed target met, or missed with the reason written down; evidence: section in `OBJECTIVES.md`.
- [ ] Raw output of all 5 runs pasted in `OBJECTIVES.md`; evidence: raw command output in `OBJECTIVES.md`.
- [ ] One filter or grouping beyond plain count is implemented and explained; evidence: code and UI/API example.
- [ ] Live WebSocket updates are implemented, or explicitly listed as unfinished with why.
- [ ] Reconnection is implemented, or explicitly listed as unfinished with why.
- [ ] The Plan contains the decision record if item 10 is reached.
- [ ] The user can explain count location, label storage, one reversed decision, and one unresolved understanding; evidence: Loom link.
- [ ] Changes use small descriptive commits on `dev-test01`; no commit says only `fix` or `wip`.
- [ ] Pull request is from `dev-test01` into `develop` of the user's own fork, not `cvat-ai/cvat`; evidence: PR link.
- [ ] Recording is 5 minutes or less; evidence: Loom link.
- [ ] Every unfinished requirement is listed with its reason.

## Remaining evidence

All unchecked items remain to be supported by real machine results or repository links after implementation.
