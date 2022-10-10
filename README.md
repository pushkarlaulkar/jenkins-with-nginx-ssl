Before creating the below file, you will need to have a domain with LetsEncrypt encryption

After you have a domain, run below command

```
yum install epel-release -y
```
```
yum install certbot python3-certbot-nginx -y
```

```
certbot --nginx -d your_domain -d www.your_domain
```

Add [jenkins.conf](https://github.com/pushkarlaulkar/jenkins-with-nginx-ssl/blob/main/jenkins.conf) to /etc/nginx/conf.d

Afterwards restart nginx service

If you encounter Bad Gateway try below command


```
setsebool -P httpd_can_network_connect 1
```
