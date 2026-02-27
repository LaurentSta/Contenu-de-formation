# 03 – Voyage de la donnée (client ↔ serveur) – version un peu plus technique

Image simple : la lettre, mais avec les étapes réseau.
- Client : vous tapez l’URL, vous écrivez la lettre.
- DNS : l’annuaire trouve l’adresse du destinataire.
- Réseau : fibre/wifi/4G sert de facteur qui transporte les paquets.
- Serveur : le destinataire lit la demande et prépare la réponse.

Étapes réelles (simplifiées)
1) Saisie de l’URL → le navigateur demande au DNS l’adresse IP du site.
2) Ouverture d’une connexion (TCP), puis chiffrement (TLS) si le site est en HTTPS.
3) Envoi d’une requête HTTP (ex. GET /page.html) du client vers le serveur.
4) Le serveur lit les fichiers ou la base de données et prépare la réponse.
5) La réponse revient en paquets ; si un CDN existe, elle peut partir d’un serveur plus proche.
6) Le navigateur reçoit les paquets et affiche la page (puis télécharge images, CSS, JS).

Messages clés
- Internet, ce sont des échanges de paquets entre ordinateurs.
- DNS dit « où aller » ; TCP/TLS ouvre un canal fiable et chiffré ; HTTP transporte le contenu.
- Un serveur reste allumé en continu et peut être dupliqué (CDN, redondance).

Mini-démo
- `nslookup` pour montrer l’étape DNS, puis ouvrir le site et observer le chargement.
- Variante : couper le wifi et relancer → la requête ne peut plus partir.

Idée d’animation
- Ligne du temps sur tableau : DNS → TCP/TLS → HTTP requête → traitement serveur → HTTP réponse → rendu navigateur.


# 03_VoyageDonnee.md

## 1. Objectifs
- Comprendre le principe d'échange d'informations (requête et réponse) entre un appareil local et un serveur distant.
- Associer les composants techniques invisibles (DNS, réseau, serveur) à une analogie familière (le service postal).
- Visualiser le concept d'adresse chiffrée (IP) qui se cache derrière le nom d'un site web.

## 2. Contexte
- **Public :** Apprenants en inclusion numérique.
- **Matériel :** Tableau blanc ou paperboard, marqueurs de couleurs différentes, vidéoprojecteur.
- **Stratégie d'animation :** Les acronymes techniques complexes (TCP, TLS, HTTP) génèrent une surcharge cognitive et doivent être exclus du discours destiné aux apprenants. Ils sont remplacés par la notion d'« enveloppe sécurisée ». La commande `nslookup` est strictement réservée au formateur pour une démonstration visuelle (l'effet "Matrix"), sans exiger de reproduction par le groupe.

## 3. Méthode
- Pédagogie analogique (fil rouge continu sur le courrier postal).
- Schématisation chronologique au tableau pour construire la compréhension étape par étape.
- Démonstration par la panne (coupure volontaire du réseau pour matérialiser la rupture du flux).

## 4. Déroulé (Durée estimée : 1h00)

| Phase | Durée | Action du formateur | Action de l'apprenant |
| :--- | :--- | :--- | :--- |
| Inclusion | 10 min | Rappeler l'analogie de la boîte aux lettres abordée au premier module. Poser la question : « Comment la lettre trouve-t-elle le bon destinataire dans le monde entier ? » | Formuler des hypothèses basées sur le système postal classique. |
| Conceptualisation | 20 min | Dessiner une ligne du temps au tableau : Expéditeur (Navigateur) → Annuaire (DNS) → Facteur (Réseau) → Destinataire (Serveur) → Réponse. | Observer la construction du schéma et copier les étapes sur un brouillon. |
| Démonstration | 15 min | Ouvrir un terminal au vidéoprojecteur. Taper la commande `nslookup` avec un site connu pour révéler l'adresse chiffrée. Variante : lancer le chargement d'une page et couper physiquement le Wi-Fi pour bloquer l'envoi de la « lettre ». | Visualiser les adresses IP cachées derrière les noms de sites. Constater l'échec de la connexion sans réseau. |
| Synthèse | 15 min | Distribuer une fiche mémo visuelle reprenant le schéma du tableau. Résumer les étapes avec le vocabulaire simplifié. | Ranger le document et poser les questions de clarification. |

## 5. Évaluation
- **Formative :** Demander au groupe de relier oralement les éléments techniques à l'analogie (ex. : « Qui est l'annuaire ? » → Le DNS).
- **Sommative :** Capacité individuelle à expliquer avec ses propres mots pourquoi un site web ne peut pas s'afficher si le Wi-Fi est désactivé (la requête ne part pas).

## 6. Contenus clés (Matière pour le formateur et les supports)

### L'analogie du réseau postal (À maîtriser par l'apprenant)
- **Le Client (Navigateur) :** Vous, en train de rédiger et d'envoyer la lettre avec votre demande.
- **Le DNS (L'annuaire) :** Le service qui traduit le nom de la personne (le nom du site) en une adresse postale exacte compréhensible par les machines.
- **Le Réseau (Fibre/Wi-Fi/4G) :** Le facteur et les camions qui transportent physiquement les paquets d'informations.
- **Le Serveur :** Le destinataire qui reçoit la lettre, la lit, trouve le document demandé, le met dans une enveloppe sécurisée et vous le renvoie.

### Les étapes techniques (Culture générale pour le formateur)
*À ne pas détailler sous cette forme aux apprenants grands débutants.*
1. Saisie de l'URL par l'utilisateur.
2. Interrogation du DNS pour obtenir l'adresse IP du serveur cible.
3. Établissement d'une connexion sécurisée (TCP/TLS) symbolisée par le cadenas (HTTPS).
4. Envoi de la requête (HTTP) vers le serveur.
5. Traitement par le serveur et renvoi de la réponse sous forme de paquets de données (parfois via un serveur relais/CDN pour accélérer le processus).
6. Réception des paquets, assemblage et affichage (rendu) par le navigateur.

### Les messages clés
- Internet fonctionne sur un principe de dialogue (une question posée, une réponse renvoyée).
- Les machines ne se comprennent qu'avec des numéros (Adresses IP) ; l'annuaire (DNS) est indispensable pour traduire les mots que nous tapons.
- Le serveur distant doit obligatoirement être allumé pour répondre à la demande.