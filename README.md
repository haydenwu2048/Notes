# Notes
## 2022 Nov 08
Set up git accounts for both GitHub and GitLab on a single machine
```
# use this command to check the git connections
ssh -T git@gitlab.oceantrack.org
ssh -T git@github.com

# tree of the .ssh folder
.
├── config
├── id_ed25519
├── id_ed25519.pub
├── id_rsa
├── id_rsa.pub
├── id_rsa_home
├── id_rsa_home.pub
├── known_hosts
└── known_hosts.old

# Content of the configuration file
# Company account
Host <Company GitLab Url>
  HostName  <Company GitLab Url>
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/id_ed25519
# GitHub account
Host github.com
  Hostname github.com
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/id_rsa_home

# Need to set git config user details for a specific project
$ cd ~/home_project
$ git config user.name "home_user"
$ git config user.email "your_name@home_email.com" 
```
### Useful resources
- [Multiple SSH keys for different accounts on Github or Gitlab](https://coderwall.com/p/7smjkq/multiple-ssh-keys-for-different-accounts-on-github-or-gitlab)
- [Testing your SSH connection](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)

## 2022 Nov 09
The method to add new files or folders to a `.gitignore` file and remove already existing stuff.
First, update the gitignore file to exclude the files and folders you don't want to commit, then:
```
git rm -r --cached .
git add .
```