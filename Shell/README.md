# SHELL

Prêt pour partir à la découverte des commandes Shell ? C'est parti !

<img src="https://cdn.iconscout.com/icon/free/png-256/free-powershell-3628993-3030218.png" width="200px" align="right" alt="Shell">

<details>
<summary style="font-size:150%">
    Table des matières 📖
</summary>

- [SHELL](#shell)
  - [Partie 1](#partie-1)
    - [Introduction](#introduction)
    - [cd](#cd)
    - [ls](#ls)
    - [pwd](#pwd)
    - [touch](#touch)
    - [mkdir](#mkdir)
    - [mv](#mv)
    - [cp](#cp)
    - [rm](#rm)
    - [rmdir](#rmdir)
    - [echo](#echo)
    - [cat](#cat)
    - [grep](#grep)
    - [more](#more)
    - [less](#less)
  - [Partie 2](#partie-2)

</details>

## Partie 1

### Introduction

Bienvenue dans ce cours conçu pour vous apprendre les commandes de base de votre terminal. Vous pourrez ainsi apprendre à vous déplacer dans vos dossiers, créer des fichiers, les modifier, les supprimer, etc.
Pour commencer, ouvrez votre terminal et placez vous dans le dossier `Shell` de ce repository.
Ah, vous ne savez pas comment faire ? Ce n'est pas grave, je suis là pour vous aider.
Tout d'abord, lorsque vous ouvrir votre terminal, vous devriez voir quelque chose comme ceci :

Sur Windows :

```bash
C:\Users\compt\...
```

> (`C:` est le nom de votre système d'exploitation, `Users` est le nom du dossier dans lequel vous vous trouvez, `compt` est le nom de votre compte utilisateur et `...` est le chemin vers le dossier dans lequel vous vous trouvez)

Sur MacOS ou Linux :

```bash
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

### cd

Pour commencer, nous allons faire simple avec la commande `cd`. Celle ci permet de se déplacer dans un dossier. Pour cela, il suffit de taper `cd` suivi du nom du dossier dans lequel vous souhaitez vous rendre. Par exemple:

```bash
cd Shell
```

Vous pouvez aussi reculer d'un dossier en y ajoutant `..`:

```bash
cd ..
```

Mais bien sûr, je dois être dans le dossier (repository) `learning-commands` pour pouvoir me rendre dans le dossier `Shell`. Mais comment savoir où se trouve le dossier `learning-commands` ?

### ls

Viens la commande `ls`. Celle-ci permet d'afficher le contenu d'un dossier (c'est à dire qu'elle affichera tous les dossiers et fichiers du dossier choisi).

```bash
ls
```

Cette commande (lancée dans notre dossier `Shell`) devrait renvoyer:

```bash
README.md
```

A vous de jouer ! Essayez de vous rendre dans le dossier `Shell` de ce repository en utilisant les commandes `cd` et `ls`.

### pwd

Maintenant que nous sommes dans le dossier `Shell`, nous allons voir la commande `pwd`. Celle-ci permet d'afficher le chemin vers le dossier dans lequel vous vous trouvez.

```bash
pwd
```

Cette commande (lancée dans notre dossier `Shell`) devrait renvoyer (devrait se terminer par):

```bash
..\learning-commands\Shell || ../learning-commands/Shell
```

### touch

Notre nouvelle commande est `touch`. Celle-ci permet de créer un fichier. Pour cela, il suffit de taper `touch` suivi du nom du fichier que vous souhaitez créer. Par exemple:

```bash
touch test.txt
```

Cette commande (lancée dans notre dossier `Shell`) devrait créer un fichier `test.txt` dans notre dossier `Shell`. Simple, pas vrai ?

### mkdir

Maintenant, nous allons voir la commande `mkdir`. Celle-ci permet de créer un dossier. Pour cela, il suffit de taper `mkdir` suivi du nom du dossier que vous souhaitez créer. Par exemple:

```bash
mkdir test
```

Cette commande (lancée dans notre dossier `Shell`) devrait créer un dossier `test` dans notre dossier `Shell`. Simple, pas vrai ?

### mv

Passons maintenant à la commande `mv`. Celle-ci permet de déplacer un fichier ou un dossier. Pour cela, il suffit de taper `mv` suivi du nom du fichier ou du dossier que vous souhaitez déplacer, puis du chemin vers le dossier dans lequel vous souhaitez le déplacer. Par exemple:

```bash
mv test.txt test
```

Nous devrions donc maintenant avoir notre fichier `test.txt` dans notre dossier `test`.
Mais, mince, nous avons oublié de faire une copie de notre fichier. Pas de panique, il existe une commande pour ça !

### cp

La commande `cp`, utile pour copier un fichier ou un dossier. Pour cela, il suffit de taper `cp` suivi du nom du fichier ou du dossier que vous souhaitez copier, puis du chemin vers le dossier dans lequel vous souhaitez le copier. Par exemple:

```bash
cp test.txt Shell
```

Nous devrions donc maintenant retrouver notre fichier `test.txt` dans notre dossier `Shell`.
C'est bien drôle tout ça mais nous devons faire de la place sur notre ordinateur. Supprimons donc notre fichier `test.txt` et notre dossier `test`.

### rm

Premièrement, la commande `rm`. Celle-ci permet de supprimer un fichier. Pour cela, il suffit de taper `rm` suivi du nom du fichier que vous souhaitez supprimer. Par exemple:

```bash
rm test.txt
```

Nous avons désormais un dossier vide !

### rmdir

Enfin, la commande `rmdir`. Celle-ci permet de supprimer un dossier. Pour cela, il suffit de taper `rmdir` suivi du nom du dossier que vous souhaitez supprimer. Par exemple:

```bash
rmdir test
```

Petite spécificité de cette commande, elle ne fonctionne que si le dossier est vide. Si vous souhaitez supprimer un dossier qui ne l'est pas, il vous faudra utiliser la commande `rm -r` (qui supprimera le dossier et tout son contenu). Comme vous pouvez le voir, l'option `-r` à été rajoutée. Mais nous verrons ça dans la partie 2.

Faisons un petit détour et testons une commande... utile ?

### echo

La commande `echo` permet d'afficher du texte dans le terminal. Pour cela, il suffit de taper `echo` suivi du texte que vous souhaitez afficher. Par exemple:

```bash
echo "Hello World !"
```

Affichera... `Hello World !` dans votre terminal. Magique, non ?
Une autre commande de ce type serait...

### cat

La commande `cat` permet d'afficher le contenu d'un fichier. Pour cela, il suffit de taper `cat` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
cat README.md
```

N.B. Vous pouvez aussi concaténer des fichiers entre eux. (Concaténer = mettre bout à bout (Si j'ai deux nombres, 143 et 528, et que je les concatène, j'obtiens 143528)).

Créez deux fichiers `test1.txt` et `text2.txt` et écrivez quelque chose dedans. Puis, concaténez les deux fichiers dans un nouveau fichier `test3.txt` en utilisant la commande `cat` comme ceci.

```bash
cat test1.txt test2.txt > test3.txt
```

Vous avez désormais un fichier `text3.txt` avec comme contenu le contenu de `test1.txt` suivi du contenu de `test2.txt`.

Compliqué cette commande nan ? Revenons sur quelque chose de plus cool.

### grep

Celle-ci s'appelle `grep`. Elle permet de rechercher un mot dans un fichier. Pour cela, il suffit de taper `grep` suivi du mot que vous souhaitez rechercher, puis du nom du (ou des) fichier(s) dans lequel vous souhaitez le rechercher. Par exemple:

```bash
grep "contenu" README.md
```

### more

La commande `more` permet d'afficher le contenu d'un fichier, mais de manière plus lisible. Pour cela, il suffit de taper `more` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
more README.md
```

### less

La commande `less`, tout comme `more`, permet d'afficher le contenu d'un fichier de manière plus lisible. Pour cela, il suffit de taper `less` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
less README.md
```

Vous voyez la différence ? Non ? Essayez de faire défiler le contenu du fichier avec les flèches de votre clavier. Vous devriez voir que `less` permet de faire défiler le contenu du fichier, contrairement à `more` qui affiche tout le contenu du fichier d'un coup.

## Partie 2

A suivre...
 