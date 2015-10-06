# GenerPdf

[![Join the chat at https://gitter.im/Ugarz/GenerPDF](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Ugarz/GenerPDF?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Réalisé avec [Sails](http://sailsjs.org), c'est une application web qui permet de générer un pdf lorsque l'on y est connecté.
Je pars du postulat que vous avez installé les outils que votre bécane aura besoin pour lancer ce projet.

| Outil	        | Rôle          												 | Link or command								     |
| ------------- |:--------------------------------------:| -----------------------------------:|
| Node 					| Permet d'utiliser les dépendances      | `sudo apt-get install nodejs npm`   |
| Grunt		      | Permet d'automatiser des tâches        | `npm install -g grunt-cli` 				 |
| Nodemon	      | Permet de lancer le serveur de l'appli | `npm install -g nodemon` 				   |

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

### La structure du projet
C'est la phase la plus mouvante.
Dans les jours / semaines à venir c'est tout sa structure qui va bouger, notemment parce que c'est encore balbutiant, mais surtout parce que c'est ici que le coeur va se faire.

### Workflow à venir
1. Dans un premier temps il faut créer une connexion.
	1. Faire une vue de connexion
	2. Ajouter une base mysql et la relier au projet (avec l'ORM de Sails [Waterline](https://github.com/balderdashy/waterline)).
2. Quand nous aurons un template dédié au front et back, on utilisera les websockets avec [socket.io](http://socket.io) pour faire une vue backend dynamique pour la génération d'un pdf.
3. Une vue backend (uniquement accessible par connexion) permettra de générer un pdf avec un header, un body et un footer.
	1. Génération du pdf avec [pdf-kit](https://github.com/pdfkit/pdfkit) et [Momentjs](http://momentjs.com/) pour la gestion des dates.
	2. Ensuite il faudra ajouter l'envoi par mail du dit pdf. Je pense qu'un petit [Nodemailer](https://github.com/andris9/Nodemailer) fera l'affaire.
4. Le projet à ce stade pourrait suffir, mais on rajoutera un formulaire sur la vue backend pour ajouter des informations depuis la base de donnée.


### Le style du projet
Les vues sont compilées grâce à `views/layout.ejs`.
Le CSS s'ajoute soit directement dans la vue, soit dans un fichier situé dans `assets/styles/monstyle.css`.
Pour ce qui est du style, un support du scss a été ajouté : vous pouvez créer vos styles dans `assets/styles/`. Si vous souhaitez ajouter des styles il suffit de créer un fichier comme `assets/style/monstyle.scss` et d'ajouter une ligne dans `assets/styles/importer.scss` pour dire de prendre en compte vos styles. Et voilà.