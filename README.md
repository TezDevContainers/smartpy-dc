# smartPyDC

## Setup
1. Fork your own copy of this repo.

2. Choose between running a local devcontainer (preferred) or a remote devcontainer (with github codespaces), and follow only the corresponding instructions:

- 2a. **Local option**
    1. Clone the repo onto your local machine 
   ```bash
    git clone [https://github.com/YOUR-GITHUB-NAME-HERE/tutorial.git](https://github.com/grum-tez/smartPyDC.git)
    cd tutorial
    code . #Opens the folder in VSCode
    ```
    2. Make sure you have Docker Engine (Docker CLI tool) or Docker Desktop installed and *running*
    3. Install the VSCode Dev Containers extension
    4. Open the VSCode command pallette, and select Dev Containers: Reopen in Container
    5. Wait for the container to build. If prompted to install recommended extensions, select Yes.
    
- 2b. **Remote option (GitHub codespaces)**
    1. Using your Github login details, sign up for a Codespaces account. You may be required to provide payment details. At the time of writing, Codespaces accounts come with 60 free hours per month, but please note that if you exceed this you will be billed.
    2. Install the VSCode Codespaces extension
    3. Open the VSCode command pallette and select Codespaces: Create New Codespace
    4. Select the tutorial repo, and the main branch.
    5. Wait for the container to build within the remote container. If prompted to install recommended extensions, select Yes.

Building the container typically takes a few minutes, but could take longer depending on your machine (or the remote machine you have been assigned). 
Your development environment should now be ready.
