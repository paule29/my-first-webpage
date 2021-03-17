# documentation

## configurer mon environnement de developpement sous windows

- installer laragon
- installer visual studio code dans le bin de laragon : C:\laragon\bin
    - [download vscode](https://code.visualstudio.com/download)
- installer git bash dans le bin de laragon 
    - [download git bash](https://git-scm.com/downloads)
    - définir visual studio code comme éditeur par défaut
    - définir la branche *main* à la place de *master*
- définir git bash comme terminal par défaut dans visual studion code à la place de powershell
    - File > Preferences > Settings
    - dans le panneau qui s'est ouvert, déplier "Features" et cliquer sur "Terminal"
    - Repérer "Integrated > Automation Shell: Windows", et cliquer sur "Edit in settings.json"
    - Coller la ligne suivante à la place du contenu de settings.json :
    >{"terminal.integrated.shell.windows": "C:\\laragon\\bin\\git\\bin\\bash.exe"}