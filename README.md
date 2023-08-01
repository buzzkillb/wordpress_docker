### Run Traefik V2, Wordpress, MariaDB using Cloudflare Full SSL/TLS encryption mode in a simple single Docker Compose  

Install docker and docker compose  

copy **docker-compose.yml** to a folder like ~/wordpress-compose  

Replace letsencrypt email, cloudflare email / global_apikey, wordpress user/passwords/database, mariadb user/passwords, make sure **_password1_** matches on both containers.  Example shows how to use root user for Bitnami containers, otherwise the containers use UUID 1001.

To run  
```
docker compose up -d
```
Login at examplewebsite.com/admin with default username: **_user_** and password: **_bitnami_**, add new user, login to new user and delete the default user.  

Once you are done find a great graphics designer such as https://surefirestudios.io to build your website out. Mention my github, **_buzzkillb_**, and get 5% off.

### Install Docker Ubuntu 22.04  
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce
sudo usermod -aG docker ${USER}
su - ${USER}
exit
docker version
```

### Install Docker Compose Ubuntu 22.04  
```
mkdir -p ~/.docker/cli-plugins/
curl -SL https://github.com/docker/compose/releases/download/v2.3.3/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose
chmod +x ~/.docker/cli-plugins/docker-compose
docker compose version
```
