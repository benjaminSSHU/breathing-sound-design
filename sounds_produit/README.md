# Sons "produit" · Fitness Check · Breathing

Version sonore enrichie (marimba / cloche harmonisées + réverbération), identique
à ce que tu as entendu dans la page de comparaison.

## Fichiers

| Fichier | Durée | Note | Usage |
|---|---|---|---|
| `countdown.wav` | ~1.0 s | marimba La5 | joué 3× sur les 3 dernières sec du repos |
| `go.wav` | ~1.4 s | cloche Sol4 | transition repos → expiration |
| `hold.wav` | ~1.1 s | marimba Mi6 (octave) | transition expiration → rétention |
| `success.wav` | ~1.4 s | arpège Do-Mi-Sol | fin du test |

Mono, 44.1 kHz, 16-bit. Normalisés à 0.85 (pas de saturation).

## Intégration (Expo)

Aucun changement de code : ces fichiers remplacent directement les bips utilitaires.

1. Copie les 4 `.wav` dans `assets/sounds/` (écrase les anciens, mêmes noms).
2. C'est tout · le hook `useFitnessTestSound` les recharge au montage.

Les sons sont joués en asynchrone : leur durée (jusqu'à 1.4 s) ne bloque pas la
logique du test. Le `hold` se joue pendant que le chrono d'apnée démarre · voulu.

## Point d'attention : le countdown

Le countdown dure ~1 s mais tu le rejoues toutes les 1 s. La queue de reverb
(~0.5 s) déborde donc légèrement sur le bip suivant → effet de résonance continue,
plutôt agréable. Si tu préfères des bips bien détachés :
- soit espace les bips de 1.2 s au lieu de 1 s,
- soit demande une version "countdown sèche" (sans reverb).

## Remplacer / ajuster

Les sons sont synthétisés (pas de licence). Pour les régénérer ou ajuster
(volume, gamme, durées), le script de synthèse est reproductible · demande la
version Python si tu veux itérer toi-même.
