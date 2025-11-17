# In detail



# Node.js 

Node.js allows developers to run JavaScript  outside of a web browser , on the  server-side , to build  scalable, high-performance applications .

### Key Features

- Open-source 
- Lightweight 
- Highly scalable 
- High performance (event-driven, non-blocking I/O) 

### Common Use Cases

- Web applications
- Real-time chat apps
- REST APIs
- Server-side scripting

---

## Install Node.js Using NVM (Node Version Manager)

NVM allows you to install  multiple Node.js versions  and switch between them easily.
Example: Use  Node 18  for one project and  Node 20  for another.

---

### Step 1: Install `curl`

`curl` is used to download the NVM installation script from the internet.

sudo apt install curl


### Step 2: Download & Install NVM

curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash


### Step 3: Load NVM into your terminal

source ~/.bashrc

note: Kali Linux uses Zsh as the default shell, we have two options to Fix: Switch to Bash OR configure Zsh properly
 **Switch your shell to Bash, command: chsh -s /bin/bash, Then log out and log in again, or run: bash
 **Stay on Zsh (default Kali): command: source "$HOME/.sdkman/bin/sdkman-init.sh", And add it permanently to: nano ~/.zshrc, then add line-source "$HOME/.sdkman/bin/sdkman-init.sh", after saving, write: source ~/.zshrc




### Verify Installation

nvm --version

### View available Node.js versions

nvm ls-remote


### Install a specific Node.js version

Example: Install Node.js  18.15.0 

nvm install 18.15.0


### List installed Node.js versions

nvm ls


### Check Node.js version

node -v



---------------------------------------------------------------------------------------------------------------------------------

# Python + pyenv Installation(Kali Linux)

## Why pyenv?

**Manage multiple Python versions** easily.
**Create virtual environments** for different projects.
**Different teams = different Python versions** → pyenv solves version conflicts.
**Keeps system Python intact** (avoids breaking OS tools).
**Consistency across environments** → same Python version for Jenkins builds on any OS.

---

## Official Repository

GitHub: pyenv → (https://github.com/pyenv/pyenv)


## Step 1: Install Dependencies

sudo apt update
sudo apt install make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl git \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev


## Step 2: Install pyenv

git clone https://github.com/pyenv/pyenv.git ~/.pyenv


## Step 3: Configure pyenv

Add to your `~/.bashrc`:

echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init - bash)"' >> ~/.bashrc


Reload shell:

source ~/.bashrc


## Step 4: Verify pyenv

pyenv install -l   # List all versions
pyenv install 3.9.6
pyenv versions     # Show installed versions
pyenv global 3.9.6 # Set default Python
python -V          # Verify


## pyenv Installed Successfully!



# to do

java- jvm
Tfswitch-for teraf
ansible
awscli
