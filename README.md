Procedure to install to the folder /docker on a linux machine
<pre>
rm -rf /docker
cd
rm -rf ./mai* ./Nextcloud-main/
docker system prune -f
docker image prune -f
mkdir /docker
wget https://codeload.github.com/YayPeace/Nextcloud/zip/refs/heads/main -o main.zip
unzip ./main
mv ./Nextcloud-main/* /docker
chmod -R 777 /docker/nc_nginx/
cd /docker
docker-compose up -d
</pre>
