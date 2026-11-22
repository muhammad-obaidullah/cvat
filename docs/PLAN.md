# Plan

## Approach

| Time | Work |
|---|---|
| 0:00–1:00 | Confirm the source-development stack, branch, commit, and CVAT data model. |
| 1:00–2:30 | Add Django app `test`, task-count API, routing, authentication, and task access. |
| 2:30–3:30 | Compute per-class counts from `annotations/instances_val2017.json` for exactly the images uploaded to the task, compare them with the endpoint's counts, and add focused API tests. |
| 3:30–4:30 | Add the task analytics page and call the endpoint. |
| 4:30–5:15 | Render the graph with loading, empty, and failed-request states. |
| 5:15–6:00 | Define and measure one speed objective with five real runs. Write the target in `docs/OBJECTIVES.md` before any measurement begins. |
| 6:00–6:45 | Add one filter or grouping beyond plain counts and explain it. |
| 6:45–7:30 | If items 1–7 are complete, assess WebSocket updates and reconnection. |
| 7:30–8:00 | Finish evidence, final checks, and the 5-minute recording. |

The first code change will be the Django app and API. UI work follows endpoint correctness.

## Already decided to skip

- Skip items 8–9 (WebSocket updates and reconnection) unless items 1–7 are complete by 6:45. If skipped, list them in the unfinished list with the reason.
- Count shapes only (`LabeledShape`) because COCO 1.0 instance import creates shape annotations. Tracks and tags are out of scope.
- Item 10 (decision record) will be added only after implementation decisions are known.

## Environment

- CPU: Apple M3 Pro
- Physical RAM: 18.00 GB (19327352832 bytes)
- OS: macOS 26.5.2, Build 25F84
- Free disk at `/`: 245 GiB
- Docker: 29.9.3
- Docker Compose: v5.7.1
- Docker runtime memory limit: 8214519808 bytes (approximately 8 GB)
- CVAT commit SHA: `d4d08dedb5ad7c5e980c0bc7319a7f5587365dad`
- Images in task: (to fill in after task creation)

## Plan changes

PR target is develop, not main. CVAT has no main branch; Section 10 says 'the main branch of your own fork', which is develop in this fork.
