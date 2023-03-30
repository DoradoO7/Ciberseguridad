## Objetivos
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solucion
usaremos la ayuda q nos dan de How can you decrypt the TLS stream?
busacando TLS y luego 
ssldump -r capture.pcap -k picopico.key -d
picoCTF{nongshim.shrimp.crackers}
## Referencias
[TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security)
