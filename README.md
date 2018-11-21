# Ansible NGINX Role

> Ansible role for NGINX.


## Tags
* nginx  
Run all tasks
* nginx-install  
Only install package
* nginx-upload-config  
Only upload config files


## Role Variables

```
---
# Install Package
nginx_package: nginx
nginx_cache_dir: /var/cache/nginx/

# Upload NGINX Main Configuration File
nginx_main_config_upload_enable: false
nginx_main_config_upload_src: nginx.conf
nginx_main_config_upload_dest: /etc/nginx/nginx.conf
# Upload NGINX Configuration Files
nginx_config_upload_enable: false
nginx_config_upload_src: conf/*.conf
nginx_config_upload_dest: /etc/nginx/conf.d/
# Upload NGINX Snippet Files
nginx_snippet_upload_enable: false
nginx_snippet_upload_src: snippets/*.conf
nginx_snippet_upload_dest: /etc/nginx/snippets/
# Upload NGINX Server Configuration Files
nginx_server_upload_enable: false
nginx_server_upload_src: sites-available/*
nginx_server_upload_dest: /etc/nginx/sites-available/
nginx_server_upload_link: /etc/nginx/sites-enabled/
# Delete NGINX Default Server
nginx_delete_default_server: false
nginx_default_server_location: /etc/nginx/sites-enabled/default
# Upload NGINX Lua Files
nginx_lua_upload_enable: false
nginx_lua_upload_src: lua/*.lua
nginx_lua_upload_dest: /etc/nginx/lua/
# Upload SSL Certificates and Keys
nginx_ssl_upload_enable: false
nginx_ssl_crt_upload_src:
  - ssl/*.crt
  - ssl/*.pem
nginx_ssl_crt_upload_dest: /etc/ssl/certs/
nginx_ssl_key_upload_src: ssl/*.key
nginx_ssl_key_upload_dest: /etc/ssl/private/
# Upload HTML Files
nginx_html_upload_enable: false
nginx_html_upload_src: html/*
nginx_html_upload_dest: /var/www/html/
# Upload NGINX Logrotate Configuration File
nginx_logrotate_upload_enable: false
nginx_logrotate_upload_src: logrotate/nginx
nginx_logrotate_upload_dest: /etc/logrotate.d/nginx
```
