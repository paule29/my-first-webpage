# Documentation

# Configurer mon environnement de développement sous Windows

- installer laragon
- installer visual studio code dans le bin de Laragon :
C:\laragon\bin

- [download vscode](https://code.visualstudio.com/download)
- insataller gitbash dans le bin de Laragon
 - [download git bash](https://git-scm.com/downloads)
    - definir visual studio comme editeur par defaut
    - definir la branche main à la place de master
- definir Git bash comme terminal par défaut dans visual studio code à la place de powershell
    - File > Preference > Settings 
    - Dans le panneau qui vient de s'ouvrir, déplier "features" et cliquer sur "Terminal" 
    - Repérer "Integreted > Automation Shell: Windows" et cliquer sur "Edit in settings.json"
    - Coller la ligne suivante à la place du contenu de settings.json:
    >{"terminal.integrated.shell.windows":}
    "C:\\laragon\\bin\\git\\bin\\bashe.exe"
    
## lier git et github avec GitBash
- dans la barre de tache Windows, utiliser la fonction recherche et taper "Git Gui" aller dans help et show SSH Key et generate key, (si pas besoin de passphrase OK*2) Copier la clef
- Aller dans GitHUB -> Settings du profil -> SSH and PGP Key -> New SSH Key et coller la clef depuis le presse papier. Et cliquer sur "Add key".
- Taper votre MDP GitHub dans le navigateur pour confirmer. 
- Maintenant quand nous voudrons faire un GitClone, il faudra récupérer le lien SSH et non plus le lien HTTPS dans l'interface de GitHub.

# Créer ma 1er page Web

- ouvrir Visual Studio Code, File > Add folder to WorkPlace et ajouter C:\laragon\www à l'espace de travail
- Terminal > New Terminal (un nouveau terminal bash s'ouvre, le symbôle $ indique que nous pouvons commencer à écrire des commandes).
    > dans un Terminal quand vous ne voyer pas $, appuyer sur CTRL+C pour terminer le processus. 
- Taper la CMD: $mkdir nom de dossier   
    > mkdir exemple
    > 
    >Pour créer un dossier exemple dans le répertoire. Notez que vous pouvez aussi créer les dossiers parents en ajoutant -p (ex: mkdir -p parent/exemple créera d’abord un dossier parent avant de créer un dossier exemple dans celui-ci

- taper ensuite: cd nom de dossier
    > cd exemple
    >
    >Permet de naviguer dans le répertoire exemple. Notez que vous pouvez simplement utiliser cd exemple si vous vous trouvez dans le répertoire du dossier auquel vous voulez accéder.

- taper git init pour initialiser le depot (*repository*) de version dans le répertoire dans lequel vous vous êtes positionné.

> Ne pas confondre le repetoire courant qui contient des fichiers et le repository qui contient les versions. 

- taper " $> README.md index.php style.css " 
- dans le panneau de gauche de VSCode, derouler le dossier et cliquer sur index.php pour commencer à l'éditer.
- deux choses: pour commencer à taper du HTML dans index.php, taper ! puis tab pour generer un doctype, entre les balises Head, ajouter une ligne, écrire link et choisir link CSS dans le menu déroulant qui s'affiche et commencer à taper du html entre les balises Body.

- taper dans l'éditeur ``` <?php ?>``` , ecrire du code php entre la balise ouvrante et fermante.
    >(taper 3 fois altgr+7 et ce mettre au milieu des 6`pour taper du code en MarkDown)
- dans une balise HTML vous pouvez declarer une id en écrivant dans la balise après le nom de la balise et avant le chevron fermant ``` id="nom-de-l-id```, puis ouvrir style.css et écrire ``` # nom-de-l-id{écire des proprietes CSS et des valeurs ici}```
- enregistrer les fichiers: CTRL+S

# Synchroniser le depot local avec un depot en ligne sur GitHub

- dans la console, taper ```$git remote [url du repository]```
- Puis: 
    - $git add . 
    - $git commit -m "description du commit" 
    - $git push

# Créer un nouveau repository 