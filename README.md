1. Install Git

- git config --global user.name "Your Name"
- git config --global user.email "Your Email"
- git config --global init.defaultBranch main

# Git commands
- git init - Initialize empty repository
- git status - Check file status
- git add - Add files to staging area
- git commit -m "Message" - Commit changes
- git log --oneline - See the commit history
- git clone <repolink> - Clone a repo
- git fetch origin - Download changes without merging
- git pull origin main

## Tag
- git tag <tagname> - Create a tag
- git show <tagname> - Show tagname
- git push origin <tagname>

## Branches
Allow to work on different part of a project without interfering with the main branch

- git branch <branchname> - Create a new branch
- git branch - List all Branches
- git checkout <branchname> - Switch between branches
- git branch -d <branchname>
- git branch -D <branchname>

# .Gitignore
- .gitignore - To hide files

# Git and Github
- SSH - Remote way to connect to a git repo using a public and a private key
- ssh-keygen - Generate a new SSH key pair
- ssh-add - Add the private key to the ssh agent
- ssh -T git@github.com - Test SSH connection
- ssh-add -l - List loaded SSH keys
- ssh-add -d - Remove a key from agent

1. eval $(ssh-agent -s) - Enable SSH
2. ssh-keygen -t rsa -b 4096 -C "your@email.com" - Generate SSH key
3. (eval "$(ssh-agent -s)" ssh-add ~/.ssh/id_rsa) - Add the key to the ssh agent 
4. clip < ~/.ssh/id_rsa.pub - Copy the key
5. Add the ssh key to github on settings, ssh...
6. ssh -T git@github.com - Test the connection
7. git remote add origin git@github.com:your-username/your-repo.git - Add the remote origin
7. git remote set-url origin git@github.com:your-username/your-repo.git - Update the remote origin

# Private email
- Copy the private email from setting, emails, under keep my email private
- git config --global user.email "12345678+nosid-l-inod@users.noreply.github.com" - Configure the private email
- git commit --amend --reset-author --no-edit - Change the author or something like that


# Working in a different version of a file
1. Create the file and add something in the main branch
2. Add and commit the changes
3. Create a new  branch for the new feature and use it
4. Edit the file in the new branch
5. Add and commit the changes
6. git switch main - To switch between the branches and see the changes (git switch main ou git switch new)
- ALWAYS COMMIT THE CHANGES BEFORE SWITCHING TO SEE THE CHANGES
7. Switch to the main branch and merge. git merge <newbranch>
8. Push
- We can delete the branch or push it without merging
- git push -u origin <newbranch>


# Most used
- git status - Check the current state
- git add . - Prepare every change to commit
- git commit -m "message" - Save a version
- Git push - Send the commit to github
- git pull - Pull commits from github
- git clone <url> - Clone a repo
- git switch -c name - Create and switch to a new branch
- git switch <branchname> - Switch to a new branch
- git merge <name> - Merge to the current branch
- git log --oneline - Check the history
- git diff - Check uncommited changes

- git blame <filename> - See who did what

# .Gitignore
- .gitignore tells git which files and folder to ignore to keep them out of the repo
- touch .gitignore - Create the gitignore file. We can also do it manually
- temp/ - Put this inside the file to ignore everything inside the folder

- git rm -r --cached foldername/ - Stop tracking a folder
- git rm --cached filename - Stop tracking a file


# Merge conflicts
- Merge conflict happens when we merge two branches that changed the same lines in a file
- git status - Check which files have conflicts
- git diff - See the differences
- Open the conflicted file and remove, edit the file and remove the conflict markers
- After fixing the file Add it and commit

- git merge --abort - Abort the merge
- git checkout --ours <filename> - Keep our changes
- git checkout --theirs <filename> - Keep their changes


# CI/CD
- Continuous Integration and Continuous Deployment/Delivery
- The code is automatically tested and deployed every time is pushed    

1. Find bugs faster
2. Deploy changes faster
3. Reduce manual steps and mistakes
4. Get quick feedback on every push

## Concepts
- Workflow: A series of jobs that run together
- Job: A group of steps that run together
- Step: A single task, like checking out code or running tests
- Runner: The computer/server that runs your jobs
- Trigger: Decides when your workflow runs
- Environment Variables: Settings for your workflow
- Secrets: Passwords or API keys
