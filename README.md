# How to update the website:

```bash
cd /var/www/kcod-website
git pull
sudo hugo
sudo nginx -t && sudo systemctl reload nginx
```