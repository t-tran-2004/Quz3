section .text
	global _start

_start:
	mov eax, num
	mov ecx, eax
	jmp loop

loop:
	dec ecx
	mul ecx
	cmp ecx, 1
	jg loop
	jmp exit

exit:
	mov eax, 1
	int 0x80

section .data
	num EQU 10
