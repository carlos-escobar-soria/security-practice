# Detecion de servicos con nmap
Identificar la un purto y su version nos permite buscar su  vuulnerabilidad
```
-sv -> indica que extraiga la version del poftware por cada puerto
nmap -sV ip
nmap -sV --version-intensity [0-9]
```
# Escaneo agresivo 
```
nmap -A scanme.nmap.org
nmap -sV -sC -O scanme.nmap.org
```
## busqueda de explot de un software por su nombre y versión
para esto utilizamos la herramienta **seachsploit**
`searchh exploit vsftpd 2.3.4`

