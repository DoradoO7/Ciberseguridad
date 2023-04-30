## Objetivos
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/2604f8b51a5cc62d38a3736938f19cef/values)
## Solucion
Aqui abriremos el archivo que nos proporciuona la pagina despues con una herramienta ya hecha corrermos el siguien programa └─$ python RsaCtfTool.py -n 1311097532562595991877980619849724606784164430105441327897358800116889057763413423 -e 65537 --uncipher 861270243527190895777142537838333832920579264010533029282104230006461420086153423

utf-8 : picoCTF{sma11_N_n0_g0od_13686679}

## Referencias
[video que explcia la instalacion ](https://www.youtube.com/watch?v=Qo4fPZxJK30)
