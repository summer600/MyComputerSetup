# Clean install option for WSL 2 Ubuntu 2004

# Ubuntu 2004 LTS
We begin with the Ubuntu 2004 LTS App in the windows Store. Install that. I assume we have already done the
prerequisites for WSL2, so start Windows Terminal or cmd and type `ubuntu2004`

Choose a suitable username and password and this first tep is done.

# Software

```
sudo apt update

sudo apt install mc
sudo apt install jq

```

# X
Using https://github.com/davidbombal/wsl2 setup xrdp for wsl2

```
sudo apt update -y && sudo apt upgrade -y

sudo apt install xrdp
sudo apt install xfce4
sudo apt install xfce4-goodies
```

# install X410

Using https://x410.dev/cookbook/wsl/using-x410-with-wsl2/#:~:text=%20In%20order%20to%20use%20X410%20with%20Linux,yet%20share%20loopback%20addresses;%20when%20you're...%20More

export the DISPLAY

# install .net 5.0

https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu

```
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

```
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-5.0
```
