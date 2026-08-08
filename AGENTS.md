# Repository Guidance for AI Coding Agents

This file defines repository-level guidance for AI-assisted development.

## Project Scope

Open LLM Engineering is an independently maintained open-source project focused on
transformer training, inference, evaluation, optimization, reproducibility, and
modern LLM engineering workflows.

The repository is derived from Sebastian Raschka's LLMs-from-scratch project.
Preserve upstream attribution, licensing, and authorship information.

## Development Requirements

Before proposing or submitting changes:

- Follow the existing repository structure.
- Keep changes focused and reviewable.
- Avoid unnecessary dependencies.
- Add or update tests for modified behavior.
- Update documentation when behavior or interfaces change.
- Preserve compatibility where practical.
- Do not remove upstream attribution or licensing notices.

## Validation

Run the relevant checks before considering a change complete:

- unit tests
- linting
- type checking where configured
- package or example execution where applicable
- documentation validation where applicable

## Security-Sensitive Areas

Treat the following areas as security-sensitive:

- checkpoint and model loading
- serialization and deserialization
- external datasets and files
- file-system access
- dependency updates
- subprocess or shell execution
- dynamically loaded code
- inference utilities
- contributed code

Avoid introducing unsafe loading patterns or executing untrusted content.

## Pull Requests

Pull requests should include:

- a clear summary
- motivation for the change
- related issue when applicable
- tests or validation steps
- documentation updates when needed
- benchmark results for performance-sensitive changes
- security considerations for security-sensitive changes

## Performance Changes

For optimization work such as KV caching, quantization, attention changes, or
inference improvements:

- provide reproducible benchmarks
- document hardware and software environment
- compare against a baseline
- avoid unsupported performance claims

## Maintainer Review

AI-generated code is not automatically trusted.

All changes must remain subject to maintainer review before merge, release, or
security-sensitive deployment.
