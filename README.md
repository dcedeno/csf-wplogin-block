# csf-wplogin-block
Bloquear todas las ip de fuerza bruta a wp-login.php

# Pasos previos
Crear directorio y archivo
* mkdir wplogin
* cd wplogin
* vi wplogin.sh

# Ejecutable
chmod +x wplogin.sh

# Agregar a Cron
0 */6 * * * /wplogin/wplogin.sh

Fuente

Akamaras http://www.akamaras.com/cpanel/how-to-block-brute-force-attacks-against-wp-login-php-on-a-cpanel-server-using-csf/
