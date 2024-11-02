# Install Docker on Ubuntu 22.04 🐳

## Update existing packages 🔄
```bash
sudo apt update```

## Install prerequisite packages for HTTPS access 🔒
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common```

## Add GPG key for the Docker repository 🔑
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg```

## Add Docker repository to APT sources ⬇️
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```

## Update package list for the repository addition to take effect 🔄
```bash
sudo apt update```

## Check Docker candidate version ⚙️
```bash
apt-cache policy docker-ce```

## Install Docker 🐳
```bash
sudo apt install docker-ce```

# Check Docker status 🚀
```bash
sudo systemctl status docker```
