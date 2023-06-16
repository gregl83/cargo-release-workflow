![Build](https://img.shields.io/github/actions/workflow/status/gregl83/cargo-release-workflow/release.yml)
![Release](https://img.shields.io/github/v/release/gregl83/cargo-release-workflow)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/gregl83/cargo-release-workflow/blob/master/LICENSE)
# cargo-release-workflow

Cargo Release Workflow.

Build Rust binaries with Cargo and publish them using GitHub Releases.

## Purpose

Demonstrate a GitHub Build and Release workflow for Cargo projects.

## Overview

Uses basic `cargo init` for example project.

See [release.yml](.github/workflows/release.yml) for workflow requirements.

## Workflow Steps

Triggered by a `git push` of a new tag using Semver 2.0 (e.g., `v1.0.0`).

### 1. Test

Runs `cargo test` in parallel with `Build` step.

*If a test fails, this step will prevent a release.*

### 2. Build
Workflow 
Runs `cargo build --release` in parallel with `Test` step.

Builds binary artifacts for Linux, MacOS, and Windows targets.

*If a build fails, this step will prevent a release.*

### 3. Release

Creates release using version tag and binary artifacts from `Build` step.

## License

[MIT](LICENSE)
