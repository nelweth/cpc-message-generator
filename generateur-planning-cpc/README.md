# Générateur de planning CPC

Génère le visuel "La semaine du club" sans Canva, directement depuis le navigateur.

---

## Utilisation (chaque semaine)

1. Ouvre `index.html` dans Chrome (double-clic sur le fichier)
2. Les jours arrivent déjà pré-remplis avec le planning par défaut (voir plus bas)
3. Modifie ce qui change cette semaine :
   - Coche "Repos" pour les jours sans intervention
   - Sinon remplis : heure, titre, intervenant(e), note (optionnel)
   - Pour une masterclass habituelle, prends-la dans "Charger une intervention enregistrée"
4. Clique **Générer le planning** pour voir l'aperçu
5. Screenshot le visuel (voir ci-dessous)

---

## Exporter en image

### Option A — Screenshot manuel (aucune installation)

1. Génère le planning
2. Zoom Chrome à **100%** (Cmd+0)
3. **Cmd+Shift+4** sur Mac → sélectionne uniquement le visuel à droite
4. L'image est sauvegardée sur le bureau

### Option B — Téléchargement automatique en PNG

Nécessite d'ajouter html2canvas une seule fois :

1. Ouvre le fichier `index.html` dans un éditeur de texte
2. Ajoute cette ligne juste avant `</head>` :
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
```
3. Sauvegarde et recharge le fichier dans Chrome
4. Le bouton **Télécharger en PNG** fonctionne maintenant

---

## Le planning par défaut

Celui qui se charge à l'ouverture. Pour le changer, **plus besoin de toucher au code** :

1. Remplis les 7 jours comme tu veux qu'ils soient pré-remplis chaque semaine
2. Clique sur **Enregistrer comme planning par défaut**

C'est mémorisé dans le navigateur. À chaque ouverture, tu retrouves ce planning, et tu n'as plus qu'à modifier ce qui bouge dans la semaine.

**Recharger le planning par défaut** remet le formulaire dans cet état, si tu t'es emmêlée.

La variable `DEFAULTS` dans `index.html` ne sert plus que de filet, au tout premier lancement sur un navigateur où rien n'est encore enregistré.

---

## Les interventions enregistrées

Pour les masterclasses qui reviennent, et qu'on en a marre de réécrire.

- **Enregistrer** : remplis un jour (heure, titre, intervenant, note), puis clique sur **Enregistrer cette intervention** en bas du bloc du jour
- **Réutiliser** : sur n'importe quel jour, choisis-la dans **Charger une intervention enregistrée**. Les 4 champs se remplissent d'un coup
- **Supprimer** : la croix à droite de son nom, en haut du formulaire

Enregistrer une intervention qui porte un titre déjà pris remplace l'ancienne, après confirmation.

---

## ⚠️ Où tes enregistrements sont stockés

Dans le navigateur, sur cet ordinateur (localStorage). Donc :

- Un autre navigateur ou un autre ordi = une autre liste
- Vider les données de navigation efface les enregistrements
- La version ouverte en double-clic (`file://`) et la version en ligne (GitHub Pages) ont **chacune leur propre liste**. Choisis-en une et garde la même, sinon tu auras l'impression d'avoir tout perdu

Si le navigateur bloque le stockage, l'outil le dit par un message et continue de marcher : tu remplis juste tout à la main, comme avant.

---

## Dimensions du visuel généré

- 1080 × 1500 px (portrait Instagram)
- Fond : #0A0A0A
- Accent : #5CD6AD
- Polices : Bebas Neue + Inter (chargées depuis Google Fonts, internet requis)
