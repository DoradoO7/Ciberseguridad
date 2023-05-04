## Objetivos
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)
## Solucion
Aqui al codigo lo modificaremos un poco y lo pondremos a correr en un emulador 
start:
 	push 0xe54409d5
 	push 0xe6cf51f0
 	push 0xd2c26416
	call asm3

asm3:
		push   ebp
		mov    ebp,esp
		xor    eax,eax
		mov    ah,BYTE PTR [ebp+0x9]
		shl    ax,0x10
		sub    al,BYTE PTR [ebp+0xe]
		add    ah,BYTE PTR [ebp+0xf]
		xor    ax,WORD PTR [ebp+0x12]
		nop
		pop    ebp
		ret    

0x375 es lo que nos queda y esa sera la flag
## Referencias
[Video de solucion](https://www.youtube.com/watch?v=REQOuLONQQc)
[Emulator](https://carlosrafaelgn.com.br/Asm86/)