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
cp ~/.ssh/id_ed25519.pub ~/.ssh/authorized_keys
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

Now change the password for your user.

```bash
passwd username
```

## Roadmap

- [x] Install base packages (that I need)
- [x] Install MATE Desktop
- [x] Install i3
- [x] Install KVM Libvirt with Vagrant
- [x] Deploy my dotfiles
- [x] Implement Vars
- [ ] Implement handler correctly
- [ ] Implement password encrypt

## TODO

- ~~Clean package cache~~
- ~~Revert sudoers~~
- Additional packages:
  - ~~KVM: qemu-full and UEFI support~~
  - ~~Browser: brave-bin firefox speech-dispatcher hunspell-en_US~~
  - ~~Yay: betterlockscreen xidlehook curtail-git i3-scrot ymuse-bin~~
  - Thunar tumbler etc
  - pfetch via AUR
  - ttc-iosevka noto-fonts noto-fonts-emoji
  - Vagrant
  - simp1e cursor
- Setup password encrypted for user
