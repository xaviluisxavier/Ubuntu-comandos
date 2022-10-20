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





