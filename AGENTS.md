# HydroLeaf repository map for coding agents

This file gives coding agents a fast path to the correct working area.

## Primary targets

- `/docs/onbaording/repo.md`: canonical human-oriented structure overview.
- `/docs/segmentation/`, `/docs/tracking/`, `/docs/deployment/`: domain docs.
- `/src/segementation/`: segmentation code.
- `/src/tracking/`: tracking code.
- `/src/interface/`: interface and integration code.
- `/src/assets/models/`: model artifacts and checkpoints.

## Agent operating guidance

1. Identify the requested domain (`segmentation`, `tracking`, `deployment`, or interface work).
2. Read the matching folder under `/docs` before editing code.
3. Apply code changes only in the corresponding `/src` subtree unless explicitly asked otherwise.
4. Keep documentation in sync whenever behavior or structure changes.
