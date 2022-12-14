# ansible-dev-setup

My ansible playbook to setup both OSX and Ubuntu environments.
Inspired by Adam Johnson's [mac-ansible](https://github.com/adamchainz/mac-ansible).


## Instructions

### Creating a new SSH key (for a new user / machine)

- [Github guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### OSX:

1. Install [homebrew](https://brew.sh)
2. `brew install python` (it's better than system python, see [guide](https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/Homebrew-and-Python.md))
3. `pip3 install ansible` (better than homebrew package as it's always latest)
4. `ansible-playbook playbook.yml`

- Use `--tags "newuser"` if running for a new user on an existing machine setup.

### Other things

- Double click `roles/aaron_common/files/term/spacegray.itermcolors` and follow instructions to use the colour preset.
- [Tree style tark compact dark style](https://github.com/doublejim/tree-style-tab-compact-dark-style)

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
