# Skill: revision-pedagogique

## Intention

Automatiser la détection d'ambiguïtés dans les documents pédagogiques (énoncés de TP, consignes, grilles d'évaluation) pour améliorer leur clarté et réduire la confusion chez les étudiants.

## Objectif

Identifier systématiquement les passages ambigus qui pourraient être mal interprétés par les étudiants et fournir des suggestions concrètes de clarification adaptées à la discipline détectée.

## Résultat attendu

Un tableau de révision séquentiel listant:
- La localisation de chaque ambiguïté (page/section)
- L'extrait problématique
- Le type d'ambiguïté (parmi 12 catégories)
- La raison du problème
- Une solution suggérée adaptée au contexte disciplinaire

### Exemple de sortie

```markdown
# Révision pédagogique - [Titre du document]

## Résumé
- **Discipline détectée:** Sciences naturelles (Chimie)
- **Total d'ambiguïtés:** 8
- **Distribution:** Référence floue (3), Date ambigu (2), Condition implicite (2), Format mal spécifié (1)

## Tableau de révision séquentiel

| N° | Localisation | Extrait | Type | Raison | Solution suggérée |
|----|--------------|---------|------|--------|-------------------|
| 1 | Page 1 | "Vous devez le remettre avant..." | Référence floue | "le" sans antécédent clair | "Vous devez remettre **le rapport de laboratoire complet** avant..." |
| 2 | Page 1 | "Deadline: vendredi prochain" | Date/délai ambigu | Date relative sans précision | "Date limite: vendredi 15 novembre 2025 à 23h59" |
```

## Utilisation

```
Télécharger un document → "Révise ce document" → Recevoir le tableau de révision
```

## Formats supportés

DOCX, PDF, PPTX, MD, TXT, Images avec texte

## Disciplines détectées

Sciences naturelles, Sciences humaines, Arts, Santé, Gestion, Techniques, Informatique

Le skill adapte automatiquement le vocabulaire de ses suggestions au contexte disciplinaire détecté.
