# ansible-dev-setup

My ansible playbook to setup both OSX and Ubuntu environments.
Inspired by Adam Johnson's [mac-ansible](https://github.com/adamchainz/mac-ansible).


## Instructions

### OSX:

1. Install [homebrew](https://brew.sh)
2. `brew install python` (it's better than system python, see [guide](https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/Homebrew-and-Python.md))
3. `pip install ansible` (better than homebrew package as it's always latest)
4. `ansible-playbook playbook.yml`

### Ubuntu:

```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
ansible-playbook playbook.yml -K
```

## What's included?

- Packages (brew/cask or apt/deb) + pip/npm/gem/golang
- Some ubuntu hardware config
- Git config
- Dotfiles
- zsh with [zplug](https://github.com/zplug/zplug)


## What's not included?

- VSCode settings (done via Setting Sync)
- Docker (https://docs.docker.com/docker-for-mac/install/)
