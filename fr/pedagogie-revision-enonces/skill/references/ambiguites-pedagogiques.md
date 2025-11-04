# Types d'ambiguïtés pédagogiques à détecter

Ce document répertorie les patterns d'ambiguïté à identifier dans les documents pédagogiques.

## 1. Références floues (Pronoms/Déterminants ambigus)

**Pattern:** Pronom sans antécédent clair ou référence ambiguë

**Exemples:**
- ❌ "Vous devez le remettre avant la date limite"
  - Problème: "le" réfère à quoi? Le travail? Le rapport? Le code?
  
- ❌ "Après avoir terminé, remettez-le sur LEA"
  - Problème: Terminé quoi? Remettre quoi?

- ❌ "Cette section doit être complétée"
  - Problème: Quelle section spécifiquement?

**Détection:**
- Pronoms: le, la, les, ce, cela, celui-ci, celui-là, en, y
- Déterminants démonstratifs: cette, ce, ces
- Sans nom spécifique dans les 2 phrases précédentes OU avec plusieurs référents possibles

**Solution:** Nommer explicitement l'objet ou le document

## 2. Instructions contradictoires

**Pattern:** Deux instructions qui se contredisent dans le document

**Exemples:**
- ❌ Page 2: "Le travail est individuel" + Page 5: "Divisez les tâches entre les membres de l'équipe"
- ❌ "Utilisez Python 3.8" + (plus loin) "Le code doit être compatible avec Python 3.11"
- ❌ "Date limite: 15 novembre" + (plus loin) "Remise le 20 novembre"

**Détection:**
- Mots-clés opposés: individuel/équipe, obligatoire/facultatif, permis/interdit
- Dates différentes pour le même livrable
- Versions/formats contradictoires

**Solution:** Identifier quelle instruction est correcte et éliminer l'autre

## 3. Conditions implicites non spécifiées

**Pattern:** Conditions d'application qui ne sont pas explicitement énoncées

**Exemples:**
- ❌ "Bonus de 5% pour travail exceptionnel"
  - Problème: Quels critères définissent "exceptionnel"?

- ❌ "Pénalité en cas de retard"
  - Problème: Quelle pénalité? Combien? Après quel délai?

- ❌ "Les étudiants en difficulté peuvent demander une extension"
  - Problème: Qui détermine "en difficulté"? Quelle procédure? Quel délai d'extension?

**Détection:**
- Termes subjectifs sans critères: exceptionnel, approprié, suffisant, adéquat, raisonnable
- Conséquences sans détails: pénalité, bonus, ajustement, modification
- Conditions sans procédure: "peuvent demander", "doivent justifier", "au besoin"

**Solution:** Expliciter les critères, valeurs ou procédures

## 4. Termes techniques non définis

**Pattern:** Utilisation de termes spécialisés sans définition ni contexte

**Exemples:**
- ❌ "Utilisez la méthode de recherche qualitative"
  - Problème (si 1ère mention): Méthode pas définie, étudiants peuvent ne pas connaître

- ❌ "Appliquez la théorie X dans votre analyse"
  - Problème: Quelle théorie précisément? Quels aspects?

- ❌ "Suivez les normes APA"
  - Problème: Quelle version? Tous les aspects ou certains seulement?

**Détection:**
- Acronymes non explicités
- Jargon technique sans définition au premier usage
- Termes supposant des connaissances préalables

**Solution:** Définir au premier usage ou référer à une ressource

## 5. Dates et délais ambigus

**Pattern:** Indication temporelle imprécise ou contradictoire

**Exemples:**
- ❌ "Remise en fin de session"
  - Problème: Quelle date exacte? Dernier jour de cours? Dernier jour d'examens?

- ❌ "Deadline: vendredi prochain"
  - Problème: Quel vendredi? À quelle heure?

- ❌ "Rapport à remettre dans 2 semaines"
  - Problème: À partir de quelle date? Moment de distribution? Moment de lecture?

**Détection:**
- Expressions relatives: prochain, dernier, dans X jours/semaines
- Expressions vagues: fin de session, bientôt, prochainement
- Absence d'heure pour une date limite
- Dates contradictoires dans le document

**Solution:** Utiliser date complète (jour/mois/année) et heure précise

## 6. Quantités et pourcentages flous

**Pattern:** Valeurs numériques imprécises ou incohérentes

**Exemples:**
- ❌ "Travail d'au moins 10 pages"
  - Problème: Interligne inclus? Marges standard? Pages de garde comptées?

- ❌ "Quelques exemples suffisent"
  - Problème: Combien? 2? 5? 10?

