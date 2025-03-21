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

Default password for user is `ndlrfz`. Password generated via `mkpasswd --method=sha-512`. This command part of the `whois` package.

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
- [x] Implement handler correctly
- [x] Implement password encrypt

## TODO

- ~~Clean package cache~~
- ~~Revert sudoers~~
- Additional packages:
  - ~~KVM: qemu-full and UEFI support~~
  - ~~Browser: brave-bin firefox speech-dispatcher hunspell-en_US~~
  - ~~Yay: betterlockscreen xidlehook curtail-git i3-scrot ymuse-bin~~
  - ~~Thunar tumbler etc~~
  - ~~pfetch light via AUR~~
  - ~~ttc-iosevka noto-fonts noto-fonts-emoji~~
  - ~~Vagrant~~
  - cursors `simp1e cursor`, `breeze-xcursor`
  - Adding material font for mpv
  - ~Add `intel-media-driver`~
  - Add grub theme and plymouth
- ~Setup password encrypted for user~
- ~~Additional packages: `xclip`, `i3-scrot` (aur)~~

## NOTE

- `linux-zen` and VirtualBox? Use the `virtualbox-host-dkms` package.
