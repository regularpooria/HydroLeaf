# Repository structure for developers

This repository is organized to separate raw resources, documentation, and implementation code.

## Top-level folders

- `/assets/` - shared non-code project assets.
- `/paper/` - research notes and manuscript-related material.
- `/docs/` - developer and project documentation.
- `/src/` - source code for the ML pipeline and interfaces.

## Documentation layout (`/docs`)

- `/docs/onbaording/repo.md` - this guide.
- `/docs/segmentation/` - segmentation documentation.
- `/docs/tracking/` - tracking documentation.
- `/docs/deployment/` - deployment documentation.

## Source layout (`/src`)

- `/src/assets/` - runtime assets used by the code.
- `/src/assets/models/` - model binaries/checkpoints.
- `/src/segementation/` - segmentation implementation.
- `/src/tracking/` - object/plant tracking implementation.
- `/src/interface/` - UI, APIs, and integration points.

## Onboarding flow

1. Read `/README.md` for project goals.
2. Read `/CONTRIBUTING.md` for collaboration workflow.
3. Start from docs in `/docs/segmentation`, `/docs/tracking`, and `/docs/deployment` based on your area.
4. Implement features in the matching `/src/*` module.