- ❌ "La majorité des points"
  - Problème: Combien exactement? 51%? 60%? 75%?

**Détection:**
- Quantificateurs vagues: plusieurs, quelques, nombreux, beaucoup, peu
- Termes relatifs: majorité, minorité, plupart
- Critères de longueur sans précision d'unité

**Solution:** Donner un nombre ou une fourchette précise

## 7. Critères d'évaluation subjectifs

**Pattern:** Critères de notation sans indicateurs mesurables

**Exemples:**
- ❌ "Travail de qualité professionnelle"
  - Problème: Comment mesurer "qualité"? Quels standards?

- ❌ "Présentation claire et organisée"
  - Problème: Quels éléments constituent "clair" et "organisé"?

- ❌ "Originalité de la solution"
  - Problème: Comment quantifier l'originalité?

**Détection:**
- Adjectifs évaluatifs sans critères: bon, excellent, approprié, adéquat, clair
- Absence de grille critériée ou de rubriques
- Termes subjectifs dans les critères de notation

**Solution:** Fournir grille critériée avec indicateurs observables

## 8. Séquences d'étapes imprécises

**Pattern:** Instructions multi-étapes sans ordre clair ou étapes manquantes

**Exemples:**
- ❌ "Préparez le matériel et commencez l'expérience"
  - Problème: Dans quel ordre? Quel matériel? Quelles étapes intermédiaires?

- ❌ "Analysez, rédigez et remettez votre travail"
  - Problème: Analyser avant ou pendant la rédaction? Quel type d'analyse?

**Détection:**
- Instructions en liste sans numérotation
- Connecteurs temporels ambigus: "puis", "ensuite", "après"
- Étapes intermédiaires omises

**Solution:** Numéroter les étapes et expliciter chaque sous-étape

## 9. Portée et limites floues

**Pattern:** Manque de clarté sur ce qui est inclus/exclu

**Exemples:**
- ❌ "Implémentez les fonctionnalités principales"
  - Problème: Quelles sont les fonctionnalités principales vs secondaires?

- ❌ "Vous pouvez utiliser des sources externes"
  - Problème: Lesquelles? Toutes? Avec quelles restrictions?

- ❌ "Travail en équipe de 2-4 personnes"
  - Problème: 1 personne seule est-elle acceptable? 5 personnes?

**Détection:**
- Termes de portée vagues: principal, secondaire, optionnel, suggéré
- Permissions sans limites: "pouvez utiliser", "libre choix"
- Fourchettes numériques sans précision sur les extrêmes

**Solution:** Énumérer ce qui est inclus/exclu explicitement

## 10. Responsabilités ambiguës (travaux d'équipe)

**Pattern:** Manque de clarté sur qui fait quoi dans un travail d'équipe

**Exemples:**
- ❌ "L'équipe doit produire un rapport"
  - Problème: Tous contribuent également? Un rédacteur principal?

- ❌ "Chaque membre doit participer"
  - Problème: Comment mesurer la participation? Quelle est la contribution minimale?

**Détection:**
- Instructions au niveau de l'équipe sans répartition
- Absence de mécanisme d'évaluation par les pairs
- Termes collectifs sans précision: "l'équipe", "tous les membres"

**Solution:** Clarifier les rôles et mécanismes d'évaluation individuelle

## 11. Suppositions non vérifiées

**Pattern:** Document suppose des connaissances ou un contexte non partagé

**Exemples:**
- ❌ "Comme vu en cours..." (sans préciser quoi)
- ❌ "Utilisez le template fourni" (quel template? où?)
- ❌ "Référez-vous à la documentation" (laquelle? où la trouver?)

**Détection:**
- Expressions présupposant contexte: "comme vu", "déjà expliqué", "fourni précédemment"
- Références sans liens ou précisions
- Présupposition d'outils/ressources sans identification

**Solution:** Fournir références complètes ou rappel bref du contexte

## 12. Formats et livrables mal spécifiés

**Pattern:** Attentes imprécises sur le format de remise

**Exemples:**
- ❌ "Remettez un document"
  - Problème: PDF? Word? Papier? Quelle longueur?

- ❌ "Incluez vos sources"
  - Problème: Format de citation? Bibliographie séparée? Quel style (APA, MLA)?

- ❌ "Préparez une présentation"
  - Problème: Durée? Format (PowerPoint, PDF, oral seulement)? Nombre de diapositives?

**Détection:**
- Termes génériques: document, fichier, présentation, code
- Absence de spécifications techniques
- Pas de modèle ou template fourni

**Solution:** Spécifier format exact, structure et contraintes techniques
