# Règles de design

Ce mémo regroupe les choix de design et d'ergonomie de Papyz. Les règles générales viennent de Furnilog (même fondateur), où chacune est née d'un vrai retour. On en ajoute une à chaque nouvelle décision.

## Identité visuelle (propre à Papyz)
- **Bleu, sérieux et rassurant**, avec un côté « national » sans jamais imiter l'État :
  - pas de Marianne, pas de drapeau, pas de bleu-blanc-rouge ;
  - pas le système de design de l'État (DSFR), réservé aux sites officiels ;
  - mention visible « app non officielle ».
- Couleurs (variables CSS, clair / sombre) :
  - `--nav` bleu nuit profond `#12224A` : barre du bas ;
  - `--ink` bleu nuit `#0F1E3A` : textes et titres ;
  - `--accent` bleu vif `#1F4FBF` : boutons, éléments actifs ;
  - `--soft` bleu très clair `#E4ECF8` : fonds de cartes, pastilles ;
  - `--paper` blanc bleuté `#F2F5FA` : fond ;
  - `--alert` rouge discret `#C3344A` : **seulement** pour les alertes (titre qui expire) ;
  - `--done` vert `#2E8158` : étape validée.
  - Thème sombre : voir `maquette/maquette.html`.
- Polices : Poppins (titres) et Inter (texte).
- Logo provisoire : une fiche bleue arrondie avec une coche.

## Principes généraux
- **Simple d'abord, surtout sur iPhone.** Un geste de plus ou une question de plus doit se justifier.
- **L'app agit, elle ne donne pas d'ordres.** « On te prévient avant la fin de ton titre », jamais « Préviens-moi » ni « Active… ».
- **Tutoiement, français simple, sans jargon administratif.** Un sigle (ANEF, OFII…) est toujours expliqué la première fois.
- **Les explications passent par des bulles ponctuelles** (tutoriel, première visite), jamais par un texte fixe ajouté à l'écran.
- **Rassurer, ne jamais affoler.** Une échéance proche s'affiche clairement, avec ce qu'il faut faire, sans dramatiser.
- **Chaque info dit d'où elle vient** (source officielle) et quand elle a été vérifiée.
- **Gestes du téléphone d'abord** (glisser, appui long), comme dans les apps natives. Les boutons servent de secours sur ordinateur.

## Navigation
- **Un appui sur un onglet du bas ramène toujours à l'accueil de cet onglet**, même quand on y est déjà : on sort des sous-pages, la recherche est effacée, la page remonte en haut.
- **Le bouton Retour ramène toujours à ce qu'on voyait juste avant**, jamais à un écran arbitraire. Dans l'ordre :
  1. il referme la fenêtre ouverte ;
  2. il quitte la sous-page ;
  3. il efface la recherche en cours ;
  4. il revient à l'écran précédent, à la même position dans la page.
  - On ne quitte l'app que depuis le premier écran.
- **Le retour à l'accueil d'un onglet est animé** : la page remonte en douceur. Jamais de saut brusque.
- **Un rechargement dans la même session n'est pas une nouvelle ouverture** : pas de tutoriel ni d'écran d'accueil à nouveau.
- **Un bouton principal qui mène à plusieurs chemins propose un choix court** dans une petite fenêtre.

## Quitter l'app vers un site externe (ANEF, service-public…)
- **Jamais de départ brusque.** Une petite fenêtre « Direction [site] », avec « C'est parti » ou « Rester ici ».
  - Exception : un bouton qui dit déjà clairement où il mène (« Ouvrir le site de l'ANEF ») ouvre directement.
- **Revenir du site ramène exactement où on était.**

## Menus (trois petits points)
- **Un menu s'affiche toujours en entier** : il flotte au-dessus de la page, s'ouvre sous le bouton s'il y a la place, sinon au-dessus, sans passer sous la barre du bas.

## Fenêtres
- **Pendant qu'une fenêtre est ouverte, la page derrière ne défile pas.**
- **Glisser vers le bas pour fermer** une fenêtre du bas, comme dans les apps natives.

## Mode sombre
- **L'app a un vrai thème sombre**, défini par des variables de couleur (clair et sombre).
- **Certains navigateurs assombrissent eux-mêmes les sites** (Samsung Internet, Chrome « Assombrir les sites ») : les détecter et passer sur notre thème sombre (méthode de Furnilog : couleur système `canvas`, paramètre `?night=1` transmis par l'app Android).
- **Toujours vérifier les deux thèmes**, et le mode « assombrissement forcé » (Chromium avec `--enable-features=WebContentsForceDark`).
- Le rouge d'alerte et le vert « validé » restent lisibles dans les deux thèmes.

## Données personnelles
- La situation de séjour est une donnée sensible : gardée sur le téléphone tant que possible, sans compte au départ.
- Jamais de photo de document envoyée sur un serveur sans le dire clairement.

## Façon de travailler
- **Vérifier à l'écran chaque changement visible** (Playwright), en clair et en sombre, au format téléphone.
- **Reproduire un bug signalé sur un vrai téléphone avant de le corriger.**
- **Un lien de test par changement**, essayé sur téléphone avant de fusionner.
