docker run -it --restart always -d -p 82:82 --name cdn -v /home/isbo/cdn/conf/nginx.conf:/etc/nginx/nginx/conf.ro -v /home/isbo/cdn/conf.d:/etc/nginx/conf.d -v /home/isbo/cdn/html:/usr/share/nginx/html -v /home/isbo/cdn/logs:/var/log/nginx -v /home/isbo/cdn/ssl:/etc/nginx/ssl nginx

---

### /etc/samba/smb.conf:

```
[cdn]
path = /home/isbo/cdn/html
writable = yes
browseable = yes
public = no
```