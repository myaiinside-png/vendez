# De gré à gré

**Un guide libre et gratuit pour vendre son bien immobilier entre particuliers, de la décision jusqu'au notaire — sans agence.**

Une seule page web, aucun serveur, aucune donnée collectée. L'outil vous accompagne à chaque étape : identifier le bien, réunir les diagnostics et les pièces obligatoires, rédiger une annonce conforme, qualifier les acheteurs, formaliser l'offre, puis transmettre un dossier complet à l'étude notariale.

> *« De gré à gré »* est le terme juridique de la vente directe, sans intermédiaire, par accord mutuel entre vendeur et acheteur.

---

## Ce que fait l'outil

Il déroule les six étapes de la vente :

1. **Bien & diagnostics** — localisation via la Base Adresse Nationale, puis liste légale des diagnostics calculée automatiquement selon les caractéristiques du bien (année de construction, gaz, électricité, copropriété, zone termites, assainissement, classe DPE).
2. **Dossier juridique** — les pièces de propriété à réunir, avec la liste copropriété (loi ALUR) le cas échéant.
3. **Annonce** — génération d'un texte prêt à copier, mentions légales DPE et risques incluses.
4. **Visiteurs** — grille de qualification des acheteurs.
5. **Offre d'achat** — saisie et vérification de la solvabilité (apport + prêt vs. prix).
6. **Notaire** — checklist des pièces à transmettre et rappels post-signature.

L'audit énergétique réglementaire s'ajoute automatiquement pour une maison classée E, F ou G.

## Vie privée

**Aucune donnée n'est envoyée nulle part.** Le dossier est enregistré localement dans le navigateur (`localStorage`). La fonction d'export `.json` sert uniquement à transférer son dossier d'un appareil à un autre. Le seul appel réseau est la recherche d'adresse, adressée au service public [adresse.data.gouv.fr](https://adresse.data.gouv.fr).

## Déploiement

C'est un fichier statique : il n'a besoin d'aucun serveur.

**En local** — ouvrez simplement `index.html` dans un navigateur.

**En ligne, gratuitement, via GitHub Pages :**

1. Créez un dépôt et déposez `index.html` à la racine.
2. Dans **Settings → Pages**, choisissez la branche `main` et le dossier `/ (root)`.
3. L'URL publique est générée en une minute.

Tout autre hébergement de fichiers statiques (Netlify, Cloudflare Pages, un simple dossier sur un serveur) fonctionne aussi.

## Personnalisation

Tout est dans `index.html`, sans étape de compilation :

- **Nom et textes** : modifiez l'en-tête (`<header class="top">`) et le `<title>`.
- **Couleurs et polices** : variables CSS regroupées en haut du fichier (`:root`).
- **Listes de documents, de diagnostics, de qualification** : constantes JavaScript en début de script (`DOCS_GENERAL`, `NOTAIRE`, etc.).

## Limites & avertissement

Cet outil **informe et organise ; il ne donne pas de conseil juridique** et ne remplace pas le notaire, seul compétent pour rédiger l'avant-contrat. Par conception, il ne rédige pas le compromis : il vous renvoie à l'étude, ce qui est la bonne pratique et n'entraîne aucun surcoût.

Les obligations légales évoluent (diagnostics, seuils de l'audit énergétique, délais). Vérifiez les points sensibles auprès de votre notaire ou des services publics avant toute décision.

## Licence

Distribué sous licence **GNU AGPL-3.0** (voir [`LICENSE`](LICENSE)). Vous pouvez l'utiliser, le modifier et le redéployer librement, à condition d'en garder le code source ouvert — y compris lorsqu'il est mis à disposition en ligne.

> Si vous préférez favoriser la réutilisation la plus large possible, quitte à autoriser des dérivés fermés, une licence permissive comme MIT est l'alternative. Remplacez alors le fichier `LICENSE` et cette section.

## Contribuer

Les remontées de bugs, corrections d'obligations légales et propositions d'amélioration sont bienvenues via les *issues* et les *pull requests*.
