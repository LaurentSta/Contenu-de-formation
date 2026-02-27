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
