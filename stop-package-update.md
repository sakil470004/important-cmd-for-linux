# Stop linux update
sudo apt-mark hold <linux-package-name>
## Example  
sudo apt-mark hold linux-image-generic linux-headers-generic
sudo apt-get update
  
# Enable linux package update
sudo apt-mark unhold linux-image-generic linux-headers-generic
