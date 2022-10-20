# Ubuntu-comandos

Update da máqina:
```
$ sudo apt update
```

Atualizar a máquina:
```
$ sudo apt upgrade
```

Instalar o Apach2(porta 80):
```
$ sudo apt install apache2
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
echo "Bem vindo a www.example.pt!" > example/index.html
```

Criar a sua propria página:
```
1.
 cd /etc/apache2/sites-available
2.
 cp 000-default.conf example.conf
```

Ativar o website e desativar o default:
```
cd etc/apache2/sites-enabled/

a2dissite 000-default.conf 

a2ensite example
```
Para usar nomes de dominios existentes:
```
1.
nano /etc/hosts

2.
ipprivado + dominio
```

