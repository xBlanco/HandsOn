# Connexió remota SSH a la MV

El protocol **SSH o Secure Shell**, és un protocol d'administració remota que permet als usuaris controlar i gestionar els seus servidors remots a través d'Internet mitjançant un mecanisme d'autenticació. El protocol **SSH** es basa en una arquitectura client-servidor que connecta un *client SSH* a un *servidor SSH*. 

El protocol **SSH** es pot utilitzar per a qualsevol tipus de connexió segura, inclosos els terminals de text, els terminals gràfics i la transferència de fitxers. El protocol *SSH* utilitza el port **TCP 22** de forma predeterminada.

Quan hem configurat la màquina virtual, hem activat el servei *SSH*. Això ens permetrà accedir a la màquina virtual de forma remota mitjançant una terminal de la màquina real.

* La màquina virtual té assignada l'adreça IP *10.0.2.15*.
* La redirecció de ports envia el trànsit de la interfície de loopback (*127.0.0.1:2222*) a l'adreça IP de la màquina virtual (*10.0.2.15:22*) per al servei **SSH**.
* Executa la comanda ```ip addr show``` a la màquina virtual per obtenir les seves adreces IP.

* Verifica que la interfície de xarxa (*enp0s1* en aquest cas) té assignada l'adreça IP *10.0.2.15*.

```sh
jordi@debianlab:~$ ip addr show
1: lo: <LOOPBACK,UP,LOWER_UP> 
    mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: enp0s1: <BROADCAST,MULTICAST,UP,LOWER_UP> 
    mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 5a:09:e9:ee:3b:c2 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global dynamic enp0s1
       valid_lft 81515sec preferred_lft 81515sec
    inet6 fec0::5809:e9ff:feee:3bc2/64 scope site dynamic mngtmpaddr
       valid_lft 86356sec preferred_lft 14356sec
    inet6 fe80::5809:e9ff:feee:3bc2/64 scope link
       valid_lft forever preferred_lft forever
```

Un cop configurada la màquina virtual, podem accedir-hi remotament des de la màquina real mitjançant una terminal. Per fer-ho, seguirem els següents passos:

1. Escrivim en una consola de la vostra màquina real:

```sh
ssh username@ip
ssh jordi@127.0.0.1 -p 2222
```

2. Acceptem el Fingerprint (**Yes**).
3. Iniciem sessió amb el vostre usuari, en el meu cas l'usuari *jordi*.
