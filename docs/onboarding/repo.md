# Repository structure for developers

This repository is organized to separate raw resources, documentation, and implementation code.

## Top-level folders

- `/paper/` - research notes and manuscript-related material.
- `/docs/` - developer and project documentation.
- `/src/` - source code for the ML pipeline and interfaces.

## Documentation layout (`/docs`)

- `/docs/onboarding/0_readme.md` - information about the project.
- `/docs/onboarding/related_works.md` - related works.
- `/docs/onboarding/repo.md` - this guide.
- `/docs/onboarding/setup.md` - Goes over how to get your dev environment setup.
- `/docs/segmentation/` - segmentation documentation.
- `/docs/tracking/` - tracking documentation.
- `/docs/deployment/` - deployment documentation.
- `/docs/assets/` - Any assets that are used in documentation, could be images, videos, ... .

## Source layout (`/src`)

- `/src/assets/` - runtime assets used by the code.
- `/src/assets/models/` - model binaries/checkpoints.
- `/src/segmentation/` - segmentation implementation.
- `/src/tracking/` - object/plant tracking implementation.
- `/src/interface/` - UI, APIs, and integration points.
<!-- 
## Onboarding flow

1. Read `/README.md` for project goals.
2. Read `/CONTRIBUTING.md` for collaboration workflow.
3. Start from docs in `/docs/segmentation`, `/docs/tracking`, and `/docs/deployment` based on your area.
4. Implement features in the matching `/src/*` module. -->
