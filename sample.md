What is GitHub actions

--->it is automation service offered by GitHub Company
--->this service can provide a automation all kinds of repository and related process and actions


it was divided into 2 types
1.ci/cd
2.code repository management



what is ci/cd

-->it is continuous integration and continuous delivery(or) continuous deployment

continuous integration:code changes are automatically built ,tested and merged with existing Code

continuous delivery:After integration ,new App or package Versions  are published automatically


what is Code repository management

--->Automate Code review and issues management

 


What is Git

--->Git is free version control system
-->it is tool
-->manage source code changes
--->it contain save code snapchats("commits")

--->we can work with different branches

--->with git you can easily rollback to older code snapshots (or) we can develop new feature without breaking production Code





Steps for installation of git

--->search for git 
--->download the git 
--->in cmd check git



git config --global user.name "your-username"
git config --global user.email "your-email"
git config --list



commands

git init 
git add .
git status 
git commit -m "initial commit"

git checkout "fcd4dea61c3a6d266ccf63b1cb8173f1717be9de"    to move from one commit to another commit head points to the selected id

git reset --hard id to remove the commits history 
example:git reset --hard 4286a4b95ea69b528804353440745921f552320e  and head also moved

git log -->to see all commits from local and global
git clone <url>  --->to clone the url
git branch                       # List local branches
git branch -a                    # List all branches (local + remote)
git branch -r			 #to see list of remote branches
git branch <name>                # Create new branch
git checkout <name>              # Switch to branch
git checkout -b <name>           # Create + switch in one step
git switch <name>                # Modern switch command
git switch -c <name>             # Modern create + switch
git branch -d <name>             # Delete branch (safe)
git branch -D <name>             # Force delete branch
git branch -m <old> <new>        # Rename branch
git pull                         # Get latest changes



real time problem:

1 day back
──────────────────────────────
dev        → 1 → 2 → 3
256        → 1 → 2 → 3

Today
──────────────────────────────
dev        → 1 → 2 → 3 → 4 → 5  ← others added new changes
256        → 1 → 2 → 3 → A → B  ← your changes


Step 1 — Save your code in 256
git add .
git commit -m "my changes done"

Step 2 — Go to dev and get latest changes
git checkout dev
git pull origin dev

Step 3 — Come back to 256
git checkout reg/chore-256

Step 4 — Bring dev changes into your 256 branch
git merge dev

⚠️ If conflict comes → Fix it
bash# Fix the file
git add .
git commit -m "resolved conflict"

Step 5 — Push your branch
git push origin reg/chore-256
Step 6 — Raise PR on GitHub
FROM → reg/chore-256
TO   → dev

👇 All Commands Together
git add .
git commit -m "my changes done"
git checkout dev
git pull origin dev
git checkout reg/chore-256
git merge dev
git push origin reg/chore-256
# Raise PR on GitHub FROM 256 TO dev ✅

😊 Simple Picture
dev     → 1 → 2 → 3 → 4 → 5
                          ↓
256     → 1 → 2 → 3 → A → B → 4 → 5  ← after merge dev
                                   ↓
                              PUSH & RAISE PR
                                   ↓
dev     → 1 → 2 → 3 → 4 → 5 → A → B ✅

git rebase -i HEAD~7  

git stash

git stash pop--->it will delete from stash after pop


git stash save apply --->it willpresent in both









               
