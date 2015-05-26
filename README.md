# Configuration nouveau Mac
## Remarques de base
* pour chercher un logiciel, utliser la loupe en haut a droite de l'écran ou le raccourci cmd+espace
* Quand l'ordinateur demande un mot de passe admin, c'est le mot de passe qui sert à ouvrir l'ordi.


## Logiciels pratiques
* Bettertouchtool pour que les fenetres se redimentionnent sur les bords : http://www.bettertouchtool.net/
* sublime text 2 pour l'éditeur de texte

## Configuration de sublime text 2
* installer le gestionnaire de paquets : https://packagecontrol.io/installation#st2
* Une fois installer, via cmd+maj+P on peut choisir "install Package" et installer tout plein de packages (dont coffeescript)
* Aller dans les préférences et faire les réglages suivants : 
```

    // The number of spaces a tab is considered equal to
    "tab_size": 2,

    // Set to true to insert spaces when tab is pressed
    "translate_tabs_to_spaces": true,

```
Comme cela chaque tabulation correspondra à deux espaces.

## Prérequis
* Installation des outils dev apple : ouvrir le terminal (appuyer sur cmd+espace pour l'outil de recherche et taper "terminal" puis entrée) et taper `gcc`. Cela devrait ouvrir une fenetre proposant une mise a jour, accepter et la lancer.
* Installer Homebrew (outil de téléchargement et installation d'outils :p) : http://brew.sh/
* Installer how my zsh (meilleur shell) : `curl -L https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh` Quitter et redémarrer le terminal quand c'est fini, ça devrait être tout joli

## Installation des autres outlis

Executer cette ligne : 

`bash <(curl -s https://raw.github.com/applidget/laptop/master/mac)`

## Note 
* Testé seulement sous Yosemite



## Autres logiciels (optionnels)
* Heroku toolbelt : https://toolbelt.heroku.com/
* AWS cli : `brew install python` puis `pip install awscli`
* AWS auto-scaling : installer JAVA JDK (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) puis télécharger l'archive ici : https://aws.amazon.com/developertools/2535 puis copier bin lib et le fchier de credentials dans ~/.auto-scaling ajouter dans le zshrc : 
```
export AWS_AUTO_SCALING_HOME="/Users/BCoulange/.auto-scaling"
export JAVA_HOME=`/usr/libexec/java_home -v 1.8
export AWS_CREDENTIAL_FILE="/Users/BCoulange/.auto-scaling/credential-file-path.template"
export PATH="$PATH:${AWS_AUTO_SCALING_HOME}/bin"
```

Enfin limiter les permission sur le fichier de credentials modifié : `sudo chmod 600 ~/.auto-scaling/credential-file-path.template`

## Rmagick et Imagemagick
brew install imagemagick
gem install rmagick

## Latex / générateur de rapport
* Télécharger MacTex : http://www.tug.org/mactex/
* L'installer

## Opencv
````
brew tap homebrew/science
brew install opencv
````

## Enblend
* le téélcharger ici : http://enblend.sourceforge.net/
* Copier le fichier binaire "enblend" dans "/usr/bin"

## Pour Cornis Maps
gem uninstall libv8
brew install v8
gem install therubyracer
gem install libv8 -v '3.11.8.17'  -- --with-system-v8


