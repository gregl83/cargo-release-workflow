# cargo-release-workflow

Cargo Release Workflow.

Build Rust binaries with Cargo and publish them using GitHub Releases.

## Purpose

Demonstrate a GitHub Build and Release workflow for Cargo projects.

## Workflow Steps

### 1. Test

Runs `cargo test` in parallel with `Build` step.

If tests fail, this step will prevent a release.

### 2. Build

Runs `cargo build --release` in parallel with `Test` step.

Builds binary artifacts for Linux, MacOS, and Windows targets.

### 3. Release

Creates release with version tags attaching each binary artifact from `Build` step.

## License

[MIT](LICENSE)
