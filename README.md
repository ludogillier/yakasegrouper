Symfony De base 2.4 && admin generator && fosuser avec les composants bootstrap 2.3.2
=======================================================

# Contenu

Cette version contient 2 bundle


1) Méthode archive en ligne de commande
----------------------------

    git archive --format=tar --remote=git@gitlab.atixnet.net:symfony2-4.git admingen-fosuser | (mkdir symfony2.4 && cd symfony2.4 && tar xf -)

ou

    git archive --format=zip --remote=git@gitlab.atixnet.net:symfony2-4.git admingen-fosuser | (mkdir symfony2.4 && cd symfony2.4 && tar xf -)


2) Méthode récupérer le repositorie avec sourcetree
---------------------------------------------------

Clone git@gitlab.atixnet.net:symfony2-4.git

Ouvrir la branche admingen-fosuser (ajouter une branche locale puis se positionner sur cete branche)


Supprimer le répertoire .git (Explorateur de fichier)

3) Méthode récupérer le repositorie en ligne de commande
--------------------------------------------------------

    git clone -b admingen-fosuser --single-branch git@gitlab.atixnet.net:symfony2-4 symfony2.4 && cd symfony2.4 && rm -Rf .git

4) methode recuper

# Installation

    composer install

BDD

    php app/console doctrine:database:create
    php app/console doctrine:schema:create

Création de l'utilisateur

    php app/console fos:user:create

> Please choose a username:admin
> Please choose an email:admin@atixnet.fr
> Please choose a password:admin

    php app/console fos:user:promote

> Please choose a username:admin
> Please choose a role:ROLE_ADMIN
> Role "ROLE_ADMIN" has been added to user "admin".

    php app/console assets:install
