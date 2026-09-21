# PackageMedic

> Portable agent for diagnosing missing or unclear package metadata.

## What it does

PackageMedic inspects project structure for common package manifests such as `package.json`, `pyproject.toml`, and `pom.xml`. It turns missing package metadata into a clear improvement recommendation.

### Diagnostic fingerprint

**Manifest discovery → packaging signal → evidence → action**

## Why this agent is distinct

PackageMedic is concerned with how a project describes itself as a distributable or runnable unit. It is separate from DependencyMedic: one focuses on the presence of dependency declarations, while PackageMedic focuses on package metadata itself.

## Workflow

```text
Project tree
    ↓
Package-manifest detector
    ↓
Metadata rule
    ↓
Evidence
    ↓
Packaging improvement plan
```

## Verification

Includes an OpenGAP-compatible passport, package-focused fixture, portability adapters for four targets, explainability contracts, and automated adapter tests.

The OpenGAP validator passed and all four generated framework exports have been exercised successfully.

## Design principle

**Metadata is part of the software interface.** PackageMedic surfaces missing project metadata instead of guessing package behavior.

## Medic family

PackageMedic is a specialized packaging diagnostic designed to compose with dependency, deployment, and documentation agents.