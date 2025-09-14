# Prompts-for-The-Causal-Canvas
Open-Source Prompts for the project The Causal Canvas: A New, Reproducible Paradigm for AI-and-Data-Driven Econometrics

## Quick Start
This guide will walk you through the setup process to get the most out of Causal Agent on Lucien. 

### Step 0: Account Setup

Register and log in to your Lucien account.

You can find docs for Lucien here: https://forum.ai4.science/t/hackathon-documents-hub. It includes complete information such as Lucien registration and installation, MCP Server development guide, hackathon FAQ, etc.

### Step 1: Configure System Prompt

1. Click on the "Settings" icon in the bottom right corner.
2. Select "Models & Prompt".
3. Copy the content from `LucienSystemPrompt.txt` into the "System Prompt" field.
4. Click "Save".


### Step 2: Import the Final Essay Writer Skill

1. Navigate to "Skills & Tools" on the setting panel.
2. Click "Import Shared Skill".
3. Copy the following ID into the dialog box: `c9661969-7399-4817-ae95-9a09201caa15`
4. Click `Save`.
5. If the import fails, follow these steps:
    * Click "Add Skill".
    * Set the Skill Name to "Final_Essay_Writer".
    * Copy the content from `FinalEssayWriterPrompt.txt` into the "Skill Prompt" field.


### Step 3: Create a Workspace

1. Exit "Settings".
2. Click on “New Workspace” in the left-hand menu.
3. You can set the Workspace Name to anything you like, like `Causal Agent`.
4. You will need to specify a local path for your workspace in “Execution Environment”, like `~/mcp3`.
5. Copy the content from `CausalAgentMainPrompt.txt` into the "Workspace Prompt" field.


### Step 4: Start the Conversation

1. On the workspace page, click "Create" under the "Sessions" section to start a new conversation.
2. **Note:** It's recommended to let Lucien create the working directory first. Then, follow the on-screen instructions to **manually copy** your datasets into the new folder.
3. After that, simply follow the instructions provided by the Agent and continue the conversation.


### Step 5: Optional - Generating LaTeX

You have the option to have the Agent generate LaTeX code. Since Lucien currently can't render LaTeX, you'll need to find the `.tex` and any other relevant files in your workspace. You can then upload them to a platform like Overleaf to compile the document.

## Necessary MCP Tools

- Please **disable** the `filesystem` MCP tool (if you has manually installed it from MCP Store), as it may produce unexceptable behavior like creating fake files.
- `shell_execute` is used for commands like creating files and folders, etc. 
- `txyz_search_scholar` is used for searching literatures on the web.

Both `shell_execute` and `txyz_search_scholar` should be provided and enabled via Lucien by default. If not, please contact Lucien tech support for help.

If there is any difficulty in `shell_execute`, you can try to add [SSH Execution](https://mcpm.sh/registry/?source=lucien&protocol=lucien-cn). Follow the doc and set your `SSH_HOST` as `localhost`, set `SSH_USERNAME` as your username, and set `SSH_PRIVATE_KEY` or `SSH_PASSWORD` accordingly.