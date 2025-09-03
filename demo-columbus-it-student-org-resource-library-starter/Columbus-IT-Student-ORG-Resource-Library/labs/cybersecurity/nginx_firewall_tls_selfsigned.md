# Cybersecurity Lab – Web Server + Firewall + Self-Signed TLS
**Estimated time:** 45–60 minutes  
**Prereqs:** Ubuntu Server VM (22.04+), sudo access  
**Objective:** Deploy nginx, enable UFW, add a self-signed certificate.

## Steps
1) **Install nginx**
```bash
sudo apt update
sudo apt install -y nginx
```

2) **Enable firewall and allow web traffic**
```bash
sudo ufw enable
sudo ufw allow 'Nginx Full'
sudo ufw status
```

3) **Create self-signed cert**
```bash
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048   -keyout /etc/ssl/private/selfsigned.key   -out /etc/ssl/certs/selfsigned.crt   -subj "/C=US/ST=State/L=City/O=StudentLab/OU=IT/CN=localhost"
```

4) **Enable TLS in nginx (default server)**
```bash
sudo tee /etc/nginx/snippets/self-signed.conf > /dev/null <<'EOF'
ssl_certificate /etc/ssl/certs/selfsigned.crt;
ssl_certificate_key /etc/ssl/private/selfsigned.key;
EOF

sudo tee /etc/nginx/snippets/ssl-params.conf > /dev/null <<'EOF'
ssl_protocols TLSv1.2 TLSv1.3;
ssl_ciphers HIGH:!aNULL:!MD5;
ssl_prefer_server_ciphers on;
EOF

sudo sed -i 's/listen 80 default_server;/listen 80 default_server;\n    listen 443 ssl default_server;\n    include snippets\/self-signed.conf;\n    include snippets\/ssl-params.conf;/' /etc/nginx/sites-available/default

sudo nginx -t && sudo systemctl reload nginx
```

5) **Test**
- Browse to `http://<vm-ip>` and `https://<vm-ip>` (accept browser warning for self-signed).

## Validation
- HTTP and HTTPS both load the default nginx page.

## Cleanup
- None.
