# Générateur de changement de prix — VMMX

Ce dossier contient tout ce qu'il faut pour héberger l'outil sur GitHub Pages ou Cloudflare Pages.

## Contenu

- `index.html` — l'application complète (autonome, aucune autre dépendance de fichier).
- `.nojekyll` — fichier vide qui indique à GitHub Pages de ne pas traiter le site avec Jekyll (recommandé, évite tout comportement inattendu).

## Déploiement avec GitHub Desktop

1. Copie tout le contenu de ce dossier (`index.html` et `.nojekyll`) dans ton dépôt local GitHub Desktop.
   - Pour héberger à la racine du site : mets les fichiers directement à la racine du dépôt.
   - Pour respecter le schéma `js/[outil]/index.html` de ton site actuel : crée un sous-dossier `js/vmmx/` et mets-y les fichiers.
2. Commit, puis Push dans GitHub Desktop.
3. Sur GitHub.com : Settings → Pages → choisis la branche et le dossier à publier.
4. GitHub fournit une URL en `https://` automatiquement (aucune configuration supplémentaire requise).

## Déploiement avec Cloudflare Pages

1. Connecte le dépôt GitHub à Cloudflare Pages.
2. Choisis le préréglage "No framework" (site 100% statique, aucune commande de build).
3. Pointe vers le dossier contenant `index.html`.

## Notes

- L'application tourne entièrement dans le navigateur : aucun fichier n'est envoyé sur un serveur.
- Les 3 seules dépendances externes sont chargées depuis cdnjs.cloudflare.com (pdf.js et ExcelJS), en HTTPS, versions figées.
- La liste des fournisseurs éditable est sauvegardée dans le navigateur de chaque utilisateur (pas partagée entre gérants).
