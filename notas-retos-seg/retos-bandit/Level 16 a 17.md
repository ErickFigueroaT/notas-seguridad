Level 16 

# Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
# Datos  de Acceso 
ssh bandit16@**bandit.labs.overthewire.org** -p2220

User: bandit16 Pass: JQttfApK4SeyHwDlI9SXGR50qclOAil1
# Solucion 

```bash
bandit16@bandit:~$ nmap localhost -p 31000-32000
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 18:56 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00017s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.14 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
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
    Session-ID: 1979C7C4F0B8E9CF01DD72FF5071CC96F5558470039F30F16A060E7915DB16E4
    Session-ID-ctx:
    Resumption PSK: 31C7B9613EF9B737F29348837C72473DF3423642FA7419983099AAA55AAD4259C8B48D5E83EE1C68406A2EE2D8C531C9
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 57 d0 a1 68 bc 5e 7f 30-2e cd e8 87 0f c4 81 ad   W..h.^.0........
    0020 - 59 63 85 6a 5d 2a ad 52-0c d7 0e e6 fd 37 e8 43   Yc.j]*.R.....7.C
    0030 - 73 b0 19 c0 20 72 84 44-f6 f4 38 3a a0 1a e8 1d   s... r.D..8:....
    0040 - ba cf a1 35 b1 9c d1 25-88 09 7d a9 19 04 dd 17   ...5...%..}.....
    0050 - 76 58 52 9a 96 a5 d6 3a-99 17 9a a7 f2 a4 f5 2e   vXR....:........
    0060 - a2 5e fe 0b 01 41 8a 02-57 89 96 5b 92 4f e4 70   .^...A..W..[.O.p
    0070 - 43 68 30 5f f4 fa 5d e4-81 d5 9c 9e c7 6b 9c c4   Ch0_..]......k..
    0080 - 1f ce 71 9e 58 86 a7 6f-b3 f0 c1 17 0d d5 fc 31   ..q.X..o.......1
    0090 - c6 a1 4e fd c1 20 02 49-01 72 fc 62 16 06 28 f8   ..N.. .I.r.b..(.
    00a0 - e7 a5 9c a6 ce a7 cd 8f-f1 a5 ef d3 c4 52 6c a7   .............Rl.
    00b0 - 4f 72 70 77 f6 45 62 d5-37 c7 1b 33 76 84 0b 78   Orpw.Eb.7..3v..x
    00c0 - 01 07 65 b2 e3 b5 07 08-b4 d8 c6 35 f7 55 64 23   ..e........5.Ud#

    Start Time: 1677178591
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
    Session-ID: E8E40C5C71BC474CFAE0A27A476EF2750B7CFFBCEA698EBB450C9D2EB77F4AE3
    Session-ID-ctx:
    Resumption PSK: 75A665DB47C6B72BBAB76F7CB7E478813AC4C09E231CA68E0EB727175EBCF5B1748690348C4CDB87D4458199CEDAF92B
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 1e 0d 7f 70 7b af 86 57-2f a0 bb fc 9d 10 82 80   ...p{..W/.......
    0020 - 7e f6 a1 41 89 61 e5 9d-ee 06 8c 25 a5 9f 65 d8   ~..A.a.....%..e.
    0030 - f1 ce fa bd 4f 8e 28 db-70 91 7d b8 1a b4 4c 4a   ....O.(.p.}...LJ
    0040 - 5c 8c 67 0b 45 81 5f 65-5f 43 36 26 18 4c 85 18   \.g.E._e_C6&.L..
    0050 - 69 cc 39 4e 6c 34 6a e0-4b 7e 03 67 f1 2d 4d 05   i.9Nl4j.K~.g.-M.
    0060 - 29 ac 84 58 b3 7a ab 7e-bf ed d3 8a 94 47 a4 1d   )..X.z.~.....G..
    0070 - 1e 32 16 38 23 24 a4 fd-55 ee 46 da 23 60 2f a1   .2.8#$..U.F.#`/.
    0080 - 59 96 83 e5 46 bd f2 d6-f4 9b db 5f 65 50 ea 95   Y...F......_eP..
    0090 - 27 00 e1 cc ab 92 aa 7b-59 2c 0d fb bc 87 b7 a3   '......{Y,......
    00a0 - e2 85 ca 69 49 52 c0 42-73 e1 0d 5d da a7 dd 07   ...iIR.Bs..]....
    00b0 - a5 d2 a5 ef 10 51 7f bc-a1 9a e6 6e c8 85 79 88   .....Q.....n..y.
    00c0 - 2a 92 95 65 93 05 cd 4e-14 20 26 a5 0b ca 45 a9   *..e...N. &...E.

    Start Time: 1677178591
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
bandit16@bandit:~$

nos vamos a kali linux 

┌──(erick㉿kali)-[~]
└─$ nano llavessh2
                                                                                                                                                                       
┌──(erick㉿kali)-[~]
└─$ chmod 600 llavessh2                                          
                                                                                                                                                                       
┌──(erick㉿kali)-[~]
└─$ ssh -i llavessh2 bandit17@bandit.labs.overthewire.org -p 2220 
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames


      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ 



```

# Notas Adicionales
- Usamos nmap para escanear los puertos.
- cat se usa para ver el contenido de un archivo.
- chmod cambia los permisos del archivo
- usamos ssh para conectarnos al servidor por medio de la llave.