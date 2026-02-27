# 05 – Navigateur : lire, contrôler, sécuriser

Périmètre de ce module
- Focus usage du navigateur : interface, onglets, téléchargements, paramètres simples.
- Pas de réseau bas niveau (vu dans IP/DNS) ni de rangement fichiers (vu dans Arborescence).

Image simple
- Le serveur envoie du texte (HTML/CSS/JS) ; le navigateur le traduit en page lisible.

Parcours en 6 mini-slides
1) Interface : barre d’adresse (URL + recherche), onglets, retour/avant, rafraîchir.
2) Confiance : repérer HTTPS + cadenas, vérifier le domaine avant de cliquer.
3) Lecture : zoom (Ctrl + +), mode lecture si dispo, traduction automatique.
4) Téléchargements : où vont les fichiers (dossier Téléchargements), ouvrir/afficher dans le dossier, se méfier des .exe inconnus.
5) Historique et traces : effacer historique récent, cookies basiques ; navigation privée = efface localement seulement.
6) Accessibilité rapide : taille de police, contraste clair/sombre, sous-titres YouTube.

Mini-démos possibles
- Clic droit → « Afficher le code source » : texte brut vs rendu.
- Désactiver brièvement le CSS (dev tools) pour voir la page sans styles.
- Télécharger un PDF et le retrouver dans Téléchargements.
- Effacer l’historique des 24 h et expliquer ce que cela change.

Messages clés
- Naviguer = lire l’URL, gérer onglets et téléchargements, vérifier le cadenas.
- La navigation privée n’est pas l’anonymat : le FAI et le site voient encore la visite.
- Zoom et traduction sont des aides d’accessibilité immédiates.

Idées d’animation
- Jeu « repère le vrai site » : deux barres d’adresse proches (service-public.fr vs service-public.fr.fake).
- Rallye express : retrouver un fichier téléchargé, activer le mode lecture, agrandir le texte.


# 05_Navigateur.md

## 1. Objectifs
- Maîtriser l'interface de base du navigateur (barre d'adresse, onglets, boutons d'actualisation).
- Gérer le téléchargement d'un fichier et savoir le retrouver sur l'ordinateur.
- Utiliser les options d'accessibilité (zoom, mode lecture, traduction) et comprendre les limites de la navigation privée.

## 2. Contexte
- **Public :** Apprenants en inclusion numérique.
- **Matériel :** Ordinateurs avec navigateur installé, vidéoprojecteur, fichiers PDF de test préparés.
- **Stratégie d'animation :** Le réseau de bas niveau et le rangement des fichiers ne sont pas abordés ici pour cibler exclusivement l'usage du logiciel. Les termes "HTML/CSS/JS" sont vulgarisés sous l'appellation "code informatique".

## 3. Méthode
- Pédagogie par la démystification (montrer "l'envers du décor" d'une page web).
- Apprentissage par l'action avec un "Rallye express" chronométré pour valider les manipulations.
- Pédagogie par l'erreur pour la sensibilisation à la sécurité (comparaison de barres d'adresse).

## 4. Déroulé (Durée estimée : 1h30)

| Phase | Durée | Action du formateur | Action de l'apprenant |
| :--- | :--- | :--- | :--- |
| Inclusion | 15 min | Expliquer le rôle du navigateur (le traducteur). Démonstration : faire un clic droit et "Afficher le code source" pour montrer ce que la machine reçoit réellement. | Observer la différence entre le texte brut (le code) et le rendu visuel de la page. |
| Conceptualisation | 20 min | Présenter l'interface : la barre d'adresse (recherche et URL), les onglets, les boutons Précédent/Suivant et Rafraîchir. | Manipuler son navigateur pour identifier chaque élément. |
| Pratique (Accessibilité et Fichiers) | 25 min | Guider l'utilisation du zoom (`Ctrl` + `+`), de la traduction et du mode lecture. Faire télécharger un fichier PDF de test. | Activer le zoom, télécharger le fichier et aller le chercher dans le dossier "Téléchargements". |
| Sensibilisation (Sécurité) | 15 min | Animer le jeu "Repère le vrai site" avec deux adresses projetées (ex: `service-public.fr` vs `service-public.fr.fake`). Expliquer l'effacement de l'historique et la navigation privée. | Identifier la fausse adresse. Effacer l'historique des dernières 24h sur son poste. |
| Synthèse | 15 min | Lancer le "Rallye express" : donner 3 consignes rapides (trouver un fichier, zoomer, activer le mode lecture). | Réaliser le défi en autonomie. |

## 5. Évaluation
- **Formative :** Validation des compétences visuelles lors du jeu "Repère le vrai site" (identification de l'extension exacte et du cadenas HTTPS).
- **Sommative :** Réussite autonome du "Rallye express", notamment la capacité à retrouver le fichier téléchargé sans l'aide du formateur.

## 6. Contenus clés (Matière pour le formateur et les supports)

### Le rôle du navigateur
- C'est un logiciel "traducteur". Le serveur lui envoie du texte brut de programmation, et le navigateur le traduit en une page visuelle, lisible et interactive.

### La sécurité et les traces
- **La confiance visuelle :** Toujours vérifier le cadenas (HTTPS) et lire attentivement le nom de domaine avant de cliquer ou d'entrer des données.
- **Les téléchargements :** Tous les fichiers vont par défaut dans le dossier "Téléchargements" de l'ordinateur. Il faut se méfier des fichiers inconnus, particulièrement ceux se terminant par `.exe` (logiciels exécutables).
- **La navigation privée :** Elle ne garantit pas l'anonymat. Le fournisseur d'accès à Internet et le site web visité voient toujours l'activité. Elle sert uniquement à ne pas laisser de traces (historique, cookies basiques) sur l'ordinateur localement utilisé.

### L'accessibilité immédiate
- Le navigateur possède des outils intégrés pour faciliter la lecture : l'agrandissement du texte (`Ctrl` + `+`), le contraste (clair/sombre), la traduction automatique des pages étrangères, et le mode lecture pour supprimer les distractions visuelles.