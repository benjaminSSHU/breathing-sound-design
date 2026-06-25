# Fitness Check · Breathing — Design sonore des transitions

Démo et ressources pour les repères sonores du test de respiration de l'app.

Chaque transition du test (repos → expiration → rétention → fin) est accompagnée
d'un son court qui **double** le visuel, pour que l'utilisateur puisse garder les
yeux fermés pendant l'apnée.

## 🔊 Démo en ligne

La page [`index.html`](./index.html) compare deux directions sonores :

- **Utilitaire** — bips simples (sinus), neutres et fonctionnels
- **Produit** — sons harmonisés (marimba, cloche) avec timbre riche et réverbération

Les sons sont synthétisés en direct dans le navigateur (Web Audio API) : aucun
fichier externe, la page est autonome. Idéal pour [GitHub Pages](#publier-sur-github-pages).

## 📁 Contenu

| Fichier / dossier | Description |
|---|---|
| `index.html` | Page de comparaison interactive (screens + player audio + tableau des transitions) |
| `sounds_produit/` | Les 4 fichiers `.wav` version « produit », prêts à intégrer dans l'app |
| `STEP1/2/3_*.png` | Captures des écrans du test |

## 🎵 Les 4 repères sonores

| Cue | Moment | Version produit |
|---|---|---|
| `countdown` | 3 dernières sec du repos (×3) | marimba La5 |
| `go` | repos → expiration | marimba Mi6 (octave) |
| `hold` | expiration → rétention | cloche Sol4 |
| `success` | fin du test | arpège Do-Mi-Sol |

Voir [`sounds_produit/README.md`](./sounds_produit/README.md) pour l'intégration Expo.

## 🚀 Publier sur GitHub Pages

1. Pousser ce repo sur GitHub (voir commandes ci-dessous).
2. Repo → **Settings** → **Pages**.
3. Source : branche `main`, dossier `/ (root)`.
4. La page sera servie à `https://<user>.github.io/<repo>/`.
