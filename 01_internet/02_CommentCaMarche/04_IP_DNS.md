# 03 – Adresse IP et DNS

Images simples
- IP = plaque d’immatriculation pour que les machines se trouvent (ex. 192.168.1.12).
- DNS = annuaire qui traduit un nom facile (service-public.fr) en adresse IP chiffrée.

Messages clés
- Chaque appareil connecté a une adresse.
- On retient des noms, le réseau parle en numéros : le DNS traduit.

Mini-démos
- `ping service-public.fr` : on voit l’adresse IP apparaître.
- `nslookup google.fr` : on lit la traduction nom → IP.

Idée d’animation
- Jeu « devine » : affichez un nom de site, faites deviner s’il est français (.fr), international (.com), associatif (.org).


# 04_IP_DNS.md

## 1. Objectifs
- Comprendre le rôle d'une adresse IP comme identifiant unique d'une machine sur le réseau.
- Assimiler la fonction du DNS (Système de Noms de Domaine) en tant que traducteur entre le langage humain et le langage machine.
- Identifier la signification des principales extensions de noms de domaine (exemples : .fr, .com, .org).

## 2. Contexte
- **Public :** Apprenants en inclusion numérique.
- **Matériel :** Vidéoprojecteur, tableau blanc, étiquettes imprimées (via Word) pour le jeu des extensions.
- **Stratégie d'animation :** Les commandes techniques (`ping`, `nslookup`) sont utilisées exclusivement par le formateur sur le vidéoprojecteur. Elles servent à prouver visuellement l'existence des chiffres derrière les mots, sans exiger de manipulation terminale de la part des apprenants.

## 3. Méthode
- Pédagogie analogique (utilisation des concepts de la plaque d'immatriculation et du répertoire téléphonique).
- Démonstration visuelle en direct pour matérialiser un processus invisible.
- Apprentissage actif via un jeu de déduction participatif.

## 4. Déroulé (Durée estimée : 1h00)

| Phase | Durée | Action du formateur | Action de l'apprenant |
| :--- | :--- | :--- | :--- |
| Inclusion | 10 min | Poser une question introductive : « Comment faites-vous pour appeler un proche dont vous ne connaissez pas le numéro par cœur ? » (Réponse attendue : le répertoire du téléphone). | Répondre et faire le lien avec la mémorisation des noms plutôt que des chiffres. |
| Conceptualisation | 15 min | Définir l'adresse IP (la plaque d'immatriculation) et le DNS (l'annuaire ou le répertoire). Expliquer que le réseau ne lit que des numéros. | Écouter et noter les deux analogies sur un brouillon. |
| Démonstration | 10 min | Ouvrir l'invite de commande au vidéoprojecteur. Lancer `ping service-public.fr` pour afficher l'IP. Lancer `nslookup google.fr` pour montrer la traduction directe nom vers IP. | Observer l'apparition des adresses chiffrées cachées derrière les noms de sites familiers. |
| Pratique (Jeu) | 15 min | Animer le jeu « Devine l'extension ». Afficher des noms de sites au tableau et faire deviner la nature du site selon sa fin (.fr, .com, .org). | Déduire la provenance ou le type de site (français, commercial, associatif). |
| Synthèse | 10 min | Distribuer la fiche mémo récapitulant les définitions simplifiées et les principales extensions. | Ranger le document et valider sa compréhension. |

## 5. Évaluation
- **Formative :** Taux de bonnes réponses lors du jeu de déduction sur les extensions de domaine.
- **Sommative :** Capacité individuelle à associer correctement les acronymes « IP » et « DNS » à leurs analogies physiques (Immatriculation et Annuaire/Répertoire).

## 6. Contenus clés (Matière pour le formateur et les supports)

### L'adresse IP (Internet Protocol)
- **Définition :** C'est la plaque d'immatriculation de chaque appareil connecté au réseau (ordinateur, téléphone, serveur).
- **Format :** Elle se présente sous forme de séries de chiffres (exemple : 192.168.1.12). Pour communiquer, les machines ont obligatoirement besoin de se cibler via ces numéros.

### Le DNS (Le traducteur)
- **Le problème :** L'être humain a de la difficulté à mémoriser des suites de chiffres complexes. Il retient beaucoup plus facilement des mots (comme « service-public.fr »).
- **La solution :** Le DNS agit comme un immense annuaire automatique. Lorsque l'utilisateur tape un nom, le DNS cherche à quelle adresse IP exacte (les chiffres) ce nom correspond, et dirige l'appareil vers la bonne destination.

### Les extensions de domaine à connaître
- **.fr :** Indique généralement un site rattaché à la France (ou une entreprise ciblant le marché français).
- **.com :** À l'origine pour "commercial", c'est aujourd'hui l'extension internationale la plus courante.
- **.org :** Réservé historiquement aux organisations, souvent utilisé par les associations à but non lucratif (ex: wikipedia.org).
- **.gouv.fr :** Extension strictement réservée aux sites gouvernementaux et officiels français (gage de sécurité).