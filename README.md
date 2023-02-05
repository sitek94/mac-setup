# Maciek's initial macOs setup

Initially, go through initial macOs setup wizard, create local user account, login to iCloud. Once on the macOs desktop do the steps below.

## Installation

### Install Xcode

```shell
xcode-select --install
```

### Install Ansible using pip

```shell
# Update PATH
export PATH=$HOME/bin:/usr/local/bin:$HOME/.local/bin:$HOME/.local/bin:$PATH

# Update pip
sudo pip3 install --upgrade pip

# Install Ansible
python3 -m pip install --user ansible
```

### Clone this repository

```shell
git clone https://github.com/sitek94/mac-setup.git

cd mac-setup
```

### Install required Ansible roles

```shell
ansible-galaxy install -r requirements.yml
```

### Run Ansible playbook

```shell
# Enter your password when prompted
ansible-playbook main.yml --ask-become-pass
```
