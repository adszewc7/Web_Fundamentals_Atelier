# 📒 Mon carnet de bord

**Nom :** Szewc

**Prénom :** Adrien

**Adresse de mon site :** https://adriensz7.pythonanywhere.com

> Modifiez ce fichier directement sur GitHub (icône crayon ✏️) pour répondre aux questions de chaque exercice.
> Écrivez avec vos propres mots : une réponse courte et juste vaut mieux qu'un long copier-coller ! 🙂

---

## 🟢 Exercice 1 — Mon premier déploiement

1. Où se trouve physiquement le code qui fabrique votre page : sur votre ordinateur, sur GitHub ou sur PythonAnywhere ?

   > _Ma réponse :_ Sur PythonAnywhere. GitHub sert seulement à stocker le code, et mon ordinateur ne fait qu'afficher la page. C'est le serveur PythonAnywhere qui éxecute la page.

2. Pourquoi votre voisin(e) peut-il voir votre site, alors que vous n'avez rien installé sur son ordinateur ?

   > _Ma réponse :_ Le site tourne sur un serveur connecté à Internet en permanence. N'importe quel navigateur peut lui envoyer une requête et recevoir la page. Il n'y a rien à installer, un navigateur suffit.

---

## 🟢 Exercice 2 — Les URL et les routes

1. Dans l'URL `https://www.google.com/maps`, quel est le nom de domaine ? Quel est le chemin ?

   > _Ma réponse :_ Le nom de domaine est `www.google.com` et le chemin est `/maps`.

2. Que veut dire le message *Not Found* ? Qui l'a envoyé : votre navigateur ou le serveur ?

   > _Ma réponse :_ Ça veut dire que la page demandée n'existe pas, parce qu'aucune route ne correspond à cette adresse. C'est le serveur qui l'envoie (erreur 404).

