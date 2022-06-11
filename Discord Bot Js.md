<h1 style="color:yellow">Comment créer un Bot Discord en JS ?</h1>
<br>

Nous allons voir ensemble :

* [Quelle est la bibliothèque js essentielle à utiliser]
* [Comment faire un chatbot Discord avec Node JS]
* [Comment héberger son bot gratuitement ou pas]

<br>

<h2 style="color:yellow">Un tutoriel bot Discord Node JS facile</h2>

<br>

Faire une application Discord n’est pas très compliqué. Dans ce tutoriel, nous utiliserons le JavaScript et les exemples de bases de bots disponibles sur le site officiel de Discord pour développeurs.

Comme je vous fournis la base du code, il ne vous reste plus qu’à y ajouter de la complexité à l’aide de conditions et autres structures de contrôle. Armé de ces connaissances fondamentales en code, vous devriez être capable de faire à peu près tout ce que vous voulez avec votre bot Discord.

Si vous n’avez pas compris le paragraphe du dessus car vous n’avez pas les connaissances de base en code, je vous invite à apprendre la base du JavaScript sur [FreeCodeCamp](https://www.freecodecamp.org/) ou le tutoriel [Apprendre à Coder avec Javascript sur OpenClassroom](https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript?archived-source=2984401) si vous ne parlez pas anglais.

<br>

<h2 style="color:yellow">Pourquoi Discord.js ?</h2>

<br>

Il est possible de créer des bots Discord dans plusieurs langages de programmation. Que ce soit en Rust, Swift, Python, Ruby, PHP, Java ou autre, les développeurs de Discord recommandent un certain nombre de bibliothèques pour interagir avec leur API et une simple recherche Google ou sur Github vous permettra de trouver des APIs moins reconnues par l’équipe Discord dans votre langage de programmation préféré.

<br>

<h2 style="color:yellow">Programmer un bot Discord v12 en Javascript avec Node JS</h2>
<br>

Pour ce tuto, c’est JavaScript que j’ai choisi pour sa simplicité et son universalité. Le JS prend le dessus sur beaucoup de fronts en programmation depuis ces dernières années. L’application de chat Discord elle-même est codée en JavaScript avec React, Electron et React-Native, toutes des librairies JS.

Mon blog mettant principalement l’accent sur le fait de “leverage” le code pour arriver à ses fins avec ces mêmes technologies, c’est donc tout naturellement que nous utiliserons la librairie Discord.js v12 pour ce premier tuto sur l’utilisation des applications Discord.

<br>

<h2 style="color:yellow">Comment installer NodeJS ?</h2>

<br>

Node permet d’exécuter du JavaScript comme un programme, sur un ordinateur, un téléphone ou un serveur. Il s’installe comme un programme classique sur votre ordinateur ou par ligne de commande.

<br>

### INSTALLER NODE JS SUR WINDOWS

<br>

![Logo node JS](https://www.commentcoder.com/static/df6ce652bdd1f70bf220efa823b30545/b17f8/utiliser-node-js-avec-discordjs.jpg)

<br>

Rendez-vous [la page de téléchargement pour Windows de NodeJS](https://nodejs.org/fr/download/) et choisissez la version LTS pour Windows. Suivez le processus d’installation et vous devriez avoir tout ce qu’il faut pour commencer à programmer votre bot.

<br>

### NODEJS POUR MAC ET LINUX
Pour Mac et Linux, vous pouvez soit télécharger le GUI pour installer Node comme pour windows en allant sur [la page de téléchargement pour Mac OSX ou Linux de NodeJS.](https://nodejs.org/fr/download/)

Si vous préférez passer par la console ou que vous êtes sur Linux, vous pouvez passer par votre gestionnaire de paquets préféré comme **brew, apt, yum, dpkg, rpm, pacman** ou un autre.

<br>

<h2 style="color:yellow">Installer Discord.js</h2>

Avec Visual Studio Code ou PowerShell sur Windows ou votre terminal préféré sur Mac et Linux, rendez-vous dans le dossier dans lequel vous voulez créer votre bot Discord. C’est un dossier dans lequel se trouveront les fichiers JavaScript et la configuration de votre bot. Vous pouvez le mettre n’importe où, tant que c’est un nouveau dossier vide pour rester organisé.

Une fois dans le dossier, initialisons le projet avec npm grâce à la commande :

```batch
npm init
```

Répondez oui à toutes les questions ou insérez les informations que vous voulez.

Si tout s’est bien passé, vous avez maintenant un dossier fermé dans lequel l’environnement de votre projet réside.

Installons maintenant Discord.js v12 avec la commande :

```batch
npm install discord.js
```

<br>

<h2 style="color:yellow">Configurer Discord.js</h2>

<br>

Une fois Node installé, votre machine devrait avoir tout ce qu’il faut pour pouvoir installer la bibliothèque discord.js et vous pourrez commencer à programmer le bot. Mais avant cela, il faut faire un petit tour sur le site de Discord pour récupérer des identifiants, voyons tout cela ensemble.

<br>

<h2>Où mettre le client id et le token de Discord dans votre code JavaScript ?</h2>

Retournez sur le portail de développeurs de Discord pour récupérer le token que l’on va mettre dans notre projet.

<br>

![tkdiscordbot](https://www.commentcoder.com/static/5a4794f4671c2c9e0f883853afaa7fbf/b17f8/token-bot-discord.jpg)

<br>

Créez un fichier JavaScript, par exemple **index.js** et ce code pour commencer :

```js
const Discord = require('discord.js');
const client = new Discord.Client();
const token = ‘INSÉREZ VOTRE TOKEN ICI’

client.once('ready', () => {
   console.log('Félicitations, votre bot Discord a été correctement initialisé !');
});

client.login(token);

```

Veillez à bien insérez votre token à la ligne 3 entre les apostrophes.
Sauvez votre fichier et lancez la commande node **index.js** (remplacez index.js par le nom de votre fichier si vous avez choisi un autre nom).

Si vous voyez le message **Félicitations, votre bot Discord a été correctement initialisé !**, c’est que tout s’est passé comme prévu, votre bot est bien lié à votre serveur Discord et nous pouvons commencez à ajouter de l’intelligence pour qu’il fasse des choses utiles.

Note : Si on vous vole le token du bot, on a accès à votre bot, n’hésitez pas à le régénérer sur le Portail de Développeur Discord. Vous devrez alors remplacez l’ancien token dans votre code par le nouveau, l’ancien étant maintenant inactif.

<h2 style="color:yellow">Exploiter au mieux Discord.js</h2>

Vous possédez maintenant toutes les clés pour vous aider dans la réussite de votre serveur Discord. Grâce aux différentes possibilités qu’un bot Discord vous offre.
Félicitations, vous avez tout ce qu’il faut pour créer un bot original qui correspond exactement à vos attentes !
Je vous souhaite un serveur Discord populaire grâce à son automatisation et que l’API Discord.js vous mène vers d’autres créations par le code.
Vous avez maintenant un boilerplate qui fonctionne, le temps est venu de s’amuser en explorant l’API Discord.js v12.
Il existe de nombreuses manières d’automatiser ses tâches et de créer des interactions avec ses membres. Je vous en montre 3 ici avec du texte, des images et de la voix.

<h2 style="color:yellow">Répondre a une message</h2>

```js
client.on("message", message => {
  if (message.content === "!ping") {
    message.channel.send("Pong.")
  }
})

```

<h2 style="color:yellow">Créer une commande Discord js</h2>

Vous savez maintenant intéragir simplement avec un serveur Discord. Pour une meilleure organisation, les bots Discord js suivent une convention qui est de créer un dossier commands dans lequel on met toutes notes commandes. Ainsi, si on créait la commande pour kicker des utilisateurs, on aurait un fichier **kick.js** dans le dossier command et on appelerait la commande dans **index.js**.

Créez un dossier commandes à la racine du dossier.

Créez un fichier kick.js et utilisez ce code :

```js
module.exports = message => {
  const member = message.mentions.members.first()
  if (!member) {
    return message.reply(`Utilisateur pas trouvé ou pas spécifié`)
  }
  if (!member.kickable) {
    return message.reply(`L'utilisateur n'est pas kickable`)
  }
  return member
    .kick()
    .then(() => message.reply(`L'utilisateur ${member.user.tag} a été kicked`))
    .catch(error => message.reply(`Une erreur s'est produite`))
}
```

Importez la commande dans votre fichier principal **index.js**, importez et appelez la commande kick comme ceci :

```js
const kick = require("../commands/kick")
module.exports = (client, message) => {
  if (message.content.startsWith("!kick")) {
    return kick(message)
  }
}
```