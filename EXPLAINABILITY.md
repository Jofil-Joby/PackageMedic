## Decision and Reasoning

PackageMedic decides whether the repository exposes recognizable package metadata. Missing package manifests are reported as a packaging-readiness finding with a targeted recommendation.

## Inputs and Data Sources

It checks for package.json, pyproject.toml, or pom.xml in the project evidence. The decision uses explicit filename rules.

## Limits and Constraints

It does not inspect package-version correctness, publishing configuration, lockfile integrity, or dependency vulnerabilities. Projects using other package systems may require manual review.
