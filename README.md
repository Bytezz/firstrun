# Fedora Post-Installation Setup Script

This script automates the setup of a Fedora system, including enabling repositories, installing essential software, and configuring devices.
It's designed to run after a fresh installation of Fedora, helping users quickly set up their environment according to their needs.

## Components Configured

- Device settings
- - Change hostname
- - Setup a second drive
- Drivers / repos
- - Fedora multimedia codecs
- - Enable RPM Fusion free and non-free
- - Install nVidia drivers
- - Install additional codecs
- - - Intel/AMD/nVidia hardware accellerated codecs
- - Install Flatpak and add Flathub repo
- Install FOSS software
- - git
- - Syncthing
- - VSCodium (from https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo)
- - Signal (from Flathub)
- Install non-FOSS software
- - Steam (from rpmfusion-nonfree)
- - Discord (from rpmfusion-nonfree)

## Usage

1. **Clone the repository or download the script**:  
```bash
git clone https://github.com/mortalic/firstrun.git
cd firstrun
```

3. **Run the script**:  
```bash
sudo ./firstrun.sh
```

**Or, if you are lazy, here is a oneliner with curl**:  
```bash
curl -s -o- https://raw.githubusercontent.com/mortalic/firstrun/main/firstrun.sh | sudo bash
```

## Requirements

- Fedora Linux (the script is tested on Fedora, adjustments might be necessary for other distributions).
- Root permissions are required for most operations.

## Customization

The script uses several global variables (`USERNAME`, `GROUP`, `PERMISSION`, `NEWHOSTNAME`, `PRETTYHOSTNAME`, `DRIVELABEL`) to configure system settings.
You can modify these variables to suit your specific requirements. Example:  
```bash
sudo NEWHOSTNAME=superpc PRETTYHOSTNAME="damn fast pc" ./firstrun.sh
```

## Contributions

Contributions to the script are welcome.
Please ensure to test changes locally before submitting a pull request.

## License

GPL 3.0

## Contact

For bugs, feature requests, or other communications, open an issue, or better, open a Pull Request with the fix.
