Ce projet est un test pour mettre en ligne via github un site web (sans back-end) grâce a l'url github.io

Créer un repositorie, ajouter le sur votre ordi pour pouvoir faire les commande dans un cli.

npx create-react-app test-pages : création du dossier react
cd test-pages

Faite un premier push de la manière que vous préférer, pour ma part je le fait depuis github-desktop

Ensuiste faite la commande suivant:
npm i gh-pages --save-dev

Ensuite dans le package.json, ajouter les lignes suivantes:
Dans les première accolades avant les dépendances ajouter cette ligne
"homepage": "https://redes19.github.io/test-pages", Attention l'url comporte https://nom_utilisateur.github.io/nom_du_projet

Puis dans les scripts ajouter les lignes suivantes,
-"predeploy": "npm run build",
-"deploy": "gh-pages -d build"

Après cela, entrez dans le terminal :
npm run build
Cela créera un dossier build dans votre app

Pour conclure ajouter les modification avec les commande suivantes:
git add .
git commit -m "deploy app"  le message n'a pas d'importance mais il est obliger d'en mettre un.
git push

Enfin vous pourez aller sur votre page github, aller dans les settings et à gauche cliquez sur pages. Vous pourrez retrouver votre url et visiter votre site react.

