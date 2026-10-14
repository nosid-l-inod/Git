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