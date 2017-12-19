# csf-wplogin-block
Bloquear todas las ip de fuerza bruta a wp-login.php

mkdir wplogin
cd wplogin
vi wplogin.sh

SCRIPT 
#!/bin/bash

###start editing
thold="100"
btime="359m"
###stop editing

egrep 'wp-login.php' /usr/local/apache/domlogs/* | grep -v ftp_log | awk -F : '{print $2}' | awk '{print $1}' | sort | uniq -c | sort -n | awk -v limit="$thold" '$1 > limit{print $2}' > $$_ip_$$

while IFS= read -r line
        do
                /usr/sbin/csf -td "$line"  "$btime" "banned for wordpress attack"
        done < $$_ip_$$
rm -f $$_ip_$$

EJECUTABLE

chmod +x wplogin.sh

CRON
0 */6 * * * /wplogin/wplogin.sh

