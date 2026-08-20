# scripting en nmap
Nmap tiene scripting  por defecto que se encuentran en `/usr/share/nmap/scripts`

los script tienen 14 categorias
1. auth
2. broadcast
3. brute
4. default
5. discovery
6. -dos
7. -exploit
8. external
9. fuzzer
10. intrusive
11. malware
12. safe
13. version
14. vuln
```
nmap --script-help [script| categoria]
nmap --script-help sage
```
tambien se puede consultar por patron textual 
`nmap --script-help "mysql* and sage"`

## ejecución de una categoría completa de scripts considerados seguros y no invasivos 
```
nmap --script safe ip -V
nmap --script "sage and http-*" -V -d 
```

## script para smb
- smb-protocols
- smb-enum-discovery
- smb-enum-users
