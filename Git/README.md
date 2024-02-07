# GIT

Prêt pour partir à la découverte des commandes Git ? C'est parti !

<img src="https://gitforwindows.org/img/git_logo.png" width="200px" align="right" alt="Git">

<details>
<summary style="font-size:150%">
  Table des matières 📖
</summary>

- [GIT](#git)
  - [Partie 1](#partie-1)
    - [Introduction](#introduction)
    - [Les commandes git](#les-commandes-git)
      - [git version](#git-version)
      - [git config](#git-config)
      - [git init](#git-init)
      - [git add](#git-add)
      - [git status](#git-status)
      - [git clone](#git-clone)
      - [git commit](#git-commit)
      - [git log](#git-log)
      - [git push](#git-push)
      - [git checkout - switch](#git-checkout---switch)
      - [git remote](#git-remote)
      - [git branch](#git-branch)
      - [git pull](#git-pull)
      - [git merge](#git-merge)
      - [git diff](#git-diff)
      - [git tag](#git-tag)
      - [git reset - revert](#git-reset---revert)
      - [git rm](#git-rm)
      - [git stash](#git-stash)
      - [git show](#git-show)
      - [git fetch](#git-fetch)
      - [git ls-tree](#git-ls-tree)
      - [git cat-file](#git-cat-file)
      - [git grep](#git-grep)
      - [gitk](#gitk)
      - [git instaweb](#git-instaweb)
      - [git gc](#git-gc)
      - [git archive](#git-archive)
      - [git prune](#git-prune)
      - [git fsck](#git-fsck)
      - [git rebase](#git-rebase)
      - [git help](#git-help)
  - [Dictionnaire](#dictionnaire)

</details>

## Partie 1

### Introduction

Bienvenue dans ce guide conçu pour vous apprendre les commandes git. Vous apprendrez à créer un repository, à ajouter des fichiers, à mettre à jour ce repo... et bien plus encore !

Git est un logiciel de gestion de versions décentralisé. C'est un logiciel libre et gratuit, créé en 2005 par [Linus Torvalds](https://fr.wikipedia.org/wiki/Linus_Torvalds), auteur du noyau Linux, et distribué selon les termes de la [licence publique générale GNU](https://fr.wikipedia.org/wiki/Licence_publique_g%C3%A9n%C3%A9rale_GNU) version 2.

**Pour commencer ce tutoriel, vous devez avoir installé `git bash` via le lien du [README.md](https://github.com/AlexShadow3/learning-commands/blob/master/README.md)**

### Les commandes git

#### git version

Maintenant que tout est installé, ouvrez bash (<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="15px" alt="Git">, <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bash/bash-original.svg" width="15px" alt="Bash"> ou <img src="https://mccarter.gallerycdn.vsassets.io/extensions/mccarter/start-git-bash/1.2.1/1499505567572/Microsoft.VisualStudio.Services.Icons.Default" width="15px" alt="Git Bash">) et tapez la commande suivante:

```bash
git --version
```

Cette simple petite commande vous permettra de vérifier que `git` est bien installé sur votre machine. Si tout est bon, vous devriez voir apparaître la version de `git` que vous avez installée.

#### git config

Maintenant que vous avez vérifié que `git` est bien installé, vous allez devoir configurer votre `git`. Pour cela, vous allez devoir renseigner votre nom et votre adresse mail. Pour cela, tapez les commandes suivantes:

```bash
git config --global user.name "Votre nom"
git config --global user.email "Votre adresse mail"
```

Ces commandes permettent de configurer votre `git` pour que vous puissiez commencer à travailler avec. Vous pouvez vérifier que tout est bien configuré en tapant la commande suivante:

```bash
git config --list
```

Vous devriez voir apparaître votre nom et votre adresse mail.
A noter que `--global` permet de configurer `git` pour tous les projets que vous allez créer. Si vous voulez configurer `git` pour un seul projet, vous pouvez omettre `--global`.
`--list` quant à lui permet de lister toutes les configurations de `git`.

#### git init

Maintenant que tout est configuré, vous allez pouvoir créer votre premier repository. Pour cela, vous allez devoir créer un dossier dans lequel vous allez travailler. Une fois ce dossier créé, tapez la commande suivante:

```bash
git init
```

#### git add

Maintenant que votre repository est créé, vous allez devoir ajouter des fichiers à ce repository. Pour cela, créez un fichier `test.txt` et tapez la commande suivante:

```bash
git add test.txt
```

Cette commande permet d'ajouter le fichier `test.txt` à votre repository. Vous pouvez vérifier que le fichier a bien été ajouté en tapant la commande suivante:

#### git status

```bash
git status
```

Cette commande permet de voir l'état de votre repository. Vous devriez voir apparaître le fichier `test.txt` en vert, ce qui signifie que le fichier a bien été ajouté à votre repository (et un fichier modifié mais n'ayant pas été ajouté avec `git add` apparaitra en rouge).

#### git clone

Cette commande permet de cloner un repository. Pour cela, tapez la commande suivante:

```bash
git clone alexshadow3@100.100.1.1:/chemin/vers/le/repository

# ou si vous avez un repository local

git clone /chemin/vers/le/repository

# EXEMPLE

git clone https://github.com/AlexShadow3/learning-commands.git
```

A l'aide de la dernière commande tapée, vous venez de cloner le repository `learning-commands` dans le dossier dans lequel vous vous trouvez.

#### git commit

Maintenant que vous avez ajouté un fichier à votre repository, vous allez devoir le valider. Pour cela, tapez la commande suivante:

```bash
git commit -m "Ajout du fichier test.txt"

# ou si vous voulez ajouter tous les fichiers modifiés

git commit -am "Ajout du fichier test.txt"

# cette dernière commande réalise d'abord un git add puis un commit en y ajoutant un message (-m)
```

Cette commande permet de valider le fichier `test.txt` que vous avez ajouté à votre repository. Vous pouvez vérifier que le fichier a bien été validé en tapant la commande suivante:

#### git log

```bash
git log
```

Cette commande permet de voir l'historique des commits que vous avez effectués. Vous devriez voir apparaître le commit que vous venez de faire (dont votre `username`, `email`, la date et l'heure du commit).

#### git push

Maintenant que vous avez validé votre fichier, vous allez devoir le pousser sur le repository distant. Pour cela, tapez la commande suivante:

```bash
git push origin master
```

Cette commande permet de pousser le commit que vous venez de faire sur le repository distant. Vous devriez voir apparaître le fichier `test.txt` sur le repository distant.

#### git checkout - switch

Maintenant que vous avez poussé votre commit sur le repository distant, vous allez pouvoir créer une branche et même changer de branche. Pour cela, tapez la commande suivante:

```bash
git checkout -b nom-de-la-branche

# ou si vous voulez changer de branche

git checkout nom-de-la-branche
git switch nom-de-la-branche

# Par défaut, la branche principale s'appelle 'master' ou 'main' selon vos préférences
```

Pour faire simple, une branche est une version parallèle de votre repository. Vous pouvez créer une branche pour travailler sur une fonctionnalité sans impacter le reste de votre repository. Une fois que vous avez terminé de travailler sur cette fonctionnalité, vous pouvez fusionner cette branche avec la branche principale.

<h6 align="center" style="color:red">
  ⛔ Attention ⛔
  <br>
  Imaginons que vous créiez une branche et qu'un ami à vous crééais lui aussi une branche et que vous faisiez tous les deux des changements sur les mêmes fichiers, alors vous risqueriez de rencontrer des conflits lors de la fusion de vos branches. Pour éviter cela, il est conseillé de communiquer avec votre équipe pour éviter ce genre de situation. Vous pouvez aussi résoudre vous même les conflits mais cela peut être compliqué.
</h6>

#### git remote

La commande permet de voir les repositories distants que vous avez ajoutés à votre repository local. Vous devriez voir apparaître le repository distant que vous avez ajouté.

```bash
git remote -v
```

Vous pouvez aussi ajouter un repository distant à votre repository local. Pour cela, tapez la commande suivante:

```bash
git remote add origin
```

#### git branch

Cette commande permet de voir les branches que vous avez créées. Vous devriez voir apparaître la branche que vous venez de créer.

```bash
git branch
```

Vous pouvez aussi supprimer une branche. Pour cela, tapez la commande suivante:

```bash
git branch -d nom-de-la-branche

# -d pour delete
```

Vous pouvez aussi renommer une branche. Pour cela, tapez la commande suivante:

```bash
git branch -m nouveau-nom-de-la-branche
```

#### git pull

Cette commande permet de fusionner toutes les modifications présentes sur le repository distant dans le repository local (au cas où votre ami aurait fait des changements sur le repository distant). Pour cela, tapez la commande suivante:

```bash
git pull

# ou

git pull origin master
```

Cette commande permet de récupérer les changements effectués sur la branche principale du repository distant (dans ce cas, la branche `master`).

#### git merge

Cette commande permet de fusionner une branche avec la branche principale. Pour cela, tapez la commande suivante:

```bash
git merge nom-de-la-branche
```

Cette commande permet de fusionner la branche `nom-de-la-branche` avec la branche principale.

#### git diff

Cette commande permet de voir les différences entre deux commits (lorsqu'il y a des confilts par exemple). Pour cela, tapez la commande suivante:

```bash
git diff --base nom-du-fichier-en-conflit

# vous pouvez aussi afficher les différences entre deux branches

git diff nom-de-la-branche-1 nom-de-la-branche-2

# ou juste énumérer tous les conflits

git diff
```

#### git tag

Cette commande permet de taguer un commit. Pour cela, tapez la commande suivante:

```bash
git tag 1.1.0 id-du-commit
```

Cette commande permet de taguer le commit `id-du-commit` avec le tag `1.1.0`.

#### git reset - revert

Ces commandes permetent de revenir à un commit précédent. Pour cela, tapez l'une des commandes suivantes:

```bash
git reset --hard HEAD
git revert id-du-commit
```

#### git rm

Cette commande permet de supprimer un fichier de votre repository. Pour cela, tapez la commande suivante:

```bash
git rm nom-du-fichier
```

#### git stash

Cette commande permet de mettre de côté des modifications que vous avez faites sur votre repository (c'est comme-ci ils étaient mis de côté, vous pourrez les récupérer plus tard si vous le souhaitez). Pour cela, tapez la commande suivante:

```bash
git stash
```

Vous pouvez aussi récupérer vos modifications en tapant la commande suivante:

```bash
git stash pop
```

#### git show

Cette commande permet de voir les modifications effectuées sur tout fichier `git`. Pour cela, tapez la commande suivante:

```bash
git show 
```

#### git fetch

Cette commande permet d'extraire les changements effectués sur le repository distant. Pour cela, tapez la commande suivante:

```bash
git fetch origin
```

#### git ls-tree

Cette commande permet de voir le contenu d'un commit. Pour cela, tapez la commande suivante:

```bash
git ls-tree HEAD
```

Vous devriez voir un fichier arborescent avec le nom et le mode de chaque élément.

#### git cat-file

Cette commande permet de voir le contenu d'un objet dans la base de données `git`. Pour cela, tapez la commande suivante:

```bash
git cat-file -p id-de-l'objet
```

#### git grep

Cette commande permet de rechercher des chaînes de caractères dans les fichiers de votre repository (tout comme la commande Shell). Pour cela, tapez la commande suivante:

```bash
git grep "chaîne-de-caractères"
```

#### gitk

`gitk` est une interface graphique pour `git`. Pour lancer `gitk`, tapez la commande suivante:

```bash
gitk
```

Mais il existe aussi d'autres interfaces graphiques pour `git` comme [Github Desktop](https://desktop.github.com/) ou [Git Kraken](https://www.gitkraken.com/).

#### git instaweb

Cette commande permet de lancer un serveur web pour visualiser votre repository. Pour cela, tapez la commande suivante:

```bash
git instaweb
```

#### git gc

Cette commande permet de nettoyer les fichiers inutiles et les optimiser. Pour cela, tapez la commande suivante:

```bash
git gc
```

#### git archive

Cette commande permet de créer un fichier `.zip` ou `.tar` à partir de votre repository. Pour cela, tapez la commande suivante:

```bash
git archive --format=zip master
```

Cette commande permet de créer un fichier `.zip` à partir de la branche `master`.

#### git prune

Via la commande git prune, les fichiers qui n’ont pas de pointeurs entrants seront supprimés:

```bash
git prune
```

#### git fsck

Cette commande permet de vérifier l'intégrité de votre repository. Pour cela, tapez la commande suivante:
```bash
git fsck
```

#### git rebase

Cette commande permet de réécrire l'historique de votre repository. Pour cela, tapez la commande suivante:

```bash
git rebase master
```

#### git help

La dernière commande de ce guide, l'une des plus importantes, permet d'obtenir de l'aide sur une commande `git`. Pour cela, tapez simplement:

```bash
git help nom-de-la-commande

# ou si vous voulez afficher toutes les commandes

git help -a
```

## Dictionnaire

**Repository**: Un repository est un espace de stockage pour votre projet. Il contient tous les fichiers de votre projet ainsi que l'historique des modifications effectuées sur ces fichiers.

| Nom de la commande | Description | Exemple d'utilisation |
| --- | --- | --- |
| `git version` | Vérifie que `git` est bien installé sur votre machine | `git --version` |
| `git config` | Configure votre `git` | `git config --global user.name "Votre nom"` / `git config --global user.email "Votre email"`|
| `git init` | Crée un repository | `git init` |
| `git add` | Ajoute un fichier à votre repository | `git add test.txt` |
| `git status` | Vérifie l'état de votre repository | `git status` |
| `git clone` | Clone un repository | `git clone https://github.com/alexshadow3/learning-commands.git` |
| `git commit` | Valide un fichier | `git commit -m "Ajout du fichier test.txt"` |
| `git log` | Vérifie l'historique des commits | `git log` |
| `git push` | Pousse un commit sur le repository distant | `git push origin master` |
| `git checkout - switch` | Crée une branche / Change de branche | `git checkout -b nom-de-la-branche` / `git checkout/switch nom-de-la-branche` |
| `git remote` | Vérifie les repositories distants | `git remote -v` |
| `git branch` | Vérifie les branches | `git branch` |
| `git pull` | Fusionne les modifications du repository distant dans le repository local | `git pull` |
| `git merge` | Fusionne une branche avec la branche principale | `git merge nom-de-la-branche` |
| `git diff` | Vérifie les différences entre deux commits | `git diff --base nom-du-fichier-en-conflit` |
| `git tag` | Tag un commit | `git tag 1.1.0 id-du-commit` |
| `git reset - revert` | Reviens à un commit précédent | `git reset --hard HEAD` / `git revert id-du-commit` |
| `git rm` | Supprime un fichier de votre repository | `git rm nom-du-fichier` |
| `git stash` | Met de côté des modifications | `git stash` |
| `git show` | Vérifie les modifications effectuées sur tout fichier `git` | `git show` |
| `git fetch` | Extrait les changements effectués sur le repository distant | `git fetch origin` |
| `git ls-tree` | Vérifie le contenu d'un commit | `git ls-tree HEAD` |
| `git cat-file` | Vérifie le contenu d'un objet dans la base de données `git` | `git cat-file -p id-de-l'objet` |
| `git grep` | Recherche des chaînes de caractères dans les fichiers de votre repository | `git grep "chaîne-de-caractères"` |
| `gitk` | Interface graphique pour `git` | `gitk` |
| `git instaweb` | Lance un serveur web pour visualiser votre repository | `git instaweb` |
| `git gc` | Nettoie les fichiers inutiles et les optimise | `git gc` |
| `git archive` | Crée un fichier `.zip` ou `.tar` à partir de votre repository | `git archive --format=zip master` |
| `git prune` | Supprime les fichiers qui n’ont pas de pointeurs entrants | `git prune` |
| `git fsck` | Vérifie l'intégrité de votre repository | `git fsck` |
| `git rebase` | Réécrit l'historique de votre repository | `git rebase master` |
| `git help` | Obtenir de l'aide sur une commande `git` | `git help nom-de-la-commande` |

