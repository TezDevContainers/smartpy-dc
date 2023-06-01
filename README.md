# smartPyDC

## Motivation

This purpose of this repo is to allow you to set up a working smartpy environment with as little fuss as possible.

By using a devcontainer, you can code in a local instance of VSCode (or other IDE that is compatible with devcontainers), and use the personalisations, customisations and extensions you are accustomed to.

Further, devcontainers allow you to *build* in the same environment in which you *learned*. Should you wish to transition directly from learning smartpy to building for production, you will not have to learn a _new_ set of 'professional' tools - as you will have been using these tools from the very beginning. Seamless!

## Setup
1. Fork a copy of this repo into your own github account

2. Choose between running a local devcontainer (preferred) or a remote devcontainer (with github codespaces - should work on any machine). Follow only the corresponding instructions:

- 2a. **Local option**
    1. Clone the repo onto your local machine 
   ```bash
    git clone https://github.com/YOUR-GITHUB-NAME-HERE/tutorial.git
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

## Verify 

To check your smartpy devcontainer is working:

1. Download an example smartpy file containing contracts and tests:

``` bash
wget smartpy.io/templates/welcome.py
```

2. Run the smartpy command on the downloaded file:

``` bash
 ./smartpy test welcome.py welcome/
```

The above command should generate test results and compiled contracts in a directory titled `welcome`. You can confirm this with:

```bash
ls -R welcome/
```
If your smartpy set up is working correctly, your output should look something like this:

```
welcome/:
Welcome  scenario.json  script_init.py

welcome/Welcome:
log.txt                        step_004_cont_0_params.json  step_007_cont_0_params.tz
step_002_cont_0_contract.json  step_004_cont_0_params.py    step_008_cont_0_params.json
step_002_cont_0_contract.tz    step_004_cont_0_params.tz    step_008_cont_0_params.py
step_002_cont_0_sizes.csv      step_005_cont_0_params.json  step_008_cont_0_params.tz
step_002_cont_0_storage.json   step_005_cont_0_params.py    step_010_cont_1_contract.json
step_002_cont_0_storage.py     step_005_cont_0_params.tz    step_010_cont_1_contract.tz
step_002_cont_0_storage.tz     step_006_cont_0_params.json  step_010_cont_1_sizes.csv
step_002_cont_0_types.py       step_006_cont_0_params.py    step_010_cont_1_storage.json
step_003_cont_0_params.json    step_006_cont_0_params.tz    step_010_cont_1_storage.py
step_003_cont_0_params.py      step_007_cont_0_params.json  step_010_cont_1_storage.tz
step_003_cont_0_params.tz      step_007_cont_0_params.py    step_010_cont_1_types.py
```

If you have any issues getting the devcontainer to work, please report this. If you find the instructions above are not complete, please report this or make a pull request. If the local devcontainer doesn't work for you, try the remote/codespaces option. The remote option should work on ALL machines. If it doesn't, please report!
