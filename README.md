# GenerPdf

Réalisé avec [Sails](http://sailsjs.org), c'est une application web qui permet de générer un pdf lorsque l'on y est connecté.

## Premiers pas
Pour commencer à utiliser le projet, utilisez le lien ssh [git@github.com:Ugarz/GenerPDF.git](http://git@github.com:Ugarz/GenerPDF.git).

### On clone le projet
```
git clone git@github.com:Ugarz/GenerPDF.git
```

### On entre et installe les dépendances
```
cd GenerPDF && npm install
```

### lancez le projet avec 
```
nodemon app.js
```
Et rendez vous sur [http://localhost:1337](http://localhost:1337)

## Edition du projet
Les vues sont compilées grâce à `views/layout.ejs`. Pour ce qui est du css, un support du scss a été ajouté et vous pouvez créer vos styles dans `assets/styles/`.
Si vous souhaitez ajouter des styles il suffit de créer un fichier `assets/style/monstyle.scss` et d'ajouter une ligne dans `assets/styles/importer.scss` pour dire de prendre en compte vos styles.