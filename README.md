docker run -it --restart always -d -p 80:80 --name cdn -v /home/isbo/cdn/conf/nginx.conf:/etc/nginx/nginx/conf.ro -v /home/isbo/cdn/conf.d:/etc/nginx/conf.d -v /home/isbo/cdn/html:/usr/share/nginx/html -v /home/isbo/cdn/logs:/var/log/nginx -v /home/isbo/cdn/ssl:/etc/nginx/ssl nginx

sudo mount -t cifs -o rw,vers=3.0,credentials=/root/.smbcredentials //192.168.1.219/Cdn /home/isbo/cdn/html

//192.168.1.219/Cdn /home/isbo/cdn/html cifs -o rw,vers=3.0,credentials=/root/.smbcredentials