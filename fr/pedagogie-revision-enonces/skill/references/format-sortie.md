# Format de sortie - Tableau de révision

## Structure du tableau

Le tableau de révision doit permettre une révision séquentielle sans sauts dans le document.

### Colonnes obligatoires

| Colonne | Contenu | Format |
|---------|---------|--------|
| **N°** | Numéro séquentiel | Entier (1, 2, 3...) |
| **Localisation** | Page ou section | "Page X" ou "Section Y" ou "Slide Z" |
| **Extrait** | Citation du passage problématique | Texte entre guillemets avec [...] si tronqué |
| **Type d'ambiguïté** | Catégorie du problème | Voir types ci-dessous |
| **Raison** | Explication précise du problème | 1-2 phrases claires |
| **Solution suggérée** | Piste de correction concrète | Action recommandée |

### Types d'ambiguïté (standardisés)

Utiliser ces termes standards pour faciliter le filtrage:

1. **Référence floue** - Pronom ou déterminant sans antécédent clair
2. **Instruction contradictoire** - Deux instructions qui se contredisent
3. **Condition implicite** - Condition d'application non spécifiée
4. **Terme non défini** - Terme technique sans définition
5. **Date/délai ambigu** - Indication temporelle imprécise
6. **Quantité floue** - Valeur numérique vague ou incohérente
7. **Critère subjectif** - Critère d'évaluation sans indicateurs mesurables
8. **Séquence imprécise** - Instructions multi-étapes sans ordre clair
9. **Portée floue** - Manque de clarté sur ce qui est inclus/exclu
10. **Responsabilité ambiguë** - Qui fait quoi pas clair (travaux d'équipe)
11. **Supposition non vérifiée** - Suppose connaissances non partagées
12. **Format mal spécifié** - Attentes imprécises sur format de remise

### Format de sortie

#### Pour les documents courts (< 5 pages ou < 2000 mots)
Tableau Markdown complet

#### Pour les documents moyens (5-15 pages)
Tableau Markdown avec résumé en haut

#### Pour les documents longs (> 15 pages)
1. Résumé exécutif (top 5-10 problèmes critiques)
2. Tableau complet Markdown

### Exemple de tableau complet

```markdown
# Révision pédagogique - [Nom du document]

## Résumé
- **Discipline détectée:** [Nom de la discipline]
- **Contexte:** [Type de travail/document]
- **Total d'ambiguïtés détectées:** 12
- **Critiques (à corriger immédiatement):** 5
- **Importantes (à clarifier):** 4
- **Mineures (suggestions):** 3

## Ambiguïtés par type
- Référence floue: 3
- Date/délai ambigu: 2
- Condition implicite: 2
- Terme non défini: 1
- (etc.)

## Tableau de révision séquentiel

| N° | Localisation | Extrait | Type | Raison | Solution suggérée |
|----|--------------|---------|------|--------|-------------------|
| 1 | Page 1 | "Vous devez le remettre avant..." | Référence floue | Le pronom "le" n'a pas d'antécédent clair. Réfère au rapport? Aux données? | Remplacer par: "Vous devez remettre **le rapport d'analyse complet** avant..." |
| 2 | Page 2 | "Deadline: vendredi prochain" | Date/délai ambigu | Date relative sans précision. Quel vendredi? À quelle heure? | Spécifier: "Date limite: vendredi 15 novembre 2025 à 23h59" |
| 3 | Page 2 | "Bonus de 5% pour travail exceptionnel" | Condition implicite | Critères d'attribution du bonus non définis | Ajouter grille: "Bonus si note ≥ 95% ET démonstration d'approche innovante" |
```

### Règles de tri et ordre

Le tableau DOIT être trié par ordre d'apparition dans le document (séquentiel) pour faciliter la révision:

1. Trier par page/section (ordre croissant)
2. À l'intérieur d'une page, trier par ordre d'apparition dans le texte
3. Numéroter séquentiellement (1, 2, 3...)

**❌ Ne PAS grouper par type d'ambiguïté** (cela force des sauts)

### Niveaux de sévérité (optionnel)

Si souhaité, ajouter une colonne "Priorité":

- 🔴 **Critique** - Bloque la compréhension, doit être corrigé
- 🟡 **Important** - Peut causer confusion, devrait être clarifié
- 🟢 **Mineur** - Suggestion d'amélioration, optionnel

### Format pour différents types de documents

#### Documents texte (DOCX, PDF, MD, TXT)
Localisation: "Page X" ou "Section Y, Page X"

#### Présentations (PPTX, Google Slides)
Localisation: "Diapo X" ou "Slide X"

#### Images avec texte
Localisation: "Image [nom_fichier]" ou "Image 1, texte ligne X"

### Cas particuliers

#### Ambiguïtés répétées
Si le même problème apparaît plusieurs fois:
- Le documenter à chaque occurrence
- Indiquer dans la solution: "(voir aussi N° X, Y)"
- Suggérer correction globale si applicable

#### Instructions qui s'étendent sur plusieurs pages
- Localiser à la première mention
- Mentionner: "s'étend sur pages X-Y"
- Expliquer où est la contradiction/ambiguïté

#### Références croisées problématiques
- Documenter aux deux endroits
- Clarifier quelle est la version correcte

### Fichiers de sortie

#### Markdown (.md)
Format principal pour facilité de lecture et modification

#### Tableau Excel (.xlsx) - Optionnel
Si l'utilisateur demande explicitement un format tableur

#### Format du nom de fichier
`revision_[nom-document]_[date].md`

Exemple: `revision_tp2-clinique_2025-11-04.md`
