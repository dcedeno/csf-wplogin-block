# csf-wplogin-block
Bloquear todas las ip de fuerza bruta a wp-login.php

# Pasos previos
mkdir wplogin
cd wplogin
vi wplogin.sh

# EJECUTABLE
chmod +x wplogin.sh

# AGREGAR A CRON
0 */6 * * * /wplogin/wplogin.sh

# FUENTE 
Akamaras http://www.akamaras.com/cpanel/how-to-block-brute-force-attacks-against-wp-login-php-on-a-cpanel-server-using-csf/
