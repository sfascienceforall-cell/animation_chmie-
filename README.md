# Animations SFA

Site statique : les animations de cours de la prépa médecine, par matière.

- **Chimie** — 17 capsules, 68 animations (ARES version 10)
- **Mathématiques** — 20 capsules, 83 animations (ARES version 8)
- **Physique** — 20 capsules, 80 animations (ARES version 8)
- **Biologie** — 19 capsules, 76 animations (ARES version 8)

## Publier sur GitHub Pages

```bash
git init
git add .
git commit -m "Animations SFA"
git branch -M main
git remote add origin git@github.com:<compte>/<depot>.git
git push -u origin main
```

Puis dans le dépôt : **Settings → Pages → Source : Deploy from a branch**,
branche `main`, dossier `/ (root)`. Le site est en ligne sous une minute à
l'adresse `https://<compte>.github.io/<depot>/`.

Le fichier `.nojekyll` est nécessaire : il demande à GitHub Pages de servir les
fichiers tels quels, sans passer par Jekyll.

## Structure

```
index.html             accueil, les 4 matières
chimie/index.html      sommaire + les 17 capsules
maths/index.html       sommaire + les 20 capsules
physique/index.html    sommaire + les 20 capsules
biologie/index.html    sommaire + les 19 capsules
```

Chaque capsule est un fichier HTML autonome : aucune dépendance, aucun script
externe hormis la police Google Fonts. Elle fonctionne aussi hors ligne, en
ouvrant le fichier directement.

## Avant une diffusion publique

Le logo SFA est encore un placeholder typographique dans chaque capsule,
marqué `REMPLACER PAR LE VRAI LOGO`. Le remplacement se fait dans le gabarit
`shell_anim.html` du dépôt de code, puis on reconstruit.
