# Installer le logiciel Poppy

> **Mise en garde** Si vous souhaitez installer le logiciel d’un robot tangible sur une carte embarquée de type Raspberry Pi, allez plutôt au [chapitre de démarrage](burn-an-image-file.md).

Cette section vous guidera pour installer le logiciel Poppy sur votre ordinateur personnel. Elle est utile **seulement** si vous êtes dans l’une de ces situations : * vous souhaitez contrôler un robot simulé. * Vous souhaitez contrôler une créature Poppy depuis votre ordinateur **sans** utiliser la carte embarquée fournie (Odroid ou Raspberry Pi).

Les créatures Poppy sont contrôlées par du code écrit en langage Python. Selon votre système d’exploitation, vous devrez installer Python et dans tous les cas, vous devrez installer les bibliothèques logicielles requises. Si vous faites vos premiers pas avec Python et que vous souhaitez installer un environnement Python complet conçu pour l'informatique scientifique, **nous vous suggérons d’utiliser [la distribution Python Anaconda](https://www.continuum.io/why-anaconda)**.

## Installer Python et le logiciel Poppy sur Windows

Si vous voulez suivre une vidéo explicative étape par étape de l’installation de Anaconda sur Windows, vous pouvez consulter [ces vidéos](https://www.youtube.com/watch?v=kw9lQwdOlOs&list=PLT6NsCw8bf8T5FG2LGk2y_KTdexi8A5BN) (il s’agit d’une playlist YouTube). <iframe width="560" height="315" src="https://www.youtube.com/embed/videoseries?list=PLT6NsCw8bf8T5FG2LGk2y_KTdexi8A5BN" frameborder="0" allowfullscreen mark="crwd-mark"></iframe> 

### Installer Python et les logiciels Poppy sur Windows

Nous encourageons l’utilisation de la distribution Python Anaconda. Toutefois, si vous avez déjà installé une distribution Python telle que Canopy (livrée avec paquets scientifiques), vous pouvez directement [installer les logiciels Poppy](#install-python-and-poppy-softwares-on-windows).

> **Info** Les bibliothèques logicielles Poppy fonctionnent avec Python 2.7 et Python 3.3 +. Si vous n’êtes pas sûr·e de la version à installer, nous vous suggérons d’utiliser Python 2.7, car nous développons avec cette version.

#### La distribution Anaconda pour Python

[Téléchargez la distribution Anaconda](https://www.continuum.io/downloads) pour Python (400 Mo) [ici pour les ordinateurs 64-bit](https://repo.continuum.io/archive/Anaconda2-4.0.0-Windows-x86_64.exe) ou [ici pour les ordinateurs 32-bit](https://repo.continuum.io/archive/Anaconda2-4.0.0-Windows-x86.exe).

Installez la distribution en cliquant sur « suivant » à chaque étape. Si vous envisagez d’installer Anaconda pour tous les utilisateurs de votre ordinateur, veillez à sélectionner « all users ».

![Anaconda pour tous les utilisateurs](../img/python/lucvincent/luc_vincent-012.png).

Il est également très important que les deux cases à cocher PATH et "default Python" soient bien cochées.

![Installation d’Anaconda](../img/python/anaconda_install_path.png)

Maintenant que vous avez une distribution Python, vous êtes prêt à [installer le logiciel Poppy](#install-python-and-poppy-softwares-on-windows).

#### Python Miniconda (alternative à Anaconda)

Miniconda est une version « allégée » de Anaconda qui contient seulement Python et le gestionnaire de paquets conda. Vous pouvez l’installer **au lieu de Anaconda** et économiser beaucoup d’espace disque (25 Mo vs 400 Mo), mais vous devrez ajouter une nouvelle étape dans le processus d’installation, et vous n’aurez pas de raccourci Jupyter Notebook sur le bureau. Download miniconda [here for 64-bit](https://repo.continuum.io/miniconda/Miniconda2-latest-Windows-x86_64.exe) computer or [here for 32-bit](https://repo.continuum.io/miniconda/Miniconda2-latest-Windows-x86.exe) computer.

Il est également très important que les deux cases à cocher PATH et "default Python" soient bien cochées.

Ouvrez la ligne de commande (appuyez sur les fenêtres principales et tapez « Command Prompt »), tapez et appuyez sur entrée pour exécuter la commande suivante :

    conda install numpy scipy notebook jupyter matplotlib
    

Vous avez maintenant une distribution Python prête à [installer les logiciels Poppy](#install-python-and-poppy-softwares-on-windows).

### Installer les logiciels Poppy sur Windows

Ouvrez la ligne de commande de votre distribution Python (appelée *Anaconda invite* si vous avez installé Anaconda) ou de la *ligne de commande* de Windows, tapez et appuyez sur entrée pour exécuter la commande suivante : ![Anaconda all users](../img/python/lucvincent/luc_vincent-031.png).

> **Note** Remplacez « poppy-ergo-jr » par « poppy-torso » ou « poppy-humanoid » pour installer respectivement un Poppy Torso ou un Poppy Humanoid.

    pip install poppy-ergo-jr
    
    

Ceci va installer tout le nécessaire pour contrôler un Poppy Ergo Jr.

### Mettre à jour le logiciel Poppy sous Windows

En cas de mise à jour, il est conseillé de mettre à jour pypot (la bibliothèque pour le contrôle des moteurs) et le paquet "creature" séparément :

> **Note** Remplacez « poppy-ergo-jr » par « poppy-torso » ou « poppy-humanoid » pour installer respectivement un Poppy Torso ou un Poppy Humanoid.

```bash
<br />pip install pypot --upgrade --no-deps
pip install poppy-creature --upgrade --no-deps
pip install poppy-ergo-jr --upgrade --no-deps
```

> **Info** Pour comprendre les commandes ci-dessus - *--upgrade* désinstallera avant de commencer l’installation - *--no-deps* évitera d’installer les dépendances, c’est utile pour éviter à pip de compiler *scipy* car cela échouera si vous n'avez pas installé les dépendances GCC et Fortran.

## Installer Python et les logiciels Poppy sous Mac OSX

Mac OSX est livré avec une distribution Python installée par défaut. Avant d’installer le logiciel Poppy, vous devez installer le gestionnaire de paquets Python **pip**. Ouvrez un terminal, puis appuyez sur entrée pour exécuter la commande suivante :

    curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | sudo python
    

Vous pouvez maintenant installer le logiciel Poppy pour la créature de votre choix :

> **Note** Remplacez « poppy-ergo-jr » par « poppy-torso » ou « poppy-humanoid » pour installer respectivement un Poppy Torso ou un Poppy Humanoid.

    pip install poppy-ergo-jr --upgrade
    
    

## Installer Python et les logiciels Poppy sous GNU/Linux

Most of GNU/Linux distributions, have already a Python distribution installed by default, but if

### Installer la distribution Python Miniconda

> **Info** Les bibliothèques logicielles Poppy fonctionnent avec Python 2.7 et Python 3.3 +. Si vous n’êtes pas sûr(e) de la version à installer, nous vous suggérons d’utiliser Python 2.7, car nous développons avec cette version.

If you want to have up-to-date numpy, scipy and jupyter without having to compile them, we suggest you to install Anaconda or at least the conda package manager distributed with miniconda. Téléchargez Miniconda (64-bit) avec les commandes ci-dessous dans votre terminal :

    curl -o miniconda.sh http://repo.continuum.io/miniconda/Miniconda-latest-Linux-x86_64.sh
    

Si vous avez un ordinateur 32 bits

     curl -o miniconda.sh http://repo.continuum.io/miniconda/Miniconda-latest-Linux-x86.sh 
    ```
    
    Exécutez les commandes ci-dessous et suivez les instructions pour installer miniconda :
    
    

chmod +x miniconda.sh ./miniconda.sh

    <br />Vous pouvez maintenant installer quelques dépendances requises ou optionnelles pour le logiciel Poppy avec conda :
    

conda install numpy scipy notebook jupyter matplotlib

    Vous pouvez maintenant [installer le logiciel Poppy](#install-poppy-software-on-gnulinux).
    
    
    ### Install dependancies with your operating system package manager (alternative solution to Anaconda/Miniiconda)
    
    Pypot, the main library of the robot is depending (amongst some other) on two big scientific libraries *Numpy* and *Scipy* which are themselves depending on C and Fortran code. These libraries may be installed with the Python package system (pip), but because of the huge number and differences between GNU/Linux distributions pip is not able to distribute binaries for Linux so all dependencies must be compiled... La solution pour éviter la compilation de numpy et scipy est de les installer avec le gestionnaire de paquets présent dans votre distribution.
    
    Sur Ubuntu et Debian : 
    
    ```bash
    curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | sudo python
    sudo apt-get install gcc build-essential python-dev python-numpy python-scipy python-matplotlib
    sudo pip install jupyter
    

Sur Fedora :

```bash
curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | sudo python
sudo yum install gcc python-devel numpy scipy python-matplotlib
sudo pip install jupyter
```

Sur Arch Linux :

```bash
curl --silent --show-error --retry 5 https://bootstrap.pypa.io/get-pip.py | sudo python
sudo pacman -S python2-scipy python2-numpy python2-matplotlib
sudo pip install jupyter

```

Vous pouvez maintenant [installer les logiciels Poppy](#install-poppy-software-on-gnulinux).

> **Note** L’inconvénient est que les bibliothèques Python de votre distribution sont très souvent obsolètes.

### Installer les logiciels Poppy sous GNU/Linux

Ouvrez un terminal, puis appuyez sur entrée pour exécuter la commande suivante :

> **Note** Remplacez « poppy-ergo-jr » par « poppy-torso » ou « poppy-humanoid » pour installer respectivement un Poppy Torso ou un Poppy Humanoid.

    pip install poppy-ergo-jr --user
    

Ceci va installer tout le nécessaire pour contrôler un Poppy Ergo Jr.

### Mettre à jour le logiciel Poppy sous GNU/Linux

En cas de mise à jour, il est conseillé de mettre à jour "pypot" (la bibliothèque pour le contrôle des moteurs) et le paquet "creature" séparément :

> **Note** Remplacez « poppy-ergo-jr » par « poppy-torso » ou « poppy-humanoid » pour installer respectivement un torse Poppy ou un humanoïde Poppy.

```bash
<br />pip install pypot --upgrade --no-deps
pip install poppy-creature --upgrade --no-deps
pip install poppy-ergo-jr --upgrade --no-deps
```

> **Info** Pour comprendre les commandes ci-dessus - *--user* va installer le paquet Python dans des répertoires utilisateur, cela évite d’utiliser `sudo` si vous utilisez l'environnement Python de votre système d'exploitation. - *--upgrade* désinstallera avant de commencer l’installation - *--no-deps* évitera d’installer les dépendances, c’est utile pour éviter à pip de compiler *scipy* car cela échouera si vous n'avez pas installé les dépendances GCC et Fortran