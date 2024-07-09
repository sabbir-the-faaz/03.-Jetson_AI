# 03.-Jetson_AI-Swaping-memory-
```
sudo systemctl disable nvzramconfig
sudo fallocate -l 8G /mnt/8GB.swap
sudo chmod 600 /mnt/8GB.swap
sudo mkswap /mnt/8GB.swap
sudo swapon /mnt/8GB.swap
echo '/mnt/8GB.swap swap swap defaults 0 0' | sudo tee -a /etc/fstab
```
These commands will:

Disable the nvzramconfig service.
Create an 8GB swap file at /mnt/8GB.swap.
Set the correct permissions on the swap file.
Set up the swap area on the file.
Enable the swap file immediately.
Add the swap file to /etc/fstab so it is enabled at boot time.
