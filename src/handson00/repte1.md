# Configurant Entorn de Desenvolupament

Per instal·lar el llenguatge de programació **C a Debian**, pots seguir aquests passos:

1. Connecta una terminal al teu sistema Debian i obra una sessió com a usuari **root**.

2. Actualitza les llistes de paquets per assegurar-te que tens la informació més recent sobre els paquets disponibles. 

```sh
apt get update -y
```

3. Instal·la el paquet build-essential, que inclou les eines i llibreries necessàries per compilar i construir programes en C:

```sh
 apt install build-essential -y
```

Aquest paquet inclou el compilador GCC, que és comunament utilitzat per programar en C.

4. Verifica la instal·lació comprovant la versió del compilador GCC instal·lat.

```sh
gcc --version
```

5. Ara pots escriure i compilar programes en C al teu sistema Debian. 

6. Crea una carpeta per desar el contingut d'aquest hands-on:

```sh
mkdir -p ~/course-X/Setmana0/handson
# Recourda X és el teu nom d'usuari de github
```

7. Utilitza VS-Code o un editor de text per crear `hola.c` a la carpeta que acabes de crear.

8. Escriu el següent codi en C al fitxer creat.

```c
#include <stdio.h>

int main() {
    printf("Hola, benvingut al DebianLab!\n");
    return 0;
}
```

8. Compila el programa amb la comanda `gcc`:

```sh
gcc -o hola hola.c
```

9. Executa el programa:

```sh
./hola
```

Realitzarem el primer commit, primer has d'afegir els canvis que vols incloure (working directory -> staging area):

```sh
git add hola.c
```


A continuació, utilitzes la comanda git commit per crear el commit amb un missatge descriptiu (staging area -> local repository):

```sh
git commit -m "Add hola.c: Hello World in C"
```

Amb aquest commit, has registrat els canvis al teu repositori local, juntament amb el missatge explicatiu.

Per pujar els canvis al repositori remot (local repository -> remote repository):

```sh
git push
```

Aquesta comanda envia els commits realitzats al teu repositori local al repositori remot corresponent. D'aquesta manera, els altres desenvolupadors poden veure els teus canvis i treballar-hi col·laborativament.
