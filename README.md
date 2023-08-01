### Run Traefik V2, Wordpress, MariaDB using Cloudflare Full SSL/TLS encryption mode.  

Install docker and docker compose  

cp docker-compose.yml to a folder  

Replace letsencrypt email, cloudflare email/apikey, wordpress user/passwords/database, mariadb user/passwords, make sure <password1> matches on both images.  

To run  
```
docker compose up -d
or
docker-compose up -d
```
Login at examplewebsite.com/admin with default username: user and password: bitnami, add new user, login to new user and delete the default user.  

Once you are done find a great graphics designer such as https://surefirestudios.io to build your website out. Mention my github and get 5% off.
