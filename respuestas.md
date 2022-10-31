1. 
   ```bash  
  mkdir repositorios
  git clone https://github.com/TecnologoInformatico/AdmInf-web.git repositiorios/repo
   ```
2. apt update
3. sudo apt install apache2
4. mkdir /var/www/lmarrero
5. sudo chown -R $USER:$USER /var/www/lmarrero
6. 
   1. sudo nano /etc/apache2/sites-available/lmarrero.conf
   ```bash
    <VirtualHost *:80>
      ServerAdmin webmaster@localhost
      ServerName lmarrero.tecnologoinformatico.com
      ServerAlias lmarrero
      DocumentRoot /var/www/lmarrero
      ErrorLog ${APACHE_LOG_DIR}/error.log
      CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>
    ```
7. Ya tenia esa configuracion en el archivo
8. sudo systemctl restart apache2
9. cp ~repositorios/AdmInf-web /var/www/lmarrero
10. sudo apache2ctl configtest
11. No se que es lo que tengo que hacer