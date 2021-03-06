# Create Package for Vault on Linux

- [ ] Run the package creation script ` safe_vault/installer/linux/scripts/create_packages.sh` in the `safe_vault` repository
- Check RPM (on e.g. a Fedora test machine)
  - Check installer can upgrade an existing version which is running
    - [ ] Check test machine has older version already installed and `safe_vault` is running
    - [ ] Copy the current bootstrap and config files
    - [ ] New installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check installer can upgrade an existing version which is not running
    - [ ] Check test machine has older version already installed and `safe_vault` is NOT running
    - [ ] Copy the current bootstrap and config files
    - [ ] New installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check installer succeeds on machine with no previous version installed
    - [ ] Check test machine has no version already installed
    - [ ] Installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check repair where current version already installed
    - [ ] Kill and remove existing version of `maidsafe_vault`
    - [ ] Copy the current bootstrap and config files
    - [ ] Installer should rerun without errors
    - [ ] Check `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files haven't been overwritten
    - [ ] Remove bootstrap and config files
    - [ ] Installer should rerun without errors
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check config file is installed in `/var/cache/safe_vault/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
  - Check uninstall
    - [ ] Check `safe_vault` is running
    - [ ] Uninstall should run without errors
    - [ ] Check `safe_vault` is not running
    - [ ] Check `safe_vault`, bootstrap and config files have all been removed
  - [ ] Copy installer from slave to yum repository machine
  - [ ] Update yum repository
  - [ ] Check `yum install safe-vault` works on a clean machine
  - [ ] Check `yum update` updates existing version
- Check .deb (on e.g. an Ubuntu test machine)
  - Check installer can upgrade an existing version which is running
    - [ ] Check test machine has older version already installed and `safe_vault` is running
    - [ ] Copy the current bootstrap and config files
    - [ ] New installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check installer can upgrade an existing version which is not running
    - [ ] Check test machine has older version already installed and `safe_vault` is NOT running
    - [ ] Copy the current bootstrap and config files
    - [ ] New installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check installer succeeds on machine with no previous version installed
    - [ ] Check test machine has no version already installed
    - [ ] Installer should run without errors
    - [ ] Check new version of `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check correct config file(s) are installed to the system cache dir `/var/cache/safe_vault`
    - [ ] Check `safe_vault.crust.config` file has `-rw-r--r--` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files are not present in app support dir `$HOME/.config/safe_vault/`
  - Check repair where current version already installed
    - [ ] Kill and remove existing version of `safe_vault`
    - [ ] Copy the current bootstrap and config files
    - [ ] Installer should rerun without errors
    - [ ] Check `safe_vault` is running and is installed in `/usr/bin/`
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check bootstrap and config files haven't been overwritten
    - [ ] Remove bootstrap and config files
    - [ ] Installer should rerun without errors
    - [ ] Check `safe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
    - [ ] Check config file is installed in `/var/cache/safe_vault/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
  - Check uninstall
    - [ ] Check `safe_vault` is running
    - [ ] Uninstall should run without errors
    - [ ] Check `safe_vault` is not running
    - [ ] Check `safe_vault`, bootstrap and config files have all been removed
  - [ ] Copy installer from slave to apt repository machine
  - [ ] Update apt repository
  - [ ] Check `apt-get install safe-vault` works on a clean machine
  - [ ] Check `apt-get update && apt-get upgrade` updates existing version
