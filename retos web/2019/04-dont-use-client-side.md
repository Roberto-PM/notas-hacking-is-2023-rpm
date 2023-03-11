# dont-use-client-side


## Descripcion
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` ([link](https://jupiter.challenges.picoctf.org/problem/17682/)) or http://jupiter.challenges.picoctf.org:17682
## Pistas
Never trust the client

## Solucion
con ayuda del inspeccionar elementos de firefox utilizamos el debuger para ver el codigo que verifica la contrasena

if (checkpass.substring(0, split) == 'pico') { if (checkpass.substring(split*6, split*7) == '706c') { if (checkpass.substring(split, split*2) == 'CTF{') { if (checkpass.substring(split*4, split*5) == 'ts_p') { if (checkpass.substring(split*3, split*4) == 'lien') { if (checkpass.substring(split*5, split*6) == 'lz_b') { if (checkpass.substring(split*2, split*3) == 'no_c') { if (checkpass.substring(split*7, split*8) == '5}') { alert("Password Verified") } } } } } } } }
## Bandera
picoCTF{no_clients_plz_b706c5}
picoCTF{}
## Notas adicionales


## Referencias
