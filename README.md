# memo

# sshd
```
sudo nano /etc/nixos/configuration.nix
--
    :
  # Enable OpenSSH daemon
   services.openssh.enable = true;
   services.openssh.permitRootLogin = "no";
   services.openssh.passwordAuthentication = true;
#  services.openssh.port = 22;
   services.openssh.protocol = "2";
    :
--

sudo nixos-rebuild switch
sudo systemctl sshd status   # confirm running

# connect from other hosts
ssh me@192.168.xx.xx
nixos-version                # confirm host
```

# home partition
/etc/fstab
```
UUID=4c8c8b7f-7667-4b60-b9b8-e22d7952e107 /home          btrfs   subvol=home,noatime,compress=zstd 0 0
```


