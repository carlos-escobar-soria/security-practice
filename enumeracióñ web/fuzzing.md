# Fuzzing
Es un ataque por diccionario
``` 
wfuzz -c -t 400 -w [ruta del diccionario] ip/FUZZ
-c -> color de salida
-t -> numero de hilos de ejecucióñ
-w -> diccionario
--hc -> filtra los codigos de erros que no queremos se muestren
```
## doble fuzzing 
```
wfuzz -c -t 400 -w [ruta del diccionario] -w[ruta segudno diccionario] ip/FUZZ.FUZZZ
```
### Recursos movidos 
```
-L indica que navegue al vinculo movido 
```
### requerimiento de login 
-H seguido de la cabecera deceada

```
-h "Cookie" security=impossiblel; PHPSESSID=...." ip
```
