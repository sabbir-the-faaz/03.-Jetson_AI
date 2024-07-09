sudo systemctl disable nvzramconfig
sudo fallocate -l 8G /mnt/8GB.swap
sudo chmod 600 /mnt/8GB.swap
sudo mkswap /mnt/8GB.swap
sudo swapon /mnt/8GB.swap
echo '/mnt/8GB.swap swap swap defaults 0 0' | sudo tee -a /etc/fstab
