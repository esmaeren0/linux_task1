# linux_task1
linux first task, postgresql server, create db and user and permission 


1. POSTGRESQL SERVER KURULUMU
```
 sudo apt update // paketleri güncelleme
```
EOF
```
 sudo apt install postgresql postgresql-contrib // postgresql ve araç kurulumu (postgresql-contrib: Ek araç ve modülleri kurar.)

 sudo systemctl status postgresql // active değilse start command ile aktifleştirerek tekrar durumu konrtol et.
```
2. POSTGRESQL'E GİRİŞ VE DB OLUŞTURMA
```
sudo -i -u postgres // postgres kullanıcısına geçiş
 psql // postgres shell'e giriş
 CREATE DATABASE odevdb ;
 /q // postgres shellden çıkış
 exit // home dönüş
 cat /etc/passwd // kullanıcıları listeledi (grep postgres ile sadece postgres kullanıcıları gözükür)
```
   output: odevuser:x:1004:1004:odev user
   * 2,2,2,2:/home/odevuser:/bin/bash

3. KULLANICI OLUŞTURMA VE YETKİLENDİRME
```
sudo adduser odevuser
sudo visudo
servisci ALL=(ALL) NOPASSWD: /bin/systemctl restart * // kullanıcı sadece yeniden başlatma yapabilir stop start yapamaz. 
```
