# smartPyDC

## Setup

1. Clone the repo onto your local machine

```bash
git clone [https://github.com/YOUR-GITHUB-NAME-HERE/tutorial.git](https://github.com/grum-tez/smartPyDC.git)
cd tutorial
code . #Opens the folder in VSCode
```

2. Make sure you have Docker Engine (Docker CLI tool) or Docker Desktop installed and *running* 

3. Choose between a local or remote devcontainer, and follow only the corresponding instructions:

- 3a. Local DevContainer option
    1. Install the VSCode Dev Containers extension
    2. Open the VSCode command pallette, and select Dev Containers: Reopen in Container
    3. Wait for the container to build. If prompted to install recommended extensions, select Yes.
    
- 3b. Remote option (GitHub codespaces)
    1. Using your Github login details, sign up for a Codespaces account. You may be required to provide payment details. At the time of writing, Codespaces accounts come with 60 free hours per month, but please note that if you exceed this you will be billed.
    2. Install the VSCode Codespaces extension
    3. Open the VSCode command pallette and select Codespaces: Create New Codespace
    4. Select the tutorial repo, and the main branch.
    5. Wait for the container to build within the remote container. If prompted to install recommended extensions, select Yes.

Building the container typically takes a few minutes, but could take longer depending on your machine. 
Your development environment should now be ready.
