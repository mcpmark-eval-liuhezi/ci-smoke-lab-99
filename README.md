# ci-smoke-lab-99
Throwaway sandbox for release-readiness CI + contribution loop smoke test (fallback name)

## Build artifact

This repository exercises the contribution-plus-CI loop end to end. The CI workflow
(`.github/workflows/demo.yml`) is dispatchable (`workflow_dispatch`) and uploads a
build artifact named exactly **demo-build**. That artifact is produced by the single
`build` job on `ubuntu-latest`, which writes `demo-build.txt` and uploads it via
`actions/upload-artifact@v4` with the name `demo-build`.
