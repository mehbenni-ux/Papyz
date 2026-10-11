# Papyz : mémo du projet

Lu automatiquement au début de chaque conversation. À tenir à jour quand une décision importante est prise.

## L'app
- **Papyz** (toujours écrit ainsi) : app gratuite, en français, qui aide les personnes étrangères en France à obtenir leurs papiers (titre de séjour, puis éventuellement nationalité).
- Elle centralise les informations, propose un parcours personnalisé étape par étape, une liste de pièces à fournir et des rappels de dates (fin de titre, renouvellement, rendez-vous).
- Public de départ : étudiants étrangers, et jeunes diplômés qui ont commencé à travailler. Aussi les conjoints de Français.
- 100 % gratuite : jamais d'abonnement ni d'option payante.
- Dépôt GitHub : `mehbenni-ux/papyz` (privé). Sans lien avec Furnilog : ne jamais toucher au dépôt de Furnilog depuis ce projet.

## Règles de prudence (essentielles)
- Infos uniquement tirées de sources officielles : service-public.fr, ANEF (administration-etrangers-en-france.interieur.gouv.fr), Légifrance, sites des préfectures. Toujours indiquer la source et la date de vérification. Rien d'inventé.
- Les règles changent souvent (loi immigration 2024, exigences de langue et d'examen civique depuis janv. 2026) : vérifier avant d'affirmer.
- Pas de conseil juridique personnalisé : pour un cas compliqué, orienter vers une association (La Cimade, etc.) ou un avocat.
- Ne jamais ressembler à un service de l'État : pas de Marianne, pas de drapeau, pas le design officiel de l'État (DSFR), pas de nom en « Ma… / Mon… ». Mention claire : « app indépendante, non officielle ».
- Données très sensibles (situation de séjour) : garder au maximum sur le téléphone, sans compte au départ.

## Comment travailler avec le fondateur
- Il tutoie, l'app tutoie aussi. Il écrit souvent depuis son téléphone, parfois par dictée vocale (attention aux mots mal transcrits, demander en cas de doute).
- Réponses courtes, en français simple, sans jargon technique.
- Pour chaque changement : branche de travail, PR, lien de prévisualisation à essayer sur téléphone, puis « Je fusionne ? » ; fusionner seulement après « Oui fusionne ».
- Toujours prévenir de l'impact d'un changement avant de fusionner.
- Ne jamais formuler un texte comme un ordre donné à l'utilisateur : c'est l'app qui agit (« On te prévient avant la fin de ton titre »).
- L'app doit rester simple, y compris sur iPhone.

## Design
- Toutes les règles de design et d'ergonomie sont dans `DESIGN.md` (reprises de Furnilog), avec la palette bleue de Papyz. Les lire avant de toucher à l'interface.
- Maquette des 4 écrans principaux : `maquette/maquette.html` (en ligne : https://claude.ai/artifact/8KXBb7RUoyNLTsJK5oAE2o).

## Langues
- Français d'abord. Ensuite : anglais, arabe (écriture de droite à gauche), espagnol…

## Prochaines étapes
1. Valider la maquette avec le fondateur.
2. Code de l'app (PWA installable), puis mise en ligne (Vercel).
- À vérifier : disponibilité de papyz.app / .fr / .com, comptes réseaux, marque (INPI, EUIPO).
