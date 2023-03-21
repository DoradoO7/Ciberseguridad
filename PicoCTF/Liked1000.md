## Objetivos
This [.tar file](https://jupiter.challenges.picoctf.org/static/52084b5ad360b25f9af83933114324e0/1000.tar) got tarred a lot.

## Solucion
Try and script this, it'll save you a lot of time un tip que nos da la pag
import tarfile #Moudle used to work with tar files
```
import tarfile 
for i in range(1000, 0, -1):
	filename = "{}.tar".format(i)
	print(filename) 
	tar = tarfile.open(filename)
	tar.extractall() 
	tar.close()
```
> `picoCTF{l0t5_0f_TAR5}`
## Referencias


