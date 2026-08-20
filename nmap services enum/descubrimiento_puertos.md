# descubrimiento de puertos 
para equipos activos 

```
nmap -sn 192.168.1.0/24 
-F (fast) 100 puertos mas populares
--top-ports n -> escanea los n servicos mas frecuentes
--port-radio <radio> -> <radio> esta entre [0-1]
``` 
### Rango de puertos
``` 
nmap -p 22, 80, 443 scanme.nmap.org
nmap -p 1-1000 scanme.nmap.org
nmap -p22 scanme.nmap.org
nmap -p- scanme.nmap.org
```
Nota
   ` -p utilizalo con --mon-rate=5000 (es ruidoso)`

### Técnica para analizar puertos con nmap 
Estas tecnicas tienen como objetivo principal evitar posibles cortafuegos y sistemas de deteccion de instrusos(IDS)
``` 
-sS tcp -> (tcp haf-connect conexiones parcioales, mayor sigilo y eficiente)
-sT connect() -> (menos sigilo y mas lento)
-sA ack
-sW windows
-sM maimon scans
-sU UDP Scan
-sN tcp null
-sF Fin
-sX xmas scans
--scanflags <Flags>: customize TCP scang flag
-sI <zombie host[:probeport]> idle scan
-sY sctp
-sZ cookie-echo scans
-sO ip protocol scan
```

#### UDP 

Problemas cuando se tiene open /filtered
```
-sF -> fin 
-sX -> xmas
-sN -> nul
```
