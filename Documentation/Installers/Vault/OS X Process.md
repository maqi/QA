# Create Package for Vault on OS X

- [ ] Run Jenkins job `maidsafe_vault_linux_nightly`
- [ ] Check job completed successfully
- Check installer can upgrade an existing version which is running
  - [ ] Check test machine has older version already installed and `maidsafe_vault` is running
  - [ ] Copy the current bootstrap and config files and note the size of the chunkstore/db dirs
  - [ ] New installer should run without errors
  - [ ] Check new version of `maidsafe_vault` is running and is installed in `/usr/local/bin/`
  - [ ] Check `maidsafe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
  - [ ] Check bootstrap and config files haven't been overwritten, `chmod`ded or `chown`ed, and the chunkstore/db dirs are unmodified
- Check installer can upgrade an existing version which is not running
  - [ ] Check test machine has older version already installed and `maidsafe_vault` is NOT running
  - [ ] Copy the current bootstrap and config files and note the size of the chunkstore/db dirs
  - [ ] New installer should run without errors
  - [ ] Check new version of `maidsafe_vault` is running and is installed in `/usr/local/bin/`
  - [ ] Check `maidsafe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
  - [ ] Check bootstrap and config files haven't been overwritten, `chmod`ded or `chown`ed, and the chunkstore/db dirs are unmodified
- Check installer succeeds on machine with no previous version installed
  - [ ] Check test machine has no version already installed
  - [ ] Installer should run without errors
  - [ ] Check new version of `maidsafe_vault` is running and is installed in `/usr/local/bin/`
  - [ ] Check `maidsafe_vault` has `-rwxr-xr-x` permissions and `SAFE` owner name and group name
  - [ ] Check bootstrap file is installed in `/var/cache/maidsafe/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
  - [ ] Check config file is installed in `/etc/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
- Check repair where current version already installed
  - [ ] Kill and remove existing version of `maidsafe_vault`
  - [ ] Copy the current bootstrap and config files and note the size of the chunkstore/db dirs
  - [ ] Installer should rerun without errors
  - [ ] Check `maidsafe_vault` is running and is installed in `/usr/local/bin/`
  - [ ] Check `maidsafe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
  - [ ] Check bootstrap and config files haven't been overwritten, `chmod`ded or `chown`ed, and the chunkstore/db dirs are unmodified
  - [ ] Remove bootstrap and config files
  - [ ] Installer should rerun without errors
  - [ ] Check `maidsafe_vault` has `-rwxr-xr-x` permissions and `safe` owner name and group name
  - [ ] Check bootstrap file is installed in `/var/cache/maidsafe/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
  - [ ] Check config file is installed in `/etc/` has `-rw-r--r--` permissions and `safe` owner name and `root` group name
- Check uninstall
  - [ ] Check `maidsafe_vault` is running
  - [ ] Uninstall should run without errors
  - [ ] Check `maidsafe_vault` is not running
  - [ ] Check `maidsafe_vault`, bootstrap and config files have all been removed
- Check installer can be downloaded
  - [ ] Webpage should detect OS and show link to appropriate installer
  - [ ] Download installer and hash check it against original
  - [ ] Check downloaded filename is meaningful
