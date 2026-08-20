# Descubrimiento de host activos 
para esto utilizaremos nmap 
-Pn no hace nada, se mira todos los puertos de los host 
-PS Scaneo SYN
-PA escaneco ACK 
-PU escaneo UDP 
-sU udp
-sF dondeo tcp fin 
-sN dondeo null
-sX sondeo Xmas
-sA sondeo tcp ACK
-sM sondeo Maimon

-PE -> ICMP echo
-PP -> timestamp
-PM -> netwok request
-PO [protocol list]: IP Protocol ping 

## Evitando un IDS 
cabe mensionar q esta en una forma 
```
nmap -PA scanme.nmap.org
```
## Descubrimiento ARP
```
nmap -PR ip-red/24
nmap -PR ip-red/24 --send-ip -> utilizamos el --send-ip si estamos en la misma ip
```

### Ejemplo por defecto 
```
nmap -PE -PP -PA80 -PS443 scanme.nmap.org
``` 
