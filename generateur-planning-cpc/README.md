# Générateur de planning CPC

Génère le visuel "La semaine du club" sans Canva, directement depuis le navigateur.

---

## Utilisation (chaque semaine)

1. Ouvre `index.html` dans Chrome (double-clic sur le fichier)
2. Remplis les jours dans le formulaire à gauche :
   - Coche "Repos" pour les jours sans intervention
   - Sinon remplis : heure, titre, intervenant(e), note (optionnel)
3. Clique **Générer le planning** pour voir l'aperçu
4. Screenshot le visuel (voir ci-dessous)

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

## Modifier les valeurs par défaut

Les valeurs pré-remplies chaque semaine sont dans le fichier `index.html`, variable `DEFAULTS` (ligne ~90).

Exemple : si le lundi est toujours "Call de bienvenue avec KIKI à 20h", ça reste pré-rempli. Tu n'as qu'à modifier ce qui change.

---

## Dimensions du visuel généré

- 1080 × 1500 px (portrait Instagram)
- Fond : #0A0A0A
- Accent : #5CD6AD
- Polices : Bebas Neue + Inter (chargées depuis Google Fonts, internet requis)
