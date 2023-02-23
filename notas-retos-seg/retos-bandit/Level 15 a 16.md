level 15
# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
# Datos  de Acceso 
ssh bandit15@**bandit.labs.overthewire.org** -p2220

User: bandit15 Pass: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
# Solucion 

```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:56 2023 GMT; NotAfter: Feb 21 22:03:56 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEF3vcjDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU2WhcNMjMwMjIxMjIwMzU2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCg
1elREdWTbtCZNl7KNMjleNrcG71f9lZhjAfM4x+TDwlPpT+Q9O3V6J687fJdMH85
xfUwcZG0XFCeN1nxnmQadGF/ZHEt0laWmCQfo5LogzgGFcaZWC1a6XZ5ZKv7SRDt
tvPK/CTKwOJD5ZJVEXEk9R8YQ/VbKwZMDc43WD/HKypvBv7fZVbJkKYY75LOby86
7gux29Emhntj5pZyYagYbmonnAiw6447bGTC1d6jilGPhXMzckTI57WGeNdp4ppL
3pXSVDLOU2XJ8Um/L2VIgGTsUk5CwrtzVxyt6I5sKavUhsNGlzqvHI/McgbsnHi8
3LDg9k/Co8F21eZFooVlAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBz
lgp6XhMshglRxhxHRg1xHkVYSFSBaS5Adq5OIoE/oetyedTiO2B9MLmNZ9Juu/WK
/+WZFmNdzQ6Iw5ueBz/rmY+DvzTjjd4CPPqeilG5mngceR5nliM9mXkpQlmm3T1a
8JuBrDugrN9BP4IeBTER0pgQcQvsRATrv/SAVFVBhTSvOKFhoYNEdBzaqxclEjD6
bl3UkzNag/S3iLuv24xoQkMmlFC2afaswkG/cQ4p3BuapuZORjbohUOXS24QDl0z
A2RDFNizi42ZVJ8ZW1qbURZ4n/VbIAi7vRHldPKjC8hYAcdvUekB0schBlc1J06Z
phGCgzTVUzJu9yz8uKzO
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
    Session-ID: E255269F3D9513438D8B303ECEF84882798FDBAA9AB6153104C2AC2B5F515FF4
    Session-ID-ctx:
    Resumption PSK: 9FB74445A93540CA0A19D6AFC60A2432B07EE2C653918D55EFABC0C02AEA118F812751F5694DA57BE35F4BCE0CC70767
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - e3 28 4d 2b e3 20 dd 81-85 cc 31 51 c2 6c cc bc   .(M+. ....1Q.l..
    0020 - dd b1 ca c8 5f bd e8 70-88 fa ef 56 03 7d b0 d5   ...._..p...V.}..
    0030 - ee 79 b5 f5 19 83 3c 98-1f 8a fc 0a f5 ba 8b 50   .y....<........P
    0040 - bd c2 58 15 eb 1d ca ea-a6 9a 32 f9 93 c6 ae b1   ..X.......2.....
    0050 - f5 5c 11 86 1b 28 58 53-9a a0 7e 49 e0 17 fd 58   .\...(XS..~I...X
    0060 - d3 ea 70 58 41 e5 1b a7-bd 74 6b 00 47 b8 3e c7   ..pXA....tk.G.>.
    0070 - b8 2f 41 c3 d1 f7 68 3d-c2 e1 37 2f d5 2c d7 80   ./A...h=..7/.,..
    0080 - f2 0e ce f0 62 85 0b 89-d5 68 cd 54 62 ea 6d 32   ....b....h.Tb.m2
    0090 - ef 7b 2d dd 6a a3 15 51-97 ee 77 e7 92 87 ec 88   .{-.j..Q..w.....
    00a0 - eb c1 24 c1 dd 5c 27 c5-be cd 15 e5 a9 bf 23 4c   ..$..\'.......#L
    00b0 - 29 5f d9 a2 2f 8f c6 a7-d1 51 cb 9a d3 e0 a3 03   )_../....Q......
    00c0 - 19 95 82 bc 48 a4 30 f0-fa 59 24 18 37 1e c9 f4   ....H.0..Y$.7...

    Start Time: 1677178152
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
    Session-ID: A92E7878C6CD076BC8C6FEDF6305C29E8101A85F012BE145AC545BC5399FA68D
    Session-ID-ctx:
    Resumption PSK: D2C73EFC757D7280AFC2EAA0516832595902DC33A7AFB2268D06970D2CE7254F5240F884CF5479151E0E9BE2624633B9
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - c8 dc d0 8d c7 99 03 e5-65 ab ca a2 00 a7 24 35   ........e.....$5
    0020 - 3a bd 8e 14 a5 3e 66 39-a5 d7 07 e7 5b df 6e e8   :....>f9....[.n.
    0030 - c2 4c da e2 8f 2b 6c b6-61 ba e6 6b b5 c4 25 91   .L...+l.a..k..%.
    0040 - 48 97 94 d2 0e c2 06 66-1a b3 a7 0d 86 10 6e 2a   H......f......n*
    0050 - 7b ef 3d 4e 58 08 62 40-39 a2 83 af 23 67 13 0e   {.=NX.b@9...#g..
    0060 - ad 8e 72 33 f3 b1 86 f4-80 78 ab 0b 51 73 19 ea   ..r3.....x..Qs..
    0070 - 36 ea 2c 51 e8 65 5e 56-f2 03 96 d3 d0 7b 7d 77   6.,Q.e^V.....{}w
    0080 - 1a e3 63 54 04 49 dc 6f-c4 d2 5b 53 7d 0e 0d c3   ..cT.I.o..[S}...
    0090 - 0b e9 22 72 3e 67 bb bd-d8 bd 68 d3 e3 8b 2b f2   .."r>g....h...+.
    00a0 - 7c 3f c1 4a fa 63 1f 8c-19 04 14 46 9f 2a b5 eb   |?.J.c.....F.*..
    00b0 - 92 4b 62 fe 38 5e d8 ac-c4 71 aa a0 48 70 69 b2   .Kb.8^...q..Hpi.
    00c0 - 0b 18 1c 7a 24 da da 39-12 5a 74 4c 2c be f9 78   ...z$..9.ZtL,..x

    Start Time: 1677178152
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$


```

# Notas Adicionales
