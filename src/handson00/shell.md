# Personalitzant la shell

*Oh My Zsh*, conté una àmplia gamma de funcionalitats i complements que poden ajudar-te a treballar de manera més eficient i productiva en la terminal. 

* **Temes personalitzables**: Oh My Zsh ofereix una gran varietat de temes visualment atractius que pots utilitzar per personalitzar l'aparença de la teva terminal. Pots canviar fàcilment el tema per adaptar-lo al teu gust o estil de treball.

* **Complementació d'ordres avançada**: Aquesta funcionalitat suggereix ordres mentre escriviu i us estalvia temps en buscar la sintaxi correcta o recordar noms d'ordres complicats.

* **Gestió de complements**: Hi ha una àmplia col·lecció de complements disponibles que poden millorar la productivitat i la comoditat durant el treball amb la terminal.

* **Configuració personalitzada**: Pots personalitzar la configuració de la terminal segons les teves preferències. Pots canviar el comportament per defecte de la terminal, afegir alias, definir variables d'entorn, crear funcions personalitzades i molt més.

Per instal·lar Oh My Zsh, segueix els següents passos:

1. Obre una terminal al teu sistema.
2. Executa la comanda següent per instal·lar Oh My Zsh:

   ```shell
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

3. Obre el fitxer ~/.zshrc amb el teu editor de text preferit.
4. Modifica les opcions segons les teves preferències. Per trobar informació sobre com configuració pots consultar [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh/) .Pots canviar el tema, afegir complements i configurar variables d'entorn, entre altres coses. 

    ```sh
    # Exemple de configuració personalitzada
    ZSH_THEME="agnoster"
    plugins=(git)
    ```

5. Crea un nou fitxer anomenat **shell.md** dins del repositori del handson. Explica la teva configuració personalitzada de la shell. Has d'utilitzar la sintaxi Markdown per a la documentació. Pots consultar la sintaxi Markdown a [Markdown Guide](https://www.markdownguide.org/basic-syntax/).

6. Crea un enllaç simbòlic del fitxer ~/.zshrc al repositori del handson. Aquest fitxer et permetra recuperar la teva configuració personalitzada de la shell per altres sistemes.

```sh
ln -s ~/.zshrc ~/course-X/Setmana0/handson/.zshrc
```

7. Un cop realitzats els canvis, has de fer commit i push al repositori remot amb el següent missatge: *feat: Add shell config*.