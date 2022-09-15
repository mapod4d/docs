# Come contribuire in modo efficiente

## indice

- [Riferire un bug](#riferire-un-bug)
- [Fare una richiesta di pull](#fare-una-richiesta-di-pull)

**Per favore leggere prima di fare qualcosa!**

## Riferire un bug

La regola d'oro e': **creare sempre *una sola* issue per *ogni singolo* bug**. Se volete
segnalare molti bug, create una nuova issue per ognuno.

## Fare una richiesta di pull

Prima di tutto controllate di proporre un miglioramento utile a tutti.

Seguite queste regole:
- create un fork del repository, meglio del solo branch master
- (opzionale) proteggete il branch master del vostro fork
- fate localmente un git clone https://github.com/USERNAME/docs
- connettet il vostro repository locale con il MAPOD4D repo, fate git remote add mapod4d https://github.com/mapod4d/docs
- per prevenire un push errato MAPOD4D repo, fate git remote set-url --push mapod4d DISABLED
- ogni volta, prima di iniziare un lavoro, fate do git pull mapod4d master o git fetch mapod4d master e next git merge mapod4d/master
- lavorate localmente con git
- fate commit del vostro lavoro
- inviate le push al vostro master
- quando pensate sia utile fate una richiesta di pull dal brench del vostro master remoto al branch master di mapod4d/docs


# How to contribute efficiently

## Table of contents

- [Reporting bugs](#reporting-bugs)
- [Contributing pull requests](#contributing-pull-requests)

**Please read the first section before do something!**

## Reporting bugs

The golden rule is to **always open *one* issue for *one* bug**. If you notice
several bugs and want to report them, make sure to create one new issue for
each of them.

## Contributing pull requests

First of all check to propose an improvement useful to everyone.

Follow this rules:
- do a fork of the repository, better only the branch master
- (optional) protect your branch in the fork
- locally do git clone https://github.com/USERNAME/docs
- connect local repository with MAPOD4D repo, do git remote add mapod4d https://github.com/mapod4d/docs
- to prevent your push on MAPOD4D repo, do git remote set-url --push mapod4d DISABLED
- everytime, before you start a work, do git pull mapod4d master or git fetch mapod4d master and next git merge mapod4d/master
- work locally with git
- commit your work
- send push to your remote master
- when you think it is useful, make a pull request from your remote to the master branch of mapod4d/docs

