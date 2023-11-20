# Maciek's initial macOs setup

Initially, go through initial macOs setup wizard, create local user account, login to iCloud. Once on the macOs desktop
do the steps below.

## Installation

### Install Xcode

```shell
xcode-select --install
```

### Install Ansible using pip

Create `.zshrc` with content:

```shell
touch ~/.zshrc
```

```shell
PATH="$PATH:"
PATH="$PATH:$HOME/Library/Python/3.9/bin"
```

Update pip

```shell
sudo pip3 install --upgrade pip
```

Install Ansible

```shell
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

## Post installation step by steps instructions

- 1Password - login to your account and setup new device using QR code
- Setup HyperKey 
  - Karabiner Elements
  - [Hyperkey](https://hyperkey.app/) (alternative)
- Dropbox - login and sync
- Raycast - import settings from Dropbox
- Keyboard Maestro - import settings from Dropbox
- Logi Options (Mouse + Keyboard) login and sync
- Setapp - login and install same apps from other machine
- Disable default Mac shortcuts
  - Screenshots
  - Spotlight
- Arc Browser - login and sync settings
- Chrome - login and sync settings
- VSCode - login (with GitHub) and sync settings

## Resources

- Ansible
  - https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
  - https://github.com/geerlingguy/mac-dev-playbook
  - https://github.com/ThePrimeagen/ansible
  - https://github.com/TalkingQuickly/ansible-osx-setup/blob/master/ansible_osx.yml
- dotfiles
  - https://github.com/geerlingguy/dotfiles
  - https://github.com/ThePrimeagen/.dotfiles
  - https://github.com/kentcdodds/dotfiles
  - https://github.com/thepr/dotfiles
