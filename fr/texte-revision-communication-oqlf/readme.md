# Skill: texte-revision-communication-oqlf

## Intention

Automatiser la révision de courriels et messages Teams en français québécois pour garantir le respect des normes de l'OQLF (ponctuation, typographie, vocabulaire) et maintenir un style professionnel, direct et bienveillant.

## Objectif

Corriger automatiquement les erreurs typographiques spécifiques au français québécois, éliminer les anglicismes, ajuster le style pour une communication professionnelle claire et valider les dates mentionnées.

## Résultat attendu

Un message révisé avec:
- Liste des révisions effectuées et leurs justifications
- Dates à confirmer (si applicable)
- Texte corrigé selon les normes OQLF
- Notes additionnelles si pertinentes

### Exemple de sortie

**Avant:**
```
Bonjour,
Je voulais savoir si vous pourriez me transmettre le rapport avant Vendredi prochain ?
Merci beaucoup !
```

**Après:**
```
📧 Courriel

✏️ RÉVISIONS :
- "Vendredi" → "vendredi" (minuscule aux jours)
- Suppression de l'espace avant "?" (norme québécoise)
- "Je voulais savoir si vous pourriez" → "Pouvez-vous" (style direct)
- Retrait du point d'exclamation excessif

📅 DATES À CONFIRMER :
- "vendredi prochain" - Date: vendredi 8 novembre 2025

---

MESSAGE RÉVISÉ :

Bonjour,

Pouvez-vous me transmettre le rapport avant vendredi prochain?

Merci!
```

## Utilisation

```
Coller votre texte → "Révise ce message" → Recevoir la version corrigée
```

Le skill demande automatiquement le type de message (courriel/Teams) s'il n'est pas spécifié.

## Normes appliquées

### Ponctuation québécoise (≠ France)
- **PAS d'espace avant:** , . ! ?
- **Espace insécable avant:** ; : » %
- **Guillemets:** « texte » (avec espaces)

### Typographie
- Minuscules: jours, mois, titres de fonction
- Dates: lundi 4 novembre 2025 (sans virgule)
- Heures: 14 h 30 (espace insécable)

### Vocabulaire
- Courriel (pas email)
- Fin de semaine (pas weekend)
- Logiciel (pas software)
- En ligne (pas online)

### Style
- Phrases courtes (≤25 mots)
- Ton direct et bienveillant
- Élimination du conditionnel inutile
