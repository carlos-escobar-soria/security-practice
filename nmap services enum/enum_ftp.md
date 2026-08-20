# enumeracion FTP
```
nmap -sV -p21, 2121 ip
nmap -p21,2121 --script banner ip
telnet ip 21
```
## script de nmap para ftp
 1. ftp-anon -> usuario anonimo
 2. ftp-bounce -> nulnerabilidad a escaneos 
 3. ftp-syst -> envia comandos syst y stat (necesita auth)
### nmap aplica los script a todos los puertos y la opcion para ver el error 
`nmap -p21,2121 --script+ftp-syst, ftp-bounce -d`
### Herramientas adicionales
para descargar el contenido de un servidor ftp podemos utilizar 

``` 
    curl ftp://usuario:password@servidor_ftp
    wget -m ftp://usuario:password@servidor_ftp
```
