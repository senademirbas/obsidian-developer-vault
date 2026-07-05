# Setup and Workflow Guide (English)

This guide provides detailed instructions on how to install, configure, and integrate the Obsidian Developer Vault template into your daily software development workflow.

---

## What's Included

The vault folder is structured as follows:

| Folder | Purpose |
|--------|---------|
| `00_Dashboard/` | Main dashboard with the task calendar view |
| `01_Daily/` | Daily journals (auto-created from daily template) |
| `02_Projects/` | Active projects tracking + Kanban boards |
| `03_Knowledge/` | Structured knowledge base with topic trees |
| `04_Snippets/` | Annotate code snippets repository |
| `05_Resources/` | Articles, references, PDFs, and assets |
| `_Templates/` | All note templates (Templater-based) |
| `tasksCalendar/` | Custom DataviewJS calendar component |

---

## Required Plugins

To enable all features of this template, install the following community plugins inside Obsidian (**Settings -> Community Plugins -> Browse**):

| Plugin | Purpose | Required? |
|---------|------|---------|
| **Templater** | Apply templates automatically on file creation | Yes |
| **Tasks** | Advanced task tracking with `#task` tags | Yes |
| **Dataview** | DataviewJS engine for the dashboard calendar | Yes |
| **QuickAdd** | `Ctrl+X` quick task capture command | Yes |
| **Kanban** | Kanban project management boards | Yes |
| **Calendar** | Daily notes calendar sidebar panel | Yes |
| **Obsidian Git** | Automatic Git backup | Recommended |
| **Omnisearch** | Full-text search across the vault | Recommended |

> **Note:** All advanced settings, shortcuts, and templating paths are preconfigured in this vault. You only need to install and enable these plugins.

---

## Installation Steps

1. **Download this Vault:**
   Download the ZIP of this repository or clone it.

2. **Open in Obsidian:**
   Open Obsidian, click **Open folder as vault**, and select the `Vault-EN/` folder inside the downloaded project.

3. **Trust the Vault and Enable Plugins:**
   Obsidian will ask to trust the vault. Click **Trust and Enable Plugins**.
   Go to **Settings -> Community Plugins**, turn off **Restricted Mode**, then install and enable the plugins listed in the table above.

4. **Apply the Theme:**
   Go to **Settings -> Appearance -> Themes**, search for **Things**, and install it. (Works beautifully in both dark and light modes).

5. **Start Using the Vault:**
   Open `00_Dashboard/main.md` as your default home page. Your calendar will render automatically.

---

## Daily Developer Workflow

### Task Management
* Press **Ctrl+X** inside any regular note. Type the task description, press Enter, then pick a due date from the calendar popup.
* The plugin will insert: `- [ ] #task your task description [due:: YYYY-MM-DD]`
* *Note:* `Ctrl+X` does not work in Kanban boards. To add tasks in Kanban, use the **+** button, and write `@{YYYY-MM-DD}` to assign a due date.

### Creating a Knowledge Note
1. Navigate to `03_Knowledge/<domain>/`
2. Create a new file (template will apply automatically).
3. In the properties frontmatter, add a hierarchical tag in the `tags` field (e.g. `ml/supervised/xgboost`).
4. Set the `parent:` field to link to the broader topic page (e.g. `[[Machine Learning]]`).

### Starting a New Project
1. Create a folder at `02_Projects/<project-name>/`
2. Create a note named `<project-name>.md` inside it (the project template applies automatically).
3. To add a Kanban board for this project, create a file named `<project-name>-Kanban.md` using the `_Templates/TPL_Kanban-Project` template.

---

## Git Backup Configuration (Optional)

To backup your vault to your private GitHub repository using the `Obsidian Git` plugin:
1. Open a terminal inside your vault folder (`Vault-EN/`) and initialize Git:
   ```bash
   git init
   git remote add origin <your-private-repo-url>
   git add .
   git commit -m "initial vault setup"
   git push -u origin main
   ```
2. In Obsidian, go to **Settings -> Community Plugins** and enable **Obsidian Git**. The plugin will automatically commit and push your changes on the preconfigured intervals.

---

## Credits

- The custom monthly task calendar in the dashboard (`tasksCalendar/`) is powered by [Obsidian-Tasks-Calendar](https://github.com/702573N/Obsidian-Tasks-Calendar) by 702573N. Special thanks to the author for sharing this visualization tool.
