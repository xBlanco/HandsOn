# Primers Passos

Una manera de començar a experimentar amb Debian és configurar una màquina virtual (MV) amb aquest sistema operatiu. Aquí tens una guia bàsica per a configurar una MV amb Debian.


1. Elecció del programa de virtualització:

    * **Arquitectura x86**: Aquesta ruta de configuració és pels estudiants que tinguin un *laptop* amb arquitectura basada en x86 (*CPU Intel o AMD*). En aquest cas s'utilitzarà el programari *VirtualBox* per realitzar la configuració i els exemples.Sou lliures d'adaptar aquesta guia a altres opcions com *VMWare*.

        * **[Descarrega el VirtualBox](https://www.virtualbox.org/wiki/Downloads)**.
        * Instal·leu el VirtualBox al vostre dispositiu.

    * **Arquitectura ARM**: Aquesta ruta de configuració és pels estudiants que tinguin un *mac* amb els nous processadors *M1 i M2*. En aquest cas s'emprarà el programari *UTM* per portar a cap la configuració i els exemples. Podeu adaptar a altres opcions com *Parallels*.

        * **[Descarrega el UTM](https://mac.getutm.app/)**.
        * Instal·leu el UTM al vostre dispositiu.


2. Descarregueu la imatge del sistema operatiu: Utiltizarem la versió **[Debian 12.0](https://www.debian.org/releases/stable/i386/release-notes/ch-whats-new.html)**.
    * Descarregar per a [**x86**](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-12.0.0-amd64-netinst.iso)
    * Descarregar per a [**ARM**](https://cdimage.debian.org/debian-cd/current/arm64/iso-cd/debian-12.0.0-arm64-netinst.iso)

3. Creació de la màquina virtual amb les següents característiques:

* Configuració bàsica:
    - **Nom**: DebianLab_OS_GEI_VM
    - **Sistema operatiu**: Debian 12.0
    - **Arquitectura**: x86/x64 (64 bits) 
    - **Memòria**: 4 GB
    - **Espai d'emmagatzematge**: 20 GB
    - **Processador**: 1 Core

* Configuració de xarxa:
    - **Mode de xarxa**: VLAN Emulat
    - **Redirecció de ports**: Sí
        - Servei SSH:
            - Protocol: TCP
            - Direcció Invitat: 10.0.2.15
            - Port Invitat: 22
            - Direcció Host: 127.0.0.1
            - Port Host: 2222



