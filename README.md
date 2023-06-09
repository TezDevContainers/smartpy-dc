# smartPyDC

This purpose of this repo is to allow you to set up a working smartpy environment with as little fuss as possible.

## Create a codespace

1. Create an account at github.com
2. Navigate to https://github.com/grum-tez/smartPyDC
3. Click _Use this template_, then click _Open in a codespace_.

This will clone a copy of the template repository to a remote server (a 'codespace'). When the codespace is created, an in-browser version of Visual Studio Code will provide you access to the repository.

It may take a few minutes for the codespace to finish building.

Your codespace should now be up and running.

## The Command Palette
The Command Palette is a searchable menu that provides access to many commands in VS Code. To open it, click the gear icon in the bottom left hand corner of the screen, and select *Command Palette*.

You will use the Command Palette often enough that it is well worth learning the keyboard shortcut!

**Command Palette keyboard shortcuts:**
Windows/Linux: Ctrl + Shift + P
macOS: ⇧⌘P

Try it out - search for "View: Toggle Terminal" in the command palette. Notice that the keyboard shortcut for *Toggle Terminal* appears alongside the command. 

**Toggle Terminal keyboard shortcuts:**
Windows/Linux: Ctrl + \`
macOS: ^\` (control + backtick)

This is another shortcut worth remembering!

## Optional: using Codespaces with your local version of VSCode

If you are new to VSCode, skip this section.

If you are familiar with VSCode and wish to use your natively-installed VSCode instead of an in-browser instance, open the command palette and select "Codespaces: Open in VS Code Desktop". 

## The .devcontainer folder

You will notice your workspace contains a single folder called ".devcontainer". This contains configuration files which allow the repo to run in a "Development Container" which keeps the development environment constant across systems. Unless you are an advanced user, leave these files alone.

## Install SmartPy

Enter the following commands in the terminal.

First, download smartpy:

```bash
wget smartpy.io/smartpy
```

Then, modify the file permissions to make it executable:

```bash
chmod a+x smartpy
```

## Test SmartPy install with sample contract

To confirm SmartPy is working correctly:

1. Download a sample smartpy file containing contracts and tests:

```bash
wget smartpy.io/templates/welcome.py
```

2. Run the smartpy command on the downloaded file:

```bash
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

You now have everything you need to complete the tutorial exercises within your codespace Visual Studio Code. The state of the codespace will be preserved between sessions, and you can find the codespace again by going to github.com and clicking on _codespaces_. Your codespace will appear on the lefthand side of the page, under the heading "by repository". IMAGE  However, your codespace will be automatically erased after 30 days of inactivity. If you want to save your work permeneantly, you will need to connect your codespace to your own fork of the tutorial repository. The instructions follow:

## Optional: Connect to your own fork of the tutorial repository

In the Activity Bar, click the Source Control view. IMAGE

To stage your changes, click the + symbol on the line next to the word changes (it appears when you mouseover the word *changes*) IMAGE

To commit your staged changes, type a commit message describing the change you've made, then click Commit. IMAGE

Click Publish Branch IMAGE

In the "Repository Name" dropdown, type a name for your new repository, then select Publish to GitHub private repository or Publish to GitHub public repository. IMAGE

## Next steps

You can now choose to either complete the tutorials with a remote setup (via a codespaces server) or a local devcontainer setup (on your own computer)

**Remote Option**: Skip the rest of this readme and complete the tutorials in your new codespace, using the in-browser Visual Studio Code
**Local Option**: Create your own fork of the repo and complete the tutorials in your local instance of Visual Studio Code

We recommend the **Remote Option** if:

- you want to start learning SmartPy *right now* and save 10-20 minutes
- you don't want to use version control (add, commit, push etc) during tutorials
- you don't mind if your work is automatically deleted if inactive for 30 days
- you don't want to install prerequisites on your machine (i.e docker, vscode)

We recommend the **Local Option** if:

- you want to _learn_ in the same environment in which you will _build_
- you plan to transition directly from learning SmartPy to building with it
- you want to create your own fork of the tutorial repo
- you want to use version control
- you don't want to be dependent on codespaces
- you want to save your free codespaces hours for other uses (you have 60 free hours per month)

To choose the **Remote Option**: Follow this LINK to the first tutorial.

To choose the **Local Option**, simply continue to follow along with this readme.

## Local Option

### Prerequisites

- Install Docker Desktop. (LINK) Make sure it is *running*. If you restart your machine, you may have to reopen it.

- Install Visual Studio Code. (LINK) Make sure you are logged in with your github credentials. You can check by clicking on the icon of the portrait on the bottom left. IMAGE

- Install the Visual Studio Code "Dev Containers" extension 

### Clone your repo locally

First, complete the earlier section titled **Optional: Connect to your own fork of the tutorial repository** (if you haven't already done so)

In your browser, navigate to your fork of the repo on github. 

Click on *Code*, then under the *local* tab, copy the HTTPS git address of the repo (IMAGE)

Open a terminal window and navigate to an appropriate folder for this repo.

Type `git clone` followed by a space and then paste the previously copied git address. You will end up with something like this command: 

  ```bash
   git clone https://github.com/YOUR-GITHUB-NAME-HERE/smartPyDC.git
```

Then open the folder in a new VScode window:

``` bash
   cd smartPyDC
   code . #Opens the folder in VSCode
  ```

### Open the folder in a local Dev Container

The final step is to open the folder in a local Dev Container.

Open the VSCode command pallette, and select Dev Containers: Reopen in Container

