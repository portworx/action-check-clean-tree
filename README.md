# Check Clean Git Tree action
GitHub action that verifies a clean git tree in the currently checked out repository (no staged/unstaged changes).
Use to prevent partial commits without updated generated files.

## Usage

```yml
jobs:
  job-name:
    runs-on: ubuntu-latest
    steps:
    # The action needs to be run in a checked out git repository
    - name: Checkout
      uses: actions/checkout@v2

    # ...more steps

    - name: Check clean git tree
      uses: portworx/action-check-clean-tree@v1

    # ...more steps
```