# LEVEL 16-17

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## LLAVE
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
## Datos acceso
ssh bandit16 @bandit.labs.overthewire.org -p 2220
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solucion
```bash
bandit16@bandit:~$ nmap -sV -T4 -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-28 00:27 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00014s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31790-TCP:V=7.80%T=SSL%I=7%D=2/28%Time=63FD4A76%P=x86_64-pc-linux-g
SF:nu%r(GenericLines,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20cu
SF:rrent\x20password\n")%r(GetRequest,31,"Wrong!\x20Please\x20enter\x20the
SF:\x20correct\x20current\x20password\n")%r(HTTPOptions,31,"Wrong!\x20Plea
SF:se\x20enter\x20the\x20correct\x20current\x20password\n")%r(RTSPRequest,
SF:31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20password\
SF:n")%r(Help,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x
SF:20password\n")%r(SSLSessionReq,31,"Wrong!\x20Please\x20enter\x20the\x20
SF:correct\x20current\x20password\n")%r(TerminalServerCookie,31,"Wrong!\x2
SF:0Please\x20enter\x20the\x20correct\x20current\x20password\n")%r(TLSSess
SF:ionReq,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x20pa
SF:ssword\n")%r(Kerberos,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x
SF:20current\x20password\n")%r(FourOhFourRequest,31,"Wrong!\x20Please\x20e
SF:nter\x20the\x20correct\x20current\x20password\n")%r(LPDString,31,"Wrong
SF:!\x20Please\x20enter\x20the\x20correct\x20current\x20password\n")%r(LDA
SF:PSearchReq,31,"Wrong!\x20Please\x20enter\x20the\x20correct\x20current\x
SF:20password\n")%r(SIPOptions,31,"Wrong!\x20Please\x20enter\x20the\x20cor
SF:rect\x20current\x20password\n");

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 98.79 seconds

bandit16@bandit:~$ openssl s_client --connect localhost:31790
CONNECTED(00000003)
Cant use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 24 22:59:05 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 24 22:59:05 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 24 22:58:05 2023 GMT; NotAfter: Feb 24 22:59:05 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEXaCVVzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjI0MjI1ODA1WhcNMjMwMjI0MjI1OTA1WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDP
cZ+PR+x7nAI6TVhZvc6x5//nXHJUZnIv2kf6x8SOY5al5BV8I5njUSVQef9fQNE2
JlBdoYNJ65jgzYWrVqPCObCqrPsHZHf8pMD/iElYUcD5u/qtNReuVPfeYefxCvBg
Cy0MltMiLGskDn3rDSwCRWNB2jr9+jQYa7rIGDyWCAq4WH/IsWtF6tan25Bqe6tp
LIMJhuAH56EjZ0biNJ3aOgsWHwqS1bBdMzURABvR+PZc0mikWaNjb2R0d8v0gJTf
qz0qkea6IstFSfwEu2FdslmDZ8PWlIwexw3erL+Ae0L2mFhdf3g1nkUARl8R0Bbe
L9/rtYsV7dF3KG7CFJbbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBH
HpXhIirw6+X3VNmrtXw7HjpriGDA1UTjP2yfeu2YuLIm83iUpz3HuiiwsfJJX9HY
VeDQnJjgMekib2qbq99OHkz+4jFKpw0zR7wTa9K8fifkrQHW/KJOVg1fmJCyFl+j
LF06QYp5f8yA+I2ICGKuNSXd3NvYEVh0tWVXemx/oXqQLHUFBjWNcyBDfCnfZIfe
jhHPhGj/9DuJJWx1lBEOIFHrfOj2uge0R5YZvU0kEm3IQ6iabWM2JF8MHOWWYX8s
wXL4aeNo+K4lnz3wjqnRfSClTwTo9zvaaq+Ym8UxPx3w7SmAU3CXbLh/ukYR6xYp
YEsSAXuYvKkxrTvey2Ik
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 3E1E7188984838866AB55B2C8469084EB58F2DA56E06B35DB5DB6CFFBCCCDAAE
    Session-ID-ctx:
    Resumption PSK: C15972A5321DBE3FB72CCAA2D5B0E88529A1654D3F739B574C0D92DAD09A74CC41BD52E77C2CE286BBF1A4A77150A536
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 70 f2 f5 0a f4 da 59 2b-66 40 bc 3c 8d 67 67 76   p.....Y+f@.<.ggv
    0010 - 0d d2 c9 c4 19 54 e2 4a-b8 25 48 35 01 24 ad 6c   .....T.J.%H5.$.l
    0020 - 83 03 85 a1 94 ec d2 68-69 c5 d4 79 82 09 bb b4   .......hi..y....
    0030 - 7f 51 35 8d 57 7d 2f 01-bf be 19 a6 45 ef b3 20   .Q5.W}/.....E..
    0040 - ba b9 f8 0d 58 3e b4 bf-a1 f8 b7 ac 10 e3 c0 a4   ....X>..........
    0050 - fe 2c ff 84 dc e3 5b 6f-c1 1d e2 af 13 24 e3 47   .,....[o.....$.G
    0060 - 16 89 94 a9 5a a7 c9 83-0a 7f fa 53 30 ff c5 70   ....Z......S0..p
    0070 - 42 06 dd e3 b4 03 ad 97-c5 2d 7e 47 e9 2a 7c af   B........-~G.*|.
    0080 - 3d b6 ea 59 f4 4a 14 5c-cc 7e f3 d6 6d 30 3a cc   =..Y.J.\.~..m0:.
    0090 - 66 11 67 3d b7 e4 4f ab-4e 29 62 33 e5 77 51 90   f.g=..O.N)b3.wQ.
    00a0 - b2 b6 6b a1 e6 82 fc fe-59 11 0f 8b c9 54 30 58   ..k.....Y....T0X
    00b0 - 4a b4 a6 74 e0 d5 dc 2e-9e c6 1e c5 84 fd 64 11   J..t..........d.
    00c0 - 0b 6c d8 04 35 d7 6f 90-e3 96 3c 70 03 7b c3 b4   .l..5.o...<p.{..

    Start Time: 1677544169
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 694BE57C20888D9A36403F054B3A594756C3F8F2BBD68941DFC97756A8047A77
    Session-ID-ctx:
    Resumption PSK: 6136EE9E93AB61BFBF94B41E4FB24CFA75CF776175C49B0EF751908DE82B2ACF3CEE31CEBABCA1F6683420BB03A86A5A
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 70 f2 f5 0a f4 da 59 2b-66 40 bc 3c 8d 67 67 76   p.....Y+f@.<.ggv
    0010 - 67 0b 51 2e e8 1f 35 99-bf 80 f3 1d fc 92 9a 99   g.Q...5.........
    0020 - 1a ac fd f1 3b e7 39 f1-14 65 b1 ca 67 cb ed e0   ....;.9..e..g...
    0030 - 0c 44 fb 95 e8 f9 0f fc-f9 0e e4 3a 52 5c d2 e9   .D.........:R\..
    0040 - ff 5b b7 07 81 78 28 cd-05 75 cd ec f7 3e dc 06   .[...x(..u...>..
    0050 - de d2 c5 24 b9 d4 95 6b-8d 8d 1d c5 59 a1 bb eb   ...$...k....Y...
    0060 - 5e 95 5c e6 9d 9c bc ad-6b c9 0d 1d c8 6d 5e 41   ^.\.....k....m^A
    0070 - 32 77 c2 92 cb e0 b1 63-1d e5 6d 3a d7 5b 44 5f   2w.....c..m:.[D_
    0080 - 7a 18 21 f5 43 6f 55 5e-21 7f 0a 75 ef 6c 7c ae   z.!.CoU^!..u.l|.
    0090 - 4b 94 d9 50 df 3b 58 45-da 03 42 7d c1 ff 47 ca   K..P.;XE..B}..G.
    00a0 - b1 ca 14 d5 8b 87 4f 8e-07 07 b8 cf 68 d0 be 33   ......O.....h..3
    00b0 - 68 b6 0b 3d 93 0d 55 28-77 b9 33 b8 61 25 a2 2e   h..=..U(w.3.a%..
    00c0 - 21 29 7e c1 e2 fb ba 84-7b 6c 57 2c a2 0e 1e a9   !)~.....{lW,....

    Start Time: 1677544169
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$exit


C:\Users\DELL ALL>ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220
```

## Notas adicionales

## Referencias

