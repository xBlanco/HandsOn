# Configurant l'Entorn de Desenvolupament

Per instal·lar el llenguatge de programació **C a Debian**, pots seguir aquests passos:

1. Connecta una terminal al teu sistema Debian i obra una sessió com a usuari **root**.

```sh
~jordi@debianlab:~$ su -
```

2. Instal·la el paquet *build-essential*, que inclou les eines i llibreries necessàries per compilar i construir programes en C. Aquest paquet inclou el compilador GCC, que és comunament utilitzat per programar en C.

```sh
~root@debianlab:/home/jordi: apt install build-essential -y
```

3. Torna a la sessió com a usuari normal i comprova que el compilador GCC s'ha instal·lat correctament.Verifica la instal·lació comprovant la versió del compilador GCC instal·lat.

```sh
~root@debianlab:/home/jordi exit
~jordi@debianlab:~$ gcc --version
```

Ara ja pots escriure i compilar programes en *C* al teu sistema Debian. 

4. Crea una carpeta al home del teu usuari per desar el contingut del curs, utilitza la comanda `mkdir`:

```sh
~jordi@debianlab:~$ mkdir -p ~/course-X/Setmana0/handson
~# Recorda que X és el teu nom d'usuari de github
```

5. Utilitza ```neovim```. O bé, qualsevol editor de text per crear `hola.c` a la carpeta que acabes de crear. Recorda que l'editor **neovim** l'has instal·lat durant el **HandsOn-00**.

```sh
nvim hola.c
# Prem la tecla i per entrar en mode d'inserció
# Enganxa el contingut
# Prem la tecla ESC per sortir del mode d'inserció
# Prem la tecla : per entrar en mode comandament
# Escriu wq per desar i sortir
```

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
