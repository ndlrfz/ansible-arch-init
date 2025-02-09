# Ansible Roles for Arch Linux Workstation

This roles used to configure my Arch Linux workstation.

## How to Use this script?

Install `ansible`, `openssh`, and `git`.

```bash
sudo pacman -S openssh ansible git
```

Start SSH.

```bash
sudo systemctl start sshd
```

Generate SSH Key for localhost.

```bash
ssh-keygen
```

Clone repository.

```bash
git clone https://github.com/ndlrfz/ansible-arch-init.git
```

Execute the script.

```bash
cd ansible-arch-init
ansible-playbook -i hosts site.yml
```

## Roadmap

- [x] Install base packages (that I need)
- [x] Install MATE Desktop
- [x] Install i3
- [ ] Install KVM Libvirt with Vagrant
- [x] Deploy my dotfiles
- [ ] Implement alias

## TODO

- ~~Clean package cache~~
- ~~Revert sudoers~~
- Additional packages:
  - KVM: qemu-full and UEFI support
  - ~~Browser: brave-bin firefox speech-dispatcher hunspell-en_US~~
  - ~~Yay: betterlockscreen xidlehook curtail-git i3-scrot ymuse-bin~~