3. Que se passe-t-il si deux fonctions portent le même nom dans `flask_app.py` ? (Indice : essayez, puis lisez l'Error log.)

   > _Ma réponse :_ Flask plante au démarrage avec l'erreur `AssertionError: View function mapping is overwriting an existing endpoint function`. Le site ne marche plus et affiche "Something went wrong".

---

## 🔵 Exercice 3 — Le langage HTML

1. Quelle est la différence entre ce que le serveur **envoie** et ce que le navigateur **affiche** ?

   > _Ma réponse :_ Le serveur envoie du simple texte avec des balises HTML. Le navigateur interprète ces balises et affiche une page mise en forme (titres, listes, images…).

2. À quoi servent les balises `<h1>`, `<p>`, `<ul>` et `<li>` ?

   > _Ma réponse :_ `<h1>` sert pour un titre principal, `<p>` pour un paragraphe, `<ul>` pour une liste à puces et `<li>` pour un élément de cette liste.

3. Pourquoi l'image s'affiche-t-elle alors qu'elle n'est pas sur votre serveur ?

   > _Ma réponse :_ La balise `<img>` contient l'adresse de l'image sur un autre serveur (Wikimedia). Le navigateur va la télécharger lui-même directement là-bas.

---

## 🔵 Exercice 4 — Les templates

1. Pourquoi est-ce une bonne idée de séparer le code Python et le HTML ? (Pensez à une équipe avec un développeur et un graphiste.)

   > _Ma réponse :_ Chacun travaille sur son fichier sans gêner l'autre : le développeur sur le Python, le graphiste sur le HTML. Le code est aussi plus lisible, et un même template peut être réutilisé avec des données différentes.

2. Les `{{ prenom }}` sont-ils remplacés par le serveur ou par le navigateur ? Comment l'avez-vous vérifié ?

   > _Ma réponse :_ Par le serveur. En affichant le code source de la page (Cmd+Option+U), on voit directement "Adrien Szewc" : les `{{ }}` ont déjà disparu avant d'arriver au navigateur.

---

## 🔵 Exercice 5 — Le CSS et les liens

1. Quelle est la différence de rôle entre le HTML et le CSS ?

   > _Ma réponse :_ Le HTML définit la structure et le contenu de la page. Le CSS définit son apparence : couleurs, polices, marges.

2. Pour afficher votre page `/presentation`, combien de fichiers le navigateur doit-il télécharger ? (Vous pourrez le vérifier à l'exercice suivant !)

   > _Ma réponse :_ 3 fichiers : la page HTML, le fichier `style.css` et l'image du logo Python.

3. Pourquoi faut-il parfois faire **Ctrl + F5** pour voir les changements de CSS ?

   > _Ma réponse :_ Le navigateur garde le CSS en cache pour charger plus vite, donc il peut réutiliser l'ancienne version. Ctrl+F5 force le navigateur à retélécharger le fichier.

---
## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > _Ma réponse :_ ## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > _Ma réponse :_ HTTP veut dire *HyperText Transfer Protocol* : ce sont les règles de communication entre un navigateur et un serveur Web. Le navigateur (le client) envoie la requête, et le serveur renvoie la réponse.

2. Combien de requêtes votre page `/presentation` a-t-elle déclenchées ? Lesquelles ?

   > _Ma réponse :_ 2 requêtes : la page `/presentation` (le HTML) et le fichier `style.css`, demandé parce que la page contient une balise `<link>` vers lui.

3. Que signifie le code `200` ? Et le code `404` de la favicon ?

   > _Ma réponse :_ `200` veut dire "OK" : le serveur a trouvé le fichier et l'a envoyé. `404` veut dire "Not Found" : le fichier demandé n'existe pas sur le serveur.

4. Pourquoi les modifications faites dans l'onglet Éléments ne sont-elles pas visibles par les autres visiteurs ?

   > _Ma réponse :_ Elles modifient seulement la copie de la page chargée dans mon navigateur. Le fichier sur le serveur ne change pas : les autres visiteurs (ou moi après un rechargement) reçoivent toujours la page d'origine.

---

## 🟣 Exercice 7 — Envoyer des informations dans l'URL

1. Dans l'URL `https://www.youtube.com/results?search_query=chat`, quel est le nom du paramètre ? Quelle est sa valeur ?

   > _Ma réponse :_ 

2. Pourquoi le serveur plante-t-il avec `a=bonjour` ? Que faudrait-il faire pour l'éviter ?

   > _Ma réponse :_ 

3. Pourquoi est-il dangereux d'afficher **tel quel** ce que l'utilisateur envoie ?

   > _Ma réponse :_ 

---

## 🟣 Exercice 8 — Les formulaires

1. Quelle est la différence visible entre GET et POST ?

   > _Ma réponse :_ 

2. Pour un formulaire de **recherche**, quelle méthode choisiriez-vous ? Et pour un formulaire de **connexion avec mot de passe** ? Pourquoi ?

   > _Ma réponse :_ 

3. Les données envoyées en POST sont-elles vraiment « secrètes » ? (Pensez à ce que vous avez vu dans l'onglet Réseau.)

   > _Ma réponse :_ 

---

## 🔴 Exercice 9 — Les codes de statut

1. Quelle est la différence entre une erreur `4xx` et une erreur `5xx` ? Qui est « fautif » dans chaque cas ?

   > _Ma réponse :_ Une erreur `4xx` est une erreur du client : la demande est mauvaise, par exemple une page qui n'existe pas (404) ou un accès interdit (403, comme sur `/secret`). Une erreur `5xx` est une erreur du serveur : la demande était correcte mais le code a planté, comme le 500 que j'ai eu quand `request` n'était pas importé ou avec `int("bonjour")`.

2. Comment fonctionne une redirection ? Qui fait la deuxième requête : le serveur ou le navigateur ?

   > _Ma réponse :_ Le serveur répond avec un code `302` et un en-tête `Location` qui indique la nouvelle adresse (ici `/`). C'est le navigateur qui fait ensuite automatiquement une deuxième requête vers cette adresse. Dans l'onglet Réseau, on voit bien 2 requêtes pour `/home` : une en 302 puis une en 200.

3. Donnez un exemple de situation où un vrai site utilise une redirection.

   > _Ma réponse :_ Après une connexion réussie, le site redirige vers la page d'accueil ou le tableau de bord. Autres exemples : un site qui passe de `http://` à `https://`, ou une page qui a changé d'adresse.

---

## 🔴 Exercice 10 — Ce que le serveur sait de vous

1. Citez trois informations que le serveur connaît sur vous, sans que vous ayez rien rempli.

   > _Ma réponse :_ 

2. À quoi peut servir l'en-tête `Accept-Language` pour un site comme Wikipédia ?

   > _Ma réponse :_ 

3. Dans l'Access log, retrouvez une requête qui a reçu un code `404`. Quelle page était demandée ?

   > _Ma réponse :_ 

4. Après cet exercice, que pensez-vous de la notion de « navigation anonyme » ?

   > _Ma réponse :_ 

---

## 🔴 Exercice 11 — Le Web des machines : API et JSON

1. Quelle est la différence entre une page HTML et une réponse JSON ? À qui chacune est-elle destinée ?

   > _Ma réponse :_ Le HTML est une page mise en forme pour un humain. Le JSON contient des données brutes pour un programme.

2. Dans la page `/horloge`, quel code s'exécute sur le **serveur** et quel code s'exécute dans le **navigateur** ?

   > _Ma réponse :_ Serveur : le Python (routes `/horloge` et `/api/heure`). Navigateur : le JavaScript du `<script>`, qui appelle l'API chaque seconde.

3. Citez une application de votre téléphone qui, selon vous, utilise une API. Quelles données échange-t-elle ?

   > _Ma réponse :_ L'appli Météo : elle envoie ma ville et reçoit la température et les prévisions.

---

## 🏁 Pour conclure

En quelques phrases, expliquez à un ami ce qui se passe entre le moment où il tape une adresse dans son navigateur et celui où la page s'affiche :

> _Ma réponse :_ Le navigateur trouve le serveur grâce au nom de domaine et lui envoie une requête HTTP pour le chemin demandé. Le serveur exécute son code, prépare la page HTML et la renvoie avec un code de statut (200, 404…). Le navigateur télécharge ensuite le CSS et les images, puis affiche la page.
