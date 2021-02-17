
# How to use Github to manage project
## Install [GitHub CLI](https://cli.github.com/)
### Debian, Ubuntu Linux (apt)

Install:

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
sudo apt-add-repository https://cli.github.com/packages
sudo apt update
sudo apt install gh
```

Upgrade:

```bash
sudo apt update
sudo apt install gh
```
## Authenticate with a GitHub host and Config
[gh auth login](https://cli.github.com/manual/gh_auth_login)
```bash
# start interactive setup
$ gh auth login

# authenticate against github.com by reading the token from a file
$ gh auth login --with-token < mytoken.txt

git config --global user.email "xxx@xxx.com"
git config --global user.name "user"
```
## Create new repo
### clone
```bash
gh repo clone <repository> [<directory>] [-- <gitflags>...]
```
```bash
gh repo clone https://github.com/
cli/cli

or

gh repo clone cli/cli

```
### Create a local repo and a rmote repo on Github
[gh repo](https://cli.github.com/manual/gh_repo)
```bash
# Create a repository for the current directory.
~/Projects/my-project$ gh repo create
✓ Created repository user/my-project on GitHub
✓ Added remote https://github.com/user/my-project.git
~/Projects/my-project$
```
see more detail [GitHub CLI Manual](https://cli.github.com/manual/)

## Push local repo to remote
```bash
# Create README.md
echo "# OS" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/user/my-project.git
git push -u origin main
```
## Fetch rmote repo
```bash
# 查看远程仓库
git remote -v
# 从远程获取最新版本到本地
git fetch origin main
# 比较远程分支和本地分支
 git log -p main origin/main
# 合并远程分支到本地
git merge origin/main
```
## Reference
[GitHub CLI Manual](https://cli.github.com/manual/)

[廖雪峰Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)
