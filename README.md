# Maciek's initial macOs setup

Initially, go through initial macOs setup wizard, create local user account, login to iCloud. Once on the macOs desktop do the steps below.

## Install Xcode

```shell
xcode-select --install
```

## Install Ansible using pip

```shell
# Add pip to PATH
export PATH="$HOME/Library/Python/3.8/bin:/opt/homebrew/bin:$PATH"

# Update pip
sudo pip3 install --upgrade pip

# Install Ansible
python3 -m pip install --user ansible
```

## Clone this repository

```shell
git clone https://github.com/sitek94/mac-setup.git
```
