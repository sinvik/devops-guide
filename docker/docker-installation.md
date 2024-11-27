## Docker installation Command

  ```bash
  sudo apt update
  sudo apt install -y     apt-transport-https     ca-certificates     curl     software-properties-common
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
  sudo apt update
  sudo apt install -y docker-ce docker-ce-cli containerd.io
  sudo docker --version
  sudo usermod -aG docker priya
  sudo usermod -aG docker $USER
  ```


  ```bash
  #For VM/ Cloud
  sudo systemctl start docker/ sudo dockerd
  sudo systemctl enable docker
  docker status
  ```


  ```bash
  #For WSL
  export DOCKER_HOST=unix:///var/run/docker.sock
  sudo dockerd --iptables=False
  sudo docker info
  ``` 