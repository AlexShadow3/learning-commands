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
    - [man](#man)
    - [D'autres commandes](#dautres-commandes)
    - [clear](#clear)
      - [exit](#exit)
      - [history](#history)
      - [sudo](#sudo)
  - [Dictionnaire](#dictionnaire)

</details>

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)

## Partie 1

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/water.png)

### Introduction

Bienvenue dans ce guide conçu pour vous apprendre les commandes de base de votre terminal. Vous pourrez ainsi apprendre à vous déplacer dans vos dossiers, créer des fichiers, les modifier, les supprimer, etc.

En informatique, un [Shell](https://fr.wikipedia.org/wiki/Interface_syst%C3%A8me) (à ne pas confondre avec "coquillage" en français) est un programme qui fournit une interface entre l'utilisateur et le système d'exploitation d'un ordinateur. Il permet à l'utilisateur de donner des commandes à l'ordinateur en utilisant un langage de ligne de commande. Le shell interprète ces commandes et les exécute, permettant ainsi à l'utilisateur d'effectuer différentes tâches telles que la navigation dans le système de fichiers, le lancement de programmes, la gestion des fichiers, etc. En résumé, le shell est une sorte de "coquille" autour du noyau de l'ordinateur, offrant un moyen pratique de communiquer avec lui.

Pour commencer, ouvrez votre `Explorateur de fichier` (Windows) ou votre `Finder` (MacOS). Créez un nouveau dossier `commandes` dans le dossier de votre choix puis créez un nouveau dossier `Shell` dans le dossier `commandes`.

Nous pouvons maintenant commencer.
Tout d'abord, ouvrez votre terminal, vous devriez voir quelque chose comme ceci :

Sur Windows :

```bash
C:\Users\compt\...
```

> (`C:` est le nom de votre système d'exploitation, `Users` est le nom du dossier dans lequel vous vous trouvez, `compt` est le nom de votre compte utilisateur et `...` est le chemin vers le dossier dans lequel vous vous trouvez)

Sur MacOS ou Linux :

```bash
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### cd

Pour commencer, nous allons faire simple avec la commande `cd`. Celle ci permet de se déplacer dans un dossier. Pour cela, il suffit de taper `cd` suivi du nom du dossier dans lequel vous souhaitez vous rendre. Par exemple:

```bash
cd Shell
```

Vous pouvez aussi reculer d'un dossier en y ajoutant `..`:

```bash
cd ..
```

Ou même retourner dans le dossier précédent en y ajoutant `-`:

```bash
cd -
```

Mais bien sûr, je dois être dans le dossier `commandes` pour pouvoir me rendre dans le dossier `Shell`. Mais comment savoir où se trouve le dossier `commandes` ?

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### ls

Viens la commande `ls`. Celle-ci permet d'afficher le contenu d'un dossier (c'est à dire qu'elle affichera tous les dossiers et fichiers du dossier choisi).

```bash
ls
```

Cette commande (lancée dans notre dossier `Shell`) devrait renvoyer `README.md`

A vous de jouer ! Essayez de vous rendre dans le dossier `Shell` en utilisant les commandes `cd` et `ls`.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### pwd

Maintenant que nous sommes dans le dossier `Shell`, nous allons voir la commande `pwd`. Celle-ci permet d'afficher le chemin vers le dossier dans lequel vous vous trouvez.

```bash
pwd
```

Cette commande (lancée dans notre dossier `Shell`) devrait renvoyer (devrait se terminer par):

```bash
..\commandes\Shell || ../commandes/Shell
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### touch

Notre nouvelle commande est `touch`. Celle-ci permet de créer un fichier. Pour cela, il suffit de taper `touch` suivi du nom du fichier que vous souhaitez créer. Par exemple:

```bash
touch test.txt
```

Cette commande (lancée dans notre dossier `Shell`) devrait créer un fichier `test.txt` dans notre dossier `Shell`. Simple, pas vrai ?
Pour la suite je vous demanderais d'écrire quelque chose dans ce fichier.

Le text suivant est très long, mais vous pouvez aussi télécharger le fichier [ici](https://github.com/AlexShadow3/learning-commands/blob/master/Shell/test.txt).

```txt
Ada était la seule fille légitime du poète George Gordon Byron et de son épouse Annabella Milbanke, une femme intelligente et cultivée, cousine de Caroline Lamb, dont la liaison avec Byron fut à l'origine d'un scandale.

Byron recherchait une femme dont la fortune paierait ses dettes. Lady Melbourne lui suggère sa propre nièce, miss Milbanke, mais celle-ci refuse dans un premier temps. Cette union est ensuite encouragée par Augusta Leigh, la demi-sœur de Byron, et Byron épouse Annabella en janvier 1815.

Ada naît en décembre de cette même année. Le premier prénom d'Ada, Augusta, aurait été choisi en hommage à Augusta avec qui Byron aurait eu des relations incestueuses. Le prénom Ada aurait été choisi par Byron lui-même, car il était « court, antique et vocalique ».

À la suite de quatre tentatives de viol en état d'ivresse de la part de Byron, Annabella quitte Byron le 16 janvier 1816, gardant Ada avec elle. Le 21 avril, Byron signe l'acte de séparation, puis quitte le Royaume-Uni pour toujours. Il ne les revit jamais.

Annabella adorait les mathématiques. Byron l’appelait même parfois « la princesse des parallélogrammes ». Annabella fit en sorte que les tuteurs d'Ada lui donnent une éducation approfondie en mathématiques et en sciences, ce qui était tout à fait inhabituel à l'époque dans l'éducation d'une jeune fille de la noblesse. En 1832, Ada rencontre Mary Somerville, éminente chercheuse et autrice scientifique du xixe siècle, qui l'encourage et l'aide à progresser en mathématiques. Le 5 juin 1833, Mary lui présente Charles Babbage, et Ada — alors âgée de 17 ans — est immédiatement fascinée par ses machines à calcul. Ils deviennent très proches, Ada semblant trouver en Babbage le père qu'elle n'avait jamais eu. Parmi ses autres connaissances, on compte David Brewster, Charles Wheatstone, Charles Dickens et Michael Faraday.

Elle se marie en 1835 avec William King, 1er comte de Lovelace. Ils auront trois enfants : Byron, né le 12 mai 1836, Annabella (Anne Blunt) née le 22 septembre 1837 et Ralph Gordon né le 2 juillet 1839. William était dévoué à Ada et encourageait les goûts et les activités d'Ada en mathématiques. La famille vécut à Ockham Park, à Ockham. Son titre et son nom complet furent pendant la plus grande partie de sa vie `La très honorable Augusta Ada, comtesse de Lovelace. Elle est plus connue sous le nom de Ada Lovelace` ou `Lady Lovelace`.

La santé fragile d'Ada, mise à l'épreuve par les grossesses, ainsi que ses responsabilités de mère et de maîtresse de maison, la tiennent écartée de ses activités mathématiques jusqu'en 1839. À cette date, elle éprouve le besoin de reprendre l'étude des mathématiques et demande à Babbage de lui recommander un tuteur : le célèbre mathématicien Auguste De Morgan accepte cette charge. Les études d'Ada reprennent, et De Morgan trouve en Ada une élève enthousiaste et créative. Ada prend confiance dans ses capacités en mathématiques, encouragée par les retours positifs de De Morgan. Le 6 février 1841, Ada écrit à sa mère une lettre où elle parle de ses goûts et aspirations : « Je crois que je possède une singulière combinaison de qualités, qui semble précisément ajustée pour me prédisposer à devenir une exploratrice des réalités cachées de la Nature ». Elle mentionne son « énergie inépuisable et insatiable » et pense avoir trouvé un sens à sa vie.

En 1841, Ada a de nouveau des problèmes de santé, mais elle revient aux mathématiques fin 1842. Elle tourne dès lors entièrement son travail vers la machine analytique de Babbage, et propose à ce dernier ses services pour en poursuivre le développement et la promotion.

Mémoire sur la machine de Babbage

En octobre 1842, paraît en français, dans un journal suisse, une description de la machine analytique de Babbage réalisée par le mathématicien italien Louis-Frédéric Ménabréa (1809-1896). Charles Wheatstone propose à Ada Lovelace, qui a un bon niveau de français, de traduire ce mémoire pour le journal `Scientific Memoirs` spécialisé dans les articles scientifiques étrangers.

Elle passe neuf mois, entre 1842 et 1843, sur cette traduction. Babbage lui-même n'intervient que très peu, étant malade pendant cette même période, et la traduction lui est présentée au début de l'année 1843 un peu comme un « fait accompli ». Il demande alors à Ada pourquoi elle n'avait pas fait elle-même un mémoire présentant la machine analytique, ce à quoi elle répondit que l'idée ne lui était pas venue à l'esprit. Babbage propose alors à Ada d'augmenter la traduction avec des notes développant et commentant certains aspects du mémoire, idée immédiatement adoptée avec enthousiasme par Ada.

S'ensuit une période de travail frénétique sur ces notes, en collaboration étroite avec Charles Babbage qui annote les brouillons, corrige les incompréhensions tout en encourageant et félicitant Ada de son travail. Elle ajoute à cet article sept notes, labellisées de A à G, représentant près de trois fois le volume de texte de l'article original. La note G s'appuie sur un véritable algorithme très détaillé pour calculer les nombres de Bernoulli avec la machine. Le programme qui en résulte est souvent considéré comme le premier véritable programme informatique au monde, car les algorithmes décrits jusque-là n'étaient pas décrits avec un formalisme, dans un langage véritablement destiné à être exécuté sur une machine. De plus, ce programme comporte selon Catherine Dufour la première boucle conditionnelle, véritable concept informatique, contrairement aux programmes séquentiels qui avaient pu être faits auparavant par Babbage, ou dans les métiers à tisser Jacquard.

On ne sait pas exactement dans quelle mesure Ada Lovelace a programmé elle-même cet algorithme, ayant été en relation constante et étroite avec Babbage. Ce qui semble sûr c'est qu'Ada a eu l'idée de donner un exemple de programmation de la machine en utilisant le calcul des nombres de Bernoulli, et que Babbage a fourni à Ada au minimum les formules mathématiques de base. Selon Betty Toole, Ada était tout à fait en mesure de réaliser elle-même le programme, ayant montré une profonde compréhension de la machine dans sa traduction et ses notes, et des lettres entre Babbage et Ada semblent indiquer que le rôle de Babbage s'est effectivement limité à fournir les formules mathématiques. En revanche, Bruce Collier, un des meilleurs spécialistes de la machine de Babbage, porte le jugement sévère suivant : « Cela ne serait qu'une légère exagération de dire que les notes du mémoire ont été écrites par Babbage, et que — pour des raisons qui lui sont propres — il a entretenu l'idée dans l'esprit d'Ada Lovelace, et dans l'esprit du public, que ces notes étaient d'elle ».

Algorithme de calcul des coefficients du produit de deux polynômes, par Charles Babbage (1838), écrit avant Lovelace, mais simple programme séquentiel.
Selon Stephen Wolfram, on n'a jamais retrouvé, dans les documents et publications de Babbage, des algorithmes aussi complexes et aussi propres que celui sous-jacent au programme de calcul des nombres de Bernoulli. Babbage, à la fin de sa vie, avait compilé une liste datée de 446 calculs possibles avec sa machine analytique `(446 Notations of the Analytical Engine)`, tous datés de 1830 à mi 1840, date après laquelle on ne trouve plus de travaux de Babbage sur les algorithmes. Ada Lovelace ayant conçu son programme en 1842, ces éléments laissent penser que c'est bien elle qui a conçu ce programme, avec la simple supervision bienveillante de Babbage.

Dans d'autres notes, Ada Lovelace montre une perception des potentialités de la machine que Doron Swade considère comme « visionnaire, même dans une perspective moderne ». Babbage avait une vision de sa machine comme étant tournée vers le calcul numérique, avec à la limite des extensions vers le calcul algébrique avec la possibilité de manipuler des symboles plutôt que des chiffres. Mais il n'a rien publié allant dans ce sens, et il n'a pas approfondi cette possibilité, allant même jusqu'à imaginer un autre type de machine spécifique pour les calculs algébriques. En revanche, Ada Lovelace décrit explicitement des possibilités allant au-delà d'un contexte mathématique, comme l'hypothèse que « la machine pourrait composer de manière scientifique et élaborée des morceaux de musique de n'importe quelle longueur ou degré de complexité ».

Un autre passage des notes d'Ada, cité par Doron Swade, illustre cette vision de calculateur universel :

« Beaucoup de personnes […] s'imaginent que parce que la Machine fournit des résultats sous une forme numérique, alors la nature de ses processus doit être forcément arithmétique et numérique, plutôt qu'algébrique ou analytique. Ceci est une erreur. La Machine peut arranger et combiner les quantités numériques exactement comme si elles étaient des lettres, ou tout autre symbole général ; en fait elle peut donner des résultats en notation algébrique, avec des conventions appropriées. »

Il fallut attendre les années 1930 avec Alan Turing pour formaliser une telle notion de calculateur universel qui manipule des symboles généraux, et abandonner la notion de calculatrice purement numérique.

Ruine et mort

Dans l’espoir de subventionner les projets de Babbage, qui n'avaient pas obtenu de financement du gouvernement britannique, Lady Lovelace se mit à jouer. Elle travailla à un système qui devait lui permettre de remporter les paris du derby d'Epsom mais ne l'entraîna que dans l'accumulation de dettes.

Elle mourut à l'âge de 36 ans d'un cancer de l'utérus, dans d'horribles souffrances. Elle laissait deux fils et une fille. Cette dernière, Anne Blunt, est connue pour avoir voyagé au Moyen-Orient et pour avoir élevé des chevaux arabes.

Elle fut enterrée conformément à son souhait près de son père qu'elle n'avait jamais connu, à l'église Sainte-Marie-Magdalene de Hucknall, à Newstead Abbey, dans le comté de Nottingham.

Notoriété posthume
Tombée dans l'oubli, Ada Lovelace et ses travaux furent exhumés avec l'avènement de l'informatique. Et c'est en son hommage qu'on a appelé Ada le langage de programmation conçu entre 1977 et 1983 pour le département de la Défense américain (DoD) par une équipe de CII Honeywell Bull dirigée par le Français Jean Ichbiah. L'idée de choisir le nom Ada est attribuée à Jack Cooper, du Naval Material Command, et remonte à juillet 1978.

Ada Lovelace est considérée par les historiens de l'informatique comme la première personne de l'histoire à avoir programmé. On peut voir notamment son portrait sur les hologrammes d'authentification des produits Microsoft.

L'entreprise Nvidia a également décidé de nommer sa nouvelle architecture graphique sous le nom de Ada Lovelace, pour sa nouvelle série de cartes graphiques RTX 4000.

L'astéroïde (232923) Adalovelace porte son nom.

La cryptomonnaie Cardano porte également son nom en hommage, le jeton s'appelle Ada et la plus petite fraction indivisible s'appelle un Lovelace.

L'École polytechnique fédérale de Lausanne baptise place Ada Lovelace la place de l'entrée nord.

L'Ada Lovelace Day est un événement annuel organisé le deuxième mardi d'octobre pour célébrer et sensibiliser aux contributions des femmes aux sciences, et notamment en technologie, en ingénierie et en mathématiques.
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### mkdir

Maintenant, nous allons voir la commande `mkdir`. Celle-ci permet de créer un dossier. Pour cela, il suffit de taper `mkdir` suivi du nom du dossier que vous souhaitez créer. Par exemple:

```bash
mkdir test
```

Cette commande (lancée dans notre dossier `Shell`) devrait créer un dossier `test` dans notre dossier `Shell`. Simple, pas vrai ?

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### mv

Passons maintenant à la commande `mv`. Celle-ci permet de déplacer un fichier ou un dossier. Pour cela, il suffit de taper `mv` suivi du nom du fichier ou du dossier que vous souhaitez déplacer, puis du chemin vers le dossier dans lequel vous souhaitez le déplacer. Par exemple:

```bash
mv test.txt test
```

Nous devrions donc maintenant avoir notre fichier `test.txt` dans notre dossier `test`.

Mince, nous avons oublié de faire une copie de notre fichier. Pas de panique, il existe une commande pour ça !

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### cp

La commande `cp`, utile pour copier un fichier ou un dossier. Pour cela, il suffit de taper `cp` suivi du nom du fichier ou du dossier que vous souhaitez copier, puis du chemin vers le dossier dans lequel vous souhaitez le copier. Par exemple:

```bash
cp test/test.txt ../Shell
```

Nous devrions donc maintenant retrouver notre fichier `test.txt` dans notre dossier `Shell`.
C'est bien drôle tout ça mais nous devons faire de la place sur notre ordinateur. Supprimons donc notre fichier `test.txt` et notre dossier `test`.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### rm

Premièrement, la commande `rm`. Celle-ci permet de supprimer un fichier. Pour cela, il suffit de taper `rm` suivi du nom du fichier que vous souhaitez supprimer. Placez vous dans le dossier `test` et tapez:

```bash
rm test.txt
```

Nous avons désormais un dossier vide !

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### rmdir

Enfin, la commande `rmdir`. Celle-ci permet de supprimer un dossier. Pour cela, il suffit de taper `rmdir` suivi du nom du dossier que vous souhaitez supprimer. Par exemple:

```bash
rmdir test
```

Petite spécificité de cette commande, elle ne fonctionne que si le dossier est vide. Si vous souhaitez supprimer un dossier qui n'est pas vide, il vous faudra utiliser la commande `rm -r` (qui supprimera le dossier et tout son contenu). Comme vous pouvez le voir, l'option `-r` à été rajoutée. Mais nous verrons ça dans la partie 2.

Faisons un petit détour et testons une commande... utile ?

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### echo

La commande `echo` permet d'afficher du texte dans le terminal. Pour cela, il suffit de taper `echo` suivi du texte que vous souhaitez afficher. Par exemple:

```bash
echo "Hello World !"
```

Affichera... `Hello World !` dans votre terminal. Magique, non ?
Une autre commande de ce type serait...

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### cat

La commande `cat` permet d'afficher le contenu d'un fichier. Pour cela, il suffit de taper `cat` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
cat test.txt
```

N.B. Vous pouvez aussi concaténer des caractères, des nombres, etc... entre eux. (Concaténer = mettre bout à bout (Si j'ai deux nombres, 143 et 528, et que je les concatène, j'obtiens 143528)).

Créez deux fichiers `test1.txt` et `text2.txt` et écrivez quelque chose dedans (`Hello,` dans l'un et `World!` dans l'autre par exemple). Puis, concaténez les deux fichiers dans un nouveau fichier `test3.txt` en utilisant la commande `cat` comme ceci.

```bash
cat test1.txt test2.txt > test3.txt
```

Vous avez désormais un fichier `text3.txt` avec comme contenu le contenu de `test1.txt` suivi du contenu de `test2.txt`.

Compliqué cette commande nan ? Revenons sur quelque chose de plus cool.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### grep

Celle-ci s'appelle `grep`. Elle permet de rechercher un mot dans un fichier. Pour cela, il suffit de taper `grep` suivi du mot que vous souhaitez rechercher, puis du nom du (ou des) fichier(s) dans lequel vous souhaitez le rechercher. Par exemple:

```bash
grep "Ada" test.txt
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### more

La commande `more` permet d'afficher le contenu d'un fichier, mais de manière plus lisible. Pour cela, il suffit de taper `more` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
more test.txt
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### less

La commande `less`, tout comme `more`, permet d'afficher le contenu d'un fichier de manière plus lisible. Pour cela, il suffit de taper `less` suivi du nom du fichier que vous souhaitez afficher. Par exemple:

```bash
less test.txt
```

Vous voyez la différence ? Non ? Essayez de faire défiler le contenu du fichier avec les flèches de votre clavier. Vous devriez voir que `less` permet de faire défiler le contenu du fichier, contrairement à `more` qui affiche tout le contenu du fichier d'un coup.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### man

L'une des commandes essentielles à connaître, `man`. Cette commande affiche un 'guide' selon la commande choisie.

```bash
man ls
```

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

### D'autres commandes

#### clear

La commande `clear` permet de nettoyer le terminal. Pour cela, il suffit de taper `clear`.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

#### exit

Comme son nom l'indique, la commande `exit` permet de quitter le terminal. Pour cela, il suffit de taper `exit`.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

#### history

Comme son nom l'indique, la commande `history` permet de visualiser un historique des commandes passées.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

#### sudo

Cette commande spéciale correspond au `Superuser`, un genre d'administrateur. Pour l'utiliser, il vous suffit simplement de rajouter `sudo` devant votre commande.

![-----](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- ## Partie 2

Nous allons dans cette deuxième partie, voir les différents paramètres des commandes que nous avons vu précédemment. -->

## Dictionnaire

| Nom de la commande | Terme entier | Commande | Exemple d'utilisation |
| ------------------ | ------------ | -------- | --------------------- |
| cd | change directory | changer de dossier | cd Shell |
| ls | list | lister les éléments d'un dossier | ls |
| pwd | print working directory | afficher le chemin vers le dossier dans lequel on se trouve | pwd |
| touch | touch | créer un fichier | touch test.txt |
| mkdir | make directory | créer un dossier | mkdir test |
| mv | move | déplacer un fichier ou un dossier | mv test.txt test |
| cp | copy | copier un fichier ou un dossier | cp test/test.txt ../Shell |
| rm | remove | supprimer un fichier | rm test.txt |
| rmdir | remove directory | supprimer un dossier | rmdir test |
| echo | echo | afficher du texte dans le terminal | echo "Hello World !" |
| cat | concatenate | afficher le contenu d'un fichier | cat test.txt |
| grep | global regular expression print | rechercher un mot dans un fichier | grep "Ada" test.txt |
| more | more | afficher le contenu d'un fichier de manière plus lisible | more test.txt |
| less | less | afficher le contenu d'un fichier de manière plus lisible | less test.txt |
