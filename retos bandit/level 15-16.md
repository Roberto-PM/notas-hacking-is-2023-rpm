# LEVEL 15-16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos acceso
ssh bandit15 @bandit.labs.overthewire.org -p 2220
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## info openssl
```bash

Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 06:19:29 2023 GMT; NotAfter: Feb 21 06:20:29 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEA7qUdzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMDYxOTI5WhcNMjMwMjIxMDYyMDI5WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDL
vM0gZzAHdXTeD5t4ruUJo/kRs4UAodA9XcqDhNtW464W0c55RqKLp921syy3Lvjr
8Q9WkqvCFX+efShMd8XnzbT/dyRrD+cZQnSiPJ3bwDdpwqfkl9h3mb609Kb5HI6R
JgogEyuRLJI+HKtr/wXHwo1vBZ0+yaPMX6sdkd6Hu5Ra0L5Q5+E5+3F/8QgvCeVE
hDRIOrh2a7jxykb8G6+xVC6jIZY0YfrZz6LrESyQau256pqyaQPqQoUWTlitxIql
Ym2Baw7vYDxmFZrvj0FkumC6NokX6K2G9bZ0DaKR/DspPdAC4oT81SawJvsBibdN
51VI6dxBn412ZS8bS155AgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQA9
skxWNwZbedjaVTa5yMPUZQ4Nf5/LAAMtS5Q7mzGH5tdQsTGR0Z4n4eA4hzrmzHBF
MVRL5mR9n+sM5pIrKDa6f4zIc5ObxDyN19ie+3SFASCPz9tihK8Js2V8qsR6LHV1
pfD8DSG0hZPtUuK3Mfi+nWqQUFiiTGj30mb9vlS1sSWv5PGznou1gQ3ZfrDs7B4K
ZKZrllPIVV1CrlDw2Bv8Dc432LQuZAmKAjBd6FG0OAboU/WJMTwAfVjlKMtvC8tg
DZ3djSTprq6PrXlI0utw/MsMIh69b61BRXUuDvRxhU11SNmSI8aegjVL8KuK+Euh
sSLPTocV29SY1YXOwEQi
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
    Session-ID: 61942E256458304454C7843FE2F7949F4008058F48F7D858ADF4A3D65C6AC459
    Session-ID-ctx:
    Resumption PSK: 38FCA5E8A3FDD4AEAFE112CF9E4CA3803D52D6EF90E880CF2DCCFB988D8C52F43D81306B4F85047EFB15E6737ECDC810
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - f6 4b e7 cf f0 b5 28 7f-3c 83 f3 4a fc 5a 83 da   .K....(.<..J.Z..
    0020 - 1e 50 a6 21 3c 48 99 26-31 7e 29 a9 d6 7d 04 51   .P.!<H.&1~)..}.Q
    0030 - 51 a8 c3 bd 67 c5 26 56-a1 9c 82 98 e8 1d 27 91   Q...g.&V......'.
    0040 - cb e0 aa e2 31 32 bc 5d-95 60 78 9a 9c ee 70 e7   ....12.].`x...p.
    0050 - 44 43 30 c9 44 94 54 6b-2e ec fd 88 09 e4 4b 5d   DC0.D.Tk......K]
    0060 - 2e 65 e3 0b 36 f7 60 a0-ae a5 b6 d2 f1 d8 bc b6   .e..6.`.........
    0070 - 15 52 fc a3 8b df 5a 96-47 5e e9 77 b0 25 f1 7f   .R....Z.G^.w.%..
    0080 - 67 08 32 37 17 8c c4 2e-99 44 fc 07 74 d1 59 ae   g.27.....D..t.Y.
    0090 - e3 da 78 e8 0b 46 a5 4d-08 00 c0 be 20 80 e9 6d   ..x..F.M.... ..m
    00a0 - 75 80 40 9d 82 7f 0b 8d-71 0f 4f 02 f4 0a 75 e9   u.@.....q.O...u.
    00b0 - 78 54 f9 79 7a c2 be d2-94 64 21 52 36 d8 f3 91   xT.yz....d!R6...
    00c0 - e8 e4 5a eb 52 c8 13 32-c3 30 d5 44 2e 8f e7 a3   ..Z.R..2.0.D....

    Start Time: 1677007670
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
    Session-ID: 276FEB84C6831BF5562977C960CD3F75602A50CC9D6A966EB4653EF9C7E9B568
    Session-ID-ctx:
    Resumption PSK: 1F05275BA2E81313EE96F103A86ADC102A2C9DE361C98E694F387F77755BBD3D07D9C32014CE825F303BE24F87D962C7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - ee ae 09 e4 56 06 6c 9e-c9 80 86 77 50 83 15 59   ....V.l....wP..Y
    0010 - 33 e4 11 a9 6a d8 9e 10-28 68 f6 58 44 10 29 8d   3...j...(h.XD.).
    0020 - bc 97 ed 8a 34 d0 c5 79-8d 81 13 ed 25 24 1a dc   ....4..y....%$..
    0030 - f5 b5 4e 80 8d e7 aa a3-77 66 6a cc 6b d4 1f fe   ..N.....wfj.k...
    0040 - 81 55 b3 55 b0 ee e4 f4-b9 1a 19 cf f3 4e e6 75   .U.U.........N.u
    0050 - b1 82 a5 6d cb 35 0e cf-b0 41 8c 0f 16 83 dd 54   ...m.5...A.....T
    0060 - 5e 16 55 ab ae f5 6d d0-d5 54 ec 4a 8c 37 6f e4   ^.U...m..T.J.7o.
    0070 - b9 fd ae ea 15 2f b0 90-b4 6f 50 81 c7 93 40 2d   ...../...oP...@-
    0080 - 55 e1 26 09 9c b1 0c 79-75 31 9b 95 a5 d6 ae 9c   U.&....yu1......
    0090 - 27 45 a2 e4 a6 10 d3 bb-c0 83 e7 97 cf a8 a3 24   'E.............$
    00a0 - bd e0 69 a8 76 2d 18 57-0d bd a5 7b eb e4 e8 18   ..i.v-.W...{....
    00b0 - ca 21 f7 4c ba 3a 3a 10-47 ef 2b 41 d5 fe 7f 37   .!.L.::.G.+A...7
    00c0 - 6e 03 f8 bb 18 48 d0 45-60 0d a4 1c 97 e5 e3 83   n....H.E`.......

    Start Time: 1677007670
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
```

## Solucion
```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 06:20:29 2023 GMT
verify return:1
---
abre el info opensssl
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$

```


## Notas adicionales
----
OpenSSL es un proyecto de software libre basado en SSLeay, desarrollado por Eric Young y Tim Hudson. Consiste en un robusto paquete de herramientas de administración y bibliotecas relacionadas con la criptografía, que suministran funciones criptográficas a otros paquetes como OpenSSH y navegadores web.
______
The **s_client** command implements a generic SSL/TLS client which connects to a remote host using SSL/TLS. It is a _very_ useful diagnostic tool for SSL servers.

## Referencias
https://es.wikipedia.org/wiki/OpenSSL
https://www.openssl.org/docs/man1.0.2/man1/openssl-s_client.html
https://linuxhint.com/openssl-s-client/
