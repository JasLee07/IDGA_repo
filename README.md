# IDGA_Repo

Unity 2D project skeleton for a small multiplayer/split-team workflow.

Quick summary:
- Project name: IDGA_Repo
- Intended use: Unity 2D game development with collaborators
- Keep the repo private on GitHub and invite collaborators via "Manage access"

Setup & recommended steps
1. Create the Unity project (2D)
   - Open Unity Hub -> New project -> 2D template -> Name it `IDGA_Repo` and set location.

2. Copy support files
   - Place the provided `.gitignore` and `.gitattributes` files in the root folder of the Unity project (same folder with Assets/ and ProjectSettings/).

3. Enable Git LFS (recommended)
   - Install Git LFS locally if not installed: `git lfs install`
   - The .gitattributes above already lists common asset types; ensure you run:
     - `git lfs install`
     - `git add .gitattributes`
     - `git commit -m "Add .gitattributes for Git LFS"`

4. Initialize repo and push to GitHub (CLI or website)
   - Option A: Using GitHub CLI (recommended if you have gh installed)
     - `git init`
     - `git add .`
     - `git commit -m "Initial commit — Unity 2D project skeleton"`
     - `gh repo create JasLee07/IDGA_Repo --private --description "Unity 2D project for collaboration" --source=. --remote=origin --push`
   - Option B: Using GitHub website
     - Create a new repository named `IDGA_Repo` and set it Private.
     - Follow the instructions that GitHub shows to push an existing repository.

5. Unity editor recommended settings (important for team collaboration)
   - In Unity go to Edit -> Project Settings -> Editor:
     - Version Control Mode: Visible Meta Files
     - Asset Serialization: Force Text
   - Commit the ProjectSettings folder (these settings are stored there).

6. Invite collaborators
   - GitHub web: Settings -> Manage access -> Invite collaborators (enter your friends' GitHub usernames)
   - Or use the GitHub UI for organization/team access if you prefer a team workflow.

Best practices to keep the repo small
- Never commit the Library/, Temp/, or Build/ directories (they are in .gitignore).
- Use Git LFS for large binary assets (art, audio, models).
- Keep art and audio compressed and trimmed before adding to the repo.
- If you import large sample assets you don't need, remove them before committing.
- Use feature branches for major changes; keep main branch stable.
- Ensure everyone uses the same Unity Editor version (ProjectSettings/ProjectVersion.txt will help).
- Provide a small starting scene and a minimal Assets folder layout (Scripts/, Scenes/, Art/) to push.
- Prepare a .editorconfig or contributor guide with branch naming rules, PR checklist, and sample GitHub Actions CI (optional).
