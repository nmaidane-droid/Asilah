# Riad Le Bougainvillier — présentation

Présentation défilante du riad et de la ville d'Asilah, en sept langues.
Site statique : aucune dépendance, aucune étape de compilation.

## Contenu

```
index.html     écran de choix de la langue (aucune redirection automatique)
fr.html        Français
de.html        Deutsch
en.html        English
es.html        Español
nl.html        Nederlands
zh.html        中文（简体）
ja.html        日本語
photos/        27 images WebP, partagées par les sept langues
```

Chaque version compte 30 diapositives et pèse environ 40 Ko.

## Déploiement

**GitHub** — pousser ces fichiers **à la racine** du dépôt. S'ils sont dans un
sous-dossier, il faudra régler le *Root Directory* côté Vercel.

**Vercel** — « Add New… → Project », choisir le dépôt, laisser tous les réglages
par défaut. Le framework détecté doit rester « Other ». Aucune commande de build,
aucun dossier de sortie à renseigner.

Chaque `git push` redéploie automatiquement.

## Fonctionnement

- Défilement automatique. La durée se règle diapositive par diapositive via
  l'attribut `data-duree` (en millisecondes) sur chaque `<section class="dia">`.
- Commandes : flèches ← →, barre d'espace pour la pause, `F` pour le plein écran,
  glissement du doigt sur mobile. Le bouton portant le code de langue ramène à
  l'écran de choix.
- Les images se chargent au fil du défilement : les trois premières diapositives
  d'abord, le reste en arrière-plan.
- Une image absente n'interrompt rien : un cadre gris prend sa place.

## Polices

Le français, l'anglais, l'espagnol et le néerlandais utilisent Marcellus et Jost.
Le chinois et le japonais basculent sur Noto Serif / Noto Sans SC et JP : les
polices latines ne contiennent aucun idéogramme. Dans ces deux versions, les
capitales forcées et l'interlettrage sont neutralisés, et l'interligne est
augmenté — indispensable à la lisibilité des idéogrammes.

## À relire avant publication

Les versions **chinoise et japonaise** ont été adaptées plutôt que traduites
littéralement, le texte français étant très idiomatique. Une relecture par un
locuteur natif est recommandée avant tout usage commercial.

## Ajouter ou remplacer une photo

Déposer le fichier dans `photos/` au format WebP, en gardant le nom attendu par
l'attribut `data-photo` correspondant dans le HTML.

Photo manquante à ce jour : `photos/cuisine.webp` (cuisine et salle à manger).

## Modifier un texte

Les textes sont en clair dans chaque fichier de langue. Toute modification doit
être reportée dans les sept.

## Crédit

La toile du guerrab visible sur la fiche « L'entrée » est créditée `@Yassink_art`.
