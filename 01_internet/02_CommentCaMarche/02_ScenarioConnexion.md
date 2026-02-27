# 07 – Scénario : se connecter à un site à l’étranger

Story courte
- Louise est en France et ouvre un site d’info situé aux États‑Unis.
- Son navigateur envoie une requête qui traverse sa box, le réseau de son FAI, puis des câbles sous-marins jusqu’au data center du site.
- Le serveur du site reçoit la requête, trouve la page demandée et renvoie la réponse par le même chemin (souvent via un CDN pour aller plus vite).

Messages clés
- Distance ≠ lenteur absolue : des câbles dédiés relient les continents à très haut débit.
- Souvent, le contenu est dupliqué dans un CDN « proche » (ex. Francfort), donc la réponse peut venir d’un serveur plus près.
- Si le serveur d’origine tombe, le site est indisponible : d’où l’importance des serveurs redondants.

Petit focus : qu’est-ce qu’un CDN ?
- CDN = Content Delivery Network : un réseau de serveurs « copies » répartis géographiquement.
- Il stocke les fichiers statiques (images, vidéos, pages mises en cache) pour les livrer depuis un serveur proche de l’utilisateur.
- Résultat : chargement plus rapide et moins de trafic jusqu’au serveur d’origine.

Démo simple
- Ouvrir un site étranger (ex. un média US) et afficher le temps de chargement.
- Lancer `tracert` ou `ping` pour montrer quelques sauts intermédiaires (sans entrer dans les détails).

Qu’est-ce qu’un serveur ? (rappel)
- C’est un ordinateur spécialisé, sans écran, conçu pour répondre à des requêtes en continu (24/7), souvent dans un data center climatisé et sécurisé.
- Il héberge des fichiers (pages, images, vidéos) et des bases de données, et renvoie ce qu’on lui demande.
