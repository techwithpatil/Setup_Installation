Install Docker on Ubuntu 22.04 🐳
Update existing packages 🔄
sudo apt update

Install prerequisite packages for HTTPS access 🔒
sudo apt install apt-transport-https ca-certificates curl software-properties-common

Add GPG key for the Docker repository 🔑
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

Add Docker repository to APT sources ⬇️
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Update package list for the repository addition to take effect 🔄
sudo apt update

Check Docker candidate version ⚙️
apt-cache policy docker-ce

Install Docker 🐳
sudo apt install docker-ce

Check Docker status 🚀
sudo systemctl status docker
