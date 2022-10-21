# Ubuntu-comandos

Update da máqina:
```
sudo apt update
```

Atualizar a máquina:
```
sudo apt upgrade
```

Instalar o Apach2(porta 80):
```
sudo apt install apache2
```


Verificar se a porta esta aberta:
```
$ ss -tln
```

Visão geral da configuração do apache2:
```
/usr/share/doc/apache2/README.Debian.gz 

/etc/apache2/
|-- apache2.conf
| `--ports.conf
|-- habilitado para mods
| |-- *.load
| `-- *.conf
|-- habilitado para conf
| `-- *.conf
|-- habilitado para sites
| `-- *.conf
          
```
Raízes do Documento  / permissoes   
```
/var/www/html
/etc/apache2/apache2.conf
```

Criar um documento e o rederecionar:
```
mkdir example 

echo "Bem vindo a www.example.pt!" > example/index.html
```

Criar a sua propria página:
```
1.
 cd /etc/apache2/sites-available
2.
 cp 000-default.conf example.conf
3.
<VirtualHost www.example.pt:80>
ServerName www.ociden.pt
DocumentRoot /var/www/example
 
```

Ativar o website e desativar o default:
```
cd /etc/apache2/sites-enabled

a2dissite 000-default.conf 

a2ensite example.conf
```
Para usar nomes de dominios existentes:
```
1.
nano /etc/hosts

2.
ipprivado + dominio

3.
cd /etc/apache2/sites-available

4.
nano example.conf

5. 
#ServerName www.example.com
```

Ativar o https:
```
1.
 sudo a2enmod ssl
 
2.
cd /etc/apache2/sites-available

3.
 cp default-ssl.conf example-ssl.conf
 
4.
<VirtualHost www.example.pt:443>
                
                DocumentRoot /var/www/example
5.
a2ensite example-ssl.conf 

```


# Ubuntu-Cliente


Update da máqina:
```
sudo apt update
```

Atualizar a máquina:
```
sudo apt upgrade
```

Instalar o Ubuntu Cliente:
```
1.
sudo apt install -y xfce4 xfce4-goodies

2.
sudo apt install -y xrdp chromium-browser filezilla

3.
sudo adduser xrdp ssl-cert

4.
sudo adduser maria

5.
login example

6.
echo xfce4-session > ~/.xsession
```







