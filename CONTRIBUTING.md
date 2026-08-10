# Contribuer à *De gré à gré*

Merci de l'intérêt porté au projet. C'est un outil civique : libre, gratuit, sans collecte de données, pensé pour rester accessible à tout le monde. Les contributions qui vont dans ce sens — plus simple, plus clair, plus juste — sont les bienvenues.

## Philosophie technique (à préserver)

- **Un seul fichier.** Toute l'application tient dans `index.html` (HTML + CSS + JavaScript). Pas de framework, pas d'étape de compilation, aucune dépendance à installer.
- **Aucun backend, aucun traceur.** Les données de l'utilisateur restent sur son appareil (`localStorage`). Le seul appel réseau est la recherche d'adresse, vers un service public (Base Adresse Nationale).
- **Vanilla JS.** Pas de bibliothèque JavaScript ajoutée. Les seules ressources externes sont les polices (Google Fonts) — une contribution qui les héberge localement, pour supprimer même cet appel, serait la bienvenue.
- **Sobriété.** Ça doit se charger vite, fonctionner sur un téléphone modeste et une connexion lente.

Si une idée impose un backend, un compte utilisateur, un traceur ou un outil de *build*, elle sort du cadre : ouvre plutôt une *issue* pour en discuter avant d'écrire du code.

## Deux façons de contribuer

**Sans savoir coder :** signaler un bug, une tournure peu claire ou une information légale erronée via les *issues*.

**En sachant coder :**
1. *Fork* du dépôt.
2. Modifier `index.html`.
3. Tester (voir plus bas).
4. Ouvrir une *pull request* qui explique le **pourquoi**, pas seulement le quoi.

Pour une petite correction, l'édition directe dans l'interface web de GitHub (icône crayon) suffit.

## Tester localement

Ouvre simplement `index.html` dans un navigateur. Pour tester la sauvegarde (`localStorage`) dans de bonnes conditions, sers le fichier via un petit serveur local :

```
python3 -m http.server
```

puis ouvre `http://localhost:8000`. Vérifie les six étapes, la recherche d'adresse, la génération de l'annonce, et la persistance (coche une case, ferme l'onglet, rouvre).

## Exactitude juridique — le point sensible

C'est un outil qui informe sur des obligations légales. **Une information fausse y est plus grave qu'un bug.** Toute contribution touchant aux diagnostics, aux délais, aux seuils ou aux pièces obligatoires doit **citer sa source officielle** dans la *pull request* : `service-public.fr`, Légifrance, ANIL/ADIL, ou le texte réglementaire concerné. Sans source vérifiable, la modification ne sera pas fusionnée. En cas de doute, on préfère prévenir l'utilisateur et le renvoyer à son notaire plutôt qu'affirmer.

## Style

- Français clair, à hauteur d'utilisateur : nommer les choses par ce que la personne connaît, pas par le jargon.
- Code lisible pour quelqu'un qui débute : noms explicites, pas d'astuce inutile.
- Réutiliser les variables CSS existantes (`:root`) plutôt que coder des couleurs en dur.

## Licence

En contribuant, tu acceptes que ton apport soit distribué sous la licence du projet (**AGPL-3.0**).
