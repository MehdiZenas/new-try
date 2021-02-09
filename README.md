# DevCommeLesPros-2021-Exo0

Modèle de départ servant à la mise en place des outils de travail pour ce cours.

<!-- TOC depthfrom:2 -->

- [Objectif](#objectif)
- [Installation de Visual Studio Code pour le développement C et C++](#installation-de-visual-studio-code-pour-le-d%C3%A9veloppement-c-et-c)
    - [Instructions pour Windows](#instructions-pour-windows)
    - [Instructions pour macOS](#instructions-pour-macos)
    - [Instructions pour Linux](#instructions-pour-linux)
- [GitHub et votre premier dépôt](#github-et-votre-premier-d%C3%A9p%C3%B4t)
    - [Instructions pour tous](#instructions-pour-tous)
- [Évaluation](#%C3%A9valuation)

<!-- /TOC -->

## Objectif

Ces instructions vont vous servir à installer et configurer [Visual Studio Code](https://code.visualstudio.com) sur votre propre ordinateur.
Code est un programme qui sert d'environnement de dévelopement.
C'est une collection d'outils propres à la programmation.
Principalement, c'est un navigateur de fichiers, un éditeur de texte et une interface de débogage et, accessoirement, encore bien d'autres choses.
Code pourra vous servir ultérieurement dans le contexte d'autres cours de programmation.
Code est aussi déjà installé sur les ordinateurs de l'université.

Vous aurez aussi à créer un compte sur [GitHub](https://github.com), le service d'hébergement de dépôts de code que nous utiliserons pour ce cours.
Une fois fait, vous procéderez à créer votre premier dépôt.

## Installation de Visual Studio Code pour le développement C et C++

Visual Studio Code est disponible pour tous les systèmes d'exploitation majeurs et son interface est la même partout.
Cette uniformité m'est utile dans un contexte d'enseignement mais je veux que vous puissiez tous tout de même utiliser l'ordinateur que vous avez déjà.

Par contre, Code est un environnement de programmation qui est au départ indépendant du langage de programmation utilisé et ne peut compiler un programme en C par soi-même.
On doit donc aussi installer un compilateur (comme `gcc` avec lequel vous êtes déjà familier) et Code y fera appel.
L'installation du compilateur diffère dépendamment de votre système d'exploitation.

Personnellement, je compile et teste vos programmes sous Debian (la «distro» Linux que l'on retrouve sur les ordinateurs de l'université) et le compilateur `gcc`.

Suivez les instructions qui correspondent à votre situation :

### Instructions pour Windows

Pour travailler sous Windows, je conseille d'installer [Windows Subystem for Linux](https://fr.wikipedia.org/wiki/Windows_Subsystem_for_Linux).
En mots très simples, WSL est une machine virtuelle qui vous donnera une vue de vos fichiers sous Windows à travers une lunette Linux.
On peut naviguer ses fichiers et lancer des programmes propres à Linux à l'invite de commandes UNIX classique.
WSL vous permet donc de compiler et déboguer vos programmes avec le même `gcc` que l'on retrouve sur les ordinateurs de l'université.

Suivez [ces instructions](https://code.visualstudio.com/docs/cpp/config-wsl) pour installer WSL, compilateur, débogueur, Visual Studio Code et l'extension `C/C++`.
Vous avez le choix de la «distro» Linux.
Ubuntu est essentiellement la plus populaire.
Debian est celle que l'université utilise.
(Parmi les trois systèmes d'exploitations, ces instructions sont les plus lourdes mais je crois qu'avoir une machine virtuelle Linux vous sera bénéfique.)

### Instructions pour macOS

Le compilateur C, C++ (et autres) d'Apple est AppleClang qui est une [fourche](https://fr.wikipedia.org/wiki/Fork_(d%C3%A9veloppement_logiciel)) de [Clang](https://fr.wikipedia.org/wiki/Clang).
Clang est un compilateur qui se garde compatible avec gcc.
AppleClang est installé avec les [Command Line Tools for Xcode](https://download.developer.apple.com/Developer_Tools/Command_Line_Tools_for_Xcode_12.2/Command_Line_Tools_for_Xcode_12.2.dmg).

Suivez [ces instructions](https://code.visualstudio.com/docs/cpp/config-clang-mac) pour installer compilateur, débogueur, Visual Studio Code et l'extension `C/C++`.

### Instructions pour Linux

C'est la configuration la plus facile.
Il n'y a qu'à installer le compilateur et débogueur à l'invite de commande s'ils n'y sont pas déjà.

Suivez [ces instructions](https://code.visualstudio.com/docs/cpp/config-linux) pour installer compilateur, débogueur, Visual Studio Code et l'extension `C/C++`.

## GitHub et votre premier dépôt

Vous pouvez créer un compte avec votre adresse mail unversitaire mais vous pouvez utiliser l'adresse que vous voulez.
Vous aurez évidement le loisir de créer d'autres comptes plus tard avec un identité autre que votre «identité universitaire».
Vous avez déjà un compte GitHub ? Tant mieux mais je devrai évidement savoir qui se cache derrière ce pseudo au moment de vous évaluer. S'il n'est pas évident, signalez-moi quel est votre pseudo par mail.

Pour vous faciliter la vie, je vous conseille de créer une [clé SSH](https://en.wikipedia.org/wiki/Ssh-keygen) qui servira à vous authentifier automatiquement avec ce service et vous évitera d'avoir à trop répétitivement tapper votre mot de passe.
Une clé SSH est une clé de chiffrement asymétrique.
Elle est donc divisée en deux parties, une publique et une privée.
GitHub aura besoin de votre clé publique pour savoir vous reconnaître.

Vous aurez à communiquer fréquemment avec GitHub lors de vos exercices.
Pour automatiser le processus d'authentification avec GitHub, on utilise un agent.
[ssh-agent](https://fr.wikipedia.org/wiki/Ssh-agent) (ou [Pageant](https://en.wikipedia.org/wiki/PuTTY) pour Windows) est un outil qui reconnaît les serveurs auxquels on s'adresse et nous authentifie automatiquement.
Cet agent doit être re-lancé si vous redémarrez votre ordinateur ou être configuré pour être lancé automatiquement dès sone démarrage.

Toutes ces instructions ont leur version propre à votre système d'exploitation.
Chaque lien d'aide GitHub le reconnaîtra automatiquement.
Pour certains, les instructions pourront vous suggérer d'utiliser un client graphique vers GitHub, vous êtes libre de le faire mais dans un but d'uniformité, je ferai toujours référence à `git` par son interface d'invite de commandes.

### Instructions pour tous

Pour toutes ces instructions, si vous travaillez sous Windows+WSL, suivez les instructions pour Linux et considérez le terminal WSL comme un terminal Linux.

1. Créez un compte GitHub.
    - http://github.com/join
1. Créez une clé SSH, ajoutez-la au `ssh-agent` et notifiez GitHub.
    - Suivez [ces instructions](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) pour créer les clés publique et privée et les ajouter à un agent.
    - Suivez [ces instructions-ci](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) pour partager la clé publique avec GitHub.
    - Générez une clé par compte/ordinateur.
    P. ex. si vous travaillerez de votre propre ordinateur et de votre compte universitaire, il vous faudra deux clés.
1. Configurez `git` localement avec votre nom et votre adresse mail :
    - `$ git config --global user.name “Nom Prénom”`
    - `$ git config --global user.email [votre adresse mail]`
    - Encore une fois, opérez cette configuration sur chaque ordinateur où vous travaillerez.
1. Créez votre propre copie de [ce dépôt](https://github.com/Amu-DevCommeLesPros-2021/DevCommeLesPros-2021-Exo0) que vous lisez présentement en l'utilisant comme modèle.
    - Suivez [ces instructions](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
        - Vous pouvez gardez le même nom de dépôt que celui-ci.
        - Choisissez l'option `Private` à l'étape 5.
    - Attention : il ne s'agit pas de créer un tout nouveau dépôt ou de faire une [fourche](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) ! Pour tous les exercices, celui-ci inclus, vous utiliserez mes dépôts comme point de départ avec leurs fichiers avec la fonctionalité «Use this template» («Utiliser ce modèle»).
1. Ajoutez le professeur comme collaborateur à votre dépôt.
    - Suivez [ces instructions](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository).
        - Nom d'utilisateur à ajouter : `thierryseegers`.
1. Clonez votre dépôt vers votre espace de travail local.
    - Suivez [ces instructions](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/cloning-a-repository).
        - À l'étape 3, choisissez «Use SSH».
    - Attention à ne pas cloner https://github.com/Amu-DevCommeLesPros-2021/DevCommeLesPros-2021-Exo0 mais bien votre propre dépôt nouvellement créé.
1. Lancez Visual Studio Code.
    - À l'invite de commandes :
        - `$ cd [nom de votre dépôt]`
        - `$ code .`
    - Ou alors, lancez Code par soi-même et ouvrez le dossier où se trouve le dépôt cloné.
1. Vous devriez voir ce fichier, `README.md`, dans sa forme «[markdown](https://fr.wikipedia.org/wiki/Markdown)».

## Évaluation

Je m'attends à recevoir une invitation à votre dépôt avant l'échéance donnée en cours.
