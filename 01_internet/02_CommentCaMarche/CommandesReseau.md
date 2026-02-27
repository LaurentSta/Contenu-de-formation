# Commandes réseau de base (Windows / macOS / Linux)

## Windows (Invite de commandes ou PowerShell)
`ping domaine.com` : tester si un site répond et mesurer la latence.  
`tracert domaine.com` : voir les étapes (sauts) traversées par une requête.  
`nslookup domaine.com` : connaître l’adresse IP renvoyée par le DNS.

## macOS / Linux (Terminal)
`ping domaine.com` : même usage.  
`traceroute domaine.com` : équivalent de tracert.  
`dig domaine.com` ou `nslookup domaine.com` : requêtes DNS.

## Astuces pédagogiques
Montrer qu’un site peut répondre mais lentement (ping OK mais temps élevé).  
Traceroute illustre le « voyage » : on voit passer par le FAI puis l’international.  
Comparer `nslookup google.fr` et `nslookup service-public.fr` pour voir des IP différentes et parfois des réponses CDN.
