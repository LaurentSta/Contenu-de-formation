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


# 02_ScenarioConnexion.md

## 1. Objectifs
- Comprendre le trajet physique et géographique d'une information sur le réseau.
- Dédramatiser la notion de distance : assimiler que l'éloignement géographique n'implique pas nécessairement une lenteur d'accès.
- Comprendre le rôle d'un serveur relais (Réseau de distribution de contenu) et consolider la définition d'un serveur classique.

## 2. Contexte
- **Public :** Apprenants en inclusion numérique.
- **Matériel :** Vidéoprojecteur, tableau blanc, chronomètre physique (ou application sur téléphone).
- **Stratégie d'animation :** Les commandes techniques (`ping`, `tracert`) sont strictement réservées à l'usage du formateur pour la démonstration visuelle. Ne pas demander aux apprenants de reproduire ces lignes de commande.

## 3. Méthode
- Pédagogie narrative (Storytelling) : utilisation d'un personnage fictif ("Louise") pour ancrer la théorie dans le quotidien.
- Démonstration visuelle par le formateur pour prouver la vitesse du réseau.
- Simplification sémantique : le terme "CDN" (Content Delivery Network) est remplacé par le concept de "Serveur relais" ou "Serveur copie".

## 4. Déroulé (Durée estimée : 45 minutes)

| Phase | Durée | Action du formateur | Action de l'apprenant |
| :--- | :--- | :--- | :--- |
| Inclusion | 5 min | Lancer un défi : « À votre avis, combien de temps met une page web pour traverser l'océan Atlantique ? » | Formuler des estimations de temps. |
| Conceptualisation | 15 min | Raconter l'histoire de Louise au tableau. Dessiner les étapes (Ordinateur > Box > Câble sous-marin > Centre de données). | Écouter et visualiser les étapes du trajet physique. |
| Démonstration | 15 min | Ouvrir un site américain. Chronométrer le temps d'affichage. Lancer une commande de diagnostic (`tracert` ou `ping`) au vidéoprojecteur pour montrer les "sauts" entre les routeurs. | Observer la vitesse d'exécution et le parcours de la requête. |
| Synthèse | 10 min | Expliquer le principe du serveur relais (la "copie" stockée plus près). Distribuer la fiche récapitulative. | Ranger le support et poser les dernières questions. |

## 5. Évaluation
- **Formative :** Demander à un apprenant de venir au tableau pour replacer les étapes du voyage dans l'ordre (Box, Réseau, Câble, Serveur).
- **Sommative :** Capacité individuelle à expliquer pourquoi un site américain s'affiche aussi vite qu'un site français.

## 6. Contenus clés (Matière pour le formateur et les supports)

### Le scénario narratif : Le voyage de la donnée
- Louise, située en France, ouvre un site d'information hébergé aux États-Unis.
- Son navigateur envoie une requête qui traverse successivement sa box internet, le réseau national de son opérateur, puis les câbles sous-marins de l'océan Atlantique.
- La requête arrive au centre de données (Data center) du site américain.
- Le serveur trouve la page demandée et renvoie les éléments (textes, images) par le même chemin en une fraction de seconde.

### La gestion de la distance (Les serveurs relais / CDN)
- **Principe :** La distance géographique n'est pas synonyme de lenteur grâce aux câbles à très haut débit.
- **Le système de copie :** Pour accélérer encore l'affichage, les sites très visités utilisent des Réseaux de Distribution de Contenu (CDN). Ce sont des "serveurs relais" qui stockent une copie des fichiers (images, vidéos) au plus près de l'utilisateur (par exemple, à Francfort ou Paris).
- **Sécurité :** Si le serveur américain d'origine tombe en panne, le site devient indisponible, d'où la nécessité pour les sites d'avoir des serveurs de secours (redondance).

### Rappel : Qu'est-ce qu'un serveur ?
- Il s'agit d'un ordinateur spécialisé, fonctionnant sans écran, conçu pour répondre aux requêtes de manière ininterrompue (24h/24 et 7j/7).
- Ces machines sont stockées dans des centres de données hautement sécurisés et climatisés.
- Leur rôle est d'héberger des fichiers et de les renvoyer dès qu'un navigateur les demande.