# Kit de lancement

*Document de travail — à garder pour toi, pas forcément à publier dans le dépôt.*

---

## 1. Réglages du dépôt (2 minutes)

Sur la page d'accueil du dépôt, clique sur la roue crantée « About » (à droite).

**Description** (à coller) :
> Guide libre et gratuit pour vendre son logement entre particuliers, de la décision au notaire. Sans agence, sans backend, sans collecte de données.

**Website** : l'URL Pages (`https://myaiinside-png.github.io/vendez/`).

**Topics** (à ajouter un par un) :
`immobilier` · `france` · `particulier-a-particulier` · `civic-tech` · `communs-numeriques` · `vanilla-javascript` · `static-site` · `github-pages` · `open-data` · `sans-tracking`

Les *topics* sont ce par quoi les gens filtrent GitHub : c'est gratuit et ça rend le dépôt trouvable.

---

## 2. Trois ou quatre « good first issues » à créer

Dans l'onglet **Issues → New issue**, colle chacune ci-dessous. Ajoute le label `good first issue` (crée-le si besoin, il est standard et très recherché par les contributeurs).

### Issue A — Imprimer sa checklist en une page
**Labels :** `good first issue`, `enhancement`
Beaucoup de vendeurs veulent une liste sur papier. Ajouter un bouton « Imprimer ma checklist » et une feuille de style `@media print` qui masque la navigation, les boutons et le sélecteur d'étapes, et met en page proprement les diagnostics requis et les documents cochés.
*Où :* section `<style>` (ajouter un bloc `@media print`) + un bouton dans le pied de page appelant `window.print()`.
*Critère d'acceptation :* depuis un mobile ou un ordinateur, l'aperçu d'impression donne une page lisible, sans l'interface.

### Issue B — Afficher les montants avec séparateur de milliers
**Labels :** `good first issue`
Les champs de prix affichent `255000`, peu lisible. Afficher `255 000` tout en gardant une valeur numérique exploitable dans l'état, sans casser la saisie (un champ `number` ne sait pas afficher d'espace — le passage à un champ texte avec analyse est la partie intéressante).
*Où :* les champs prix (étapes 3 et 5) et les gestionnaires `[data-field]` / `[data-offer]`.
*Critère :* on saisit un montant, il s'affiche au format français, et l'annonce comme l'analyse restent correctes.

### Issue C — Lien contextuel pour vérifier la zone termites
**Labels :** `good first issue`
La case « zone termites » demande une information que l'utilisateur n'a pas forcément. Ajouter à côté un petit lien vers Géorisques pour vérifier sa commune.
*Où :* le `<label class="check">` de `zone_termites`, à l'étape 1.
*Critère :* un lien discret « vérifier ma commune ↗ » ouvre Géorisques dans un nouvel onglet.

### Issue D — Ajouter un test de `requiredDiagnostics()`
**Labels :** `good first issue`, `tests`
La logique des diagnostics obligatoires est le cœur métier ; un test la protège des régressions. Écrire un petit fichier `tests/diagnostics.test.js` lançable avec `node --test`, couvrant quelques cas (maison d'avant 1949, maison classée E/F/G, appartement en copropriété…).
*Critère :* `node --test` passe, avec au moins quatre cas.

---

## 3. Faire connaître l'outil aux vendeurs

Priorité aux relais humains qui touchent déjà les gens au bon moment — plus efficace qu'une diffusion large.

- **Notaires près de Douarnenez.** Ton outil leur envoie des dossiers déjà complets : c'est un cadeau pour eux. Présente-leur le lien ; certains le recommanderont à leurs vendeurs.
- **ADIL du Finistère (29).** Conseil logement gratuit et neutre : relais naturel d'un outil libre et sans collecte.
- **Associations de consommateurs locales** (UFC-Que Choisir, CLCV). Un outil gratuit qui ne prend aucune donnée, c'est exactement ce qu'elles aiment relayer.
- **France Services / CCAS.** Points d'accueil qui touchent précisément les publics éloignés du numérique.
- **Groupes Facebook et forums « vente entre particuliers » (Bretagne / Finistère).** Une présence utile — répondre, puis mentionner l'outil quand c'est pertinent — marche mieux qu'une annonce.
- **Ton LinkedIn.** Post ci-dessous.

Côté codeurs : la communauté **BlueHats** (communs numériques d'intérêt public, autour de `code.gouv.fr`), un « show and tell » sur `dev.to` ou `r/opensource`, et le label `good first issue` sur le dépôt.

---

## 4. Post LinkedIn (brouillon, à retoucher)

> J'ai mis en ligne un petit outil. Rien de spectaculaire, honnêtement.
>
> Vendre un logement soi-même, sans agence, c'est possible — mais c'est un labyrinthe : quels diagnostics, quels papiers, dans quel ordre, jusqu'où aller seul avant le notaire. J'ai essayé de transformer ce labyrinthe en un fil qu'on suit étape par étape, jusqu'à la porte de l'étude.
>
> C'est gratuit, libre, et ça tient dans une seule page. Aucune donnée n'est collectée : tout reste sur votre appareil. Je crois que ça compte — un outil qui aide ne devrait pas, en échange, prendre quelque chose.
>
> Ce n'est pas parfait, sûrement incomplet, et le droit bouge. Je le laisse ouvert, justement, pour qu'on l'améliore à plusieurs — des vendeurs qui repèrent ce qui manque, des codeurs qui veulent mettre la main.
>
> 👉 https://myaiinside-png.github.io/vendez/
>
> Si ça épargne à quelqu'un une soirée d'angoisse administrative, ce sera déjà ça.
