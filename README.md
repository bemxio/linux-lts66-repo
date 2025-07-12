# linux-lts66-repo
A custom [Arch Linux](https://archlinux.org/) repository for the [Linux LTS 6.6](https://aur.archlinux.org/pkgbase/linux-lts66) kernel, automatically checked daily and updated upon a new release. Made it for personal use, since my sound card has problems with kernels 6.8 and above, and I wanted to automate the process of compiling it. Hopefully, it can be useful for someone else that has similar issues!

## Usage
To use this repository, firstly import my GPG key:
```bash
pacman-key --recv-key D6BA2CBC66075B2B
pacman-key --finger D6BA2CBC66075B2B
pacman-key --lsign-key D6BA2CBC66075B2B
```

Then, add the following lines to your `/etc/pacman.conf`:
```
[linux-lts66]
Server = https://linux-lts66.bemxio.xyz/
```

After that, simply update your system, and proceed to install the kernel!
```bash
pacman -Syu linux-lts66 linux-lts66-headers
```

## License
The [workflow script](.github/workflows/main.yml) is licensed under the MIT License - see the [`LICENSE`](LICENSE) file for details.

Contributions are welcome! If you want to contribute, whether it's an issue you've encountered or a pull request with new features, feel free to do so.