## Welcome to Innovations Groups

We are a multinational company that you help you to simplify your inventory management, and track your needs. 

You can visit our official page (https://innovations-groups.com) to to learn more about our services. 

You will find here the code that help us to get this customer satisfaction going everyday below. 

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block
1- Installing PostgreSQL and Wkhtmltopdf on Ubuntu

$ sudo apt update
$ sudo apt install postgresql
$ systemctl status postgresql
$ systemctl is-enabled postgresql
$ wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb
$ sudo dpkg -i  wkhtmltox_0.12.5-1.bionic_amd64.deb
$ sudo apt -f install 
$ which wkhtmltopdf
$ which wkhtmltoimage

2- Installing Odoo 13 in Ubuntu

$ sudo wget -O - https://nightly.odoo.com/odoo.key | sudo apt-key add -
$ sudo echo "deb http://nightly.odoo.com/13.0/nightly/deb/ ./" | sudo tee -a /etc/apt/sources.list.d/odoo.list
$ sudo apt-get update && apt-get install odoo
$ systemctl status odoo
$ systemctl is-enabled odoo
$ sudo netstat -tpln
OR
$ sudo ss -tpln

3- Install and Configure Nginx as a Reverse Proxy for Odoo

$ sudo apt install nginx
$ systemctl status nginx
$ systemctl is-enabled nginx
$ sudo vi /etc/nginx/conf.d/odoo.conf
server {
        listen      80;
        server_name odoo.tecmint.lan; access_log /var/log/nginx/odoo_access.log; error_log /var/log/nginx/odoo_error.log; proxy_buffers 16 64k; proxy_buffer_size 128k; location / { proxy_pass http://127.0.0.1:8069; proxy_redirect off; proxy_set_header X-Real-IP $remote_addr; proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; proxy_set_header Host $http_host; } location ~* /web/static/ { proxy_cache_valid 200 60m; proxy_buffering on; expires 864000; proxy_pass http://127.0.0.1:8069; } gzip on; gzip_min_length 1000; }
$ sudo nginx -t
$ sudo systemctl restart nginx
$ sudo ufw allow http
$ sudo ufw allow https
$ sudo ufw reload

4- Accessing Odoo Web Administration Interface

Innovations Groups

[Link](https://innovations-groups.com/)

For more details see [the original website with graphics](https://www.tecmint.com/install-odoo-in-ubuntu/).

### The Innovations Groups Developer Team

This site repository can still be access and modify via[repository settings](https://github.com/Innovation-Sarl/Odoo-With-Innovations-Groups/settings/pages). 

### Support or Contact

Having trouble with Pages? [contact support](https://innovations-groups.com/contact-us/) and we’ll help you sort it out.
