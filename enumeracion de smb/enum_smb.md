# enumeracióñn smb (server message block)
Protocolo para compartir recursos como archivos, impresoras en general cualquier recurso 
- en window esta funcion es nativa 
- en linux se utiliza samba
## Herramientas 
1. nbtscan -> antiguo pero sirve con netbios-sn -> netbios-ssn -> microsoft-ds
2. enum4linux
3. smbclient
4. rpcclient
5. nmap

Para que samba acepte diferentes versiones debe tener 
```
/etc/samba/smb.conf -> client min procotol = NT
systemctl restart smb
```
### smbmap
```
-H ip host
-P puerto
-V informacion sobre versiones
-U usuario
-P password
-R si hay permiso listar share
```
