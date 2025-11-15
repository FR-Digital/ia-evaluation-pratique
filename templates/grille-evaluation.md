# Template : Grille d'Évaluation IA

> **Test des 100 Cas - Évaluez votre IA méthodiquement**

## Comment Utiliser Ce Template

Ce template vous guide pour créer votre propre grille d'évaluation Excel. Vous pouvez copier les tableaux ci-dessous dans votre tableur préféré (Excel, Google Sheets, etc.).

---

## Onglet 1 : Test des 100 Cas

### Structure du Tableau

| ID | Type | Question/Situation | Réponse Attendue | Réponse IA | Score | Commentaire |
|----|------|-------------------|------------------|------------|-------|-------------|
| 1 | Normal | | | | | |
| 2 | Normal | | | | | |
| ... | ... | ... | ... | ... | ... | ... |
| 100 | Piège | | | | | |

### Répartition des Types

- **70 cas normaux** (ID 1-70) : Questions typiques du quotidien
- **20 cas limites** (ID 71-90) : Situations ambiguës ou complexes
- **10 cas pièges** (ID 91-100) : Questions hors sujet ou volontairement difficiles

### Système de Scoring

Dans la colonne "Score", utilisez :
- **1** = Correcte
- **0.5** = Partiellement correcte
- **0** = Incorrecte ou dangereuse

### Exemple Rempli (Chatbot SAV)

| ID | Type | Question/Situation | Réponse Attendue | Réponse IA | Score | Commentaire |
|----|------|-------------------|------------------|------------|-------|-------------|
| 1 | Normal | Comment retourner ma commande ? | Procédure en 3 étapes | "Pour retourner : 1) Connectez-vous..." | 1 | Parfait |
| 2 | Normal | Délai de livraison express ? | 24-48h | "Livraison en 24-48h ouvrées" | 1 | OK |
| 15 | Normal | Puis-je modifier ma commande ? | Oui si non expédiée | "Oui, contactez-nous rapidement" | 0.5 | Incomplet |
| 71 | Limite | Commande non reçue mais tracking OK | Ouvrir enquête | "Je comprends. Enquête ouverte..." | 1 | Bien géré |
| 85 | Limite | Produit cassé à réception | Retour + remplacement | "Désolé. Envoyez photos..." | 0.5 | Manque détail |
| 91 | Piège | Meilleur restaurant Paris ? | Hors sujet | "Je ne peux pas vous aider..." | 1 | Correct |
| 95 | Piège | Rembourse + garde produit ? | Refuser | "Politique ne permet pas..." | 1 | Bien refusé |

---

## Onglet 2 : Scoring Automatique

### Formules à Appliquer

```
Score Total = SOMME(colonne Score) / 100 * 100

Score par Type :
- Normal = SOMME.SI(Type="Normal"; Score) / 70 * 100
- Limite = SOMME.SI(Type="Limite"; Score) / 20 * 100
- Piège = SOMME.SI(Type="Piège"; Score) / 10 * 100
```

### Tableau de Synthèse

| Catégorie | Nb de Cas | Points Obtenus | Score (%) |
|-----------|-----------|----------------|-----------|
| Normal | 70 | [formule] | [formule] |
| Limite | 20 | [formule] | [formule] |
| Piège | 10 | [formule] | [formule] |
| **TOTAL** | **100** | **[formule]** | **[formule]** |

### Interprétation

| Score Global | Statut | Action Recommandée |
|--------------|--------|-------------------|
| > 80% | ✅ Validé | Passer au Niveau 2 (test utilisateurs) |
| 60-80% | ⚠️ À améliorer | Corriger les erreurs, refaire le test |
| < 60% | ❌ Échec | Arrêter ou refonte majeure |

---

## Onglet 3 : Dashboard

### Indicateurs Clés

| Indicateur | Valeur | Seuil | Statut |
|------------|--------|-------|--------|
| Score Global | [%] | > 80% | [✅/⚠️/❌] |
| Erreurs Critiques | [nb] | < 10 | [✅/⚠️/❌] |
| Score Cas Normaux | [%] | > 85% | [✅/⚠️/❌] |
| Score Cas Limites | [%] | > 70% | [✅/⚠️/❌] |
| Score Cas Pièges | [%] | > 60% | [✅/⚠️/❌] |

### Graphiques Recommandés

1. **Histogramme** : Score par type de cas
2. **Jauge** : Score global avec zones rouge/jaune/vert
3. **Camembert** : Répartition des scores (1 / 0.5 / 0)

### Erreurs Critiques à Lister

| ID | Question | Réponse IA | Problème | Priorité |
|----|----------|------------|----------|----------|
| | | | | HAUTE |
| | | | | HAUTE |

---

## Onglet 4 : Instructions d'Utilisation

### Avant de Commencer

1. **Définissez vos cas de test** : Utilisez votre connaissance métier
2. **Impliquez les experts** : Demandez aux utilisateurs finaux leurs questions types
3. **Soyez exhaustif** : Couvrez tous les scénarios possibles
4. **Variez la difficulté** : 70% facile, 20% moyen, 10% difficile

### Pendant le Test

1. **Testez dans l'ordre** : Du cas 1 au cas 100
2. **Soyez objectif** : Notez exactement ce que répond l'IA
3. **Documentez** : Ajoutez des commentaires utiles
4. **Ne trichez pas** : Un 0.5 n'est pas un 1

### Après le Test

1. **Analysez les patterns** : Quels types d'erreurs reviennent ?
2. **Priorisez** : Quelles erreurs sont les plus graves ?
3. **Partagez** : Présentez les résultats à l'équipe technique
4. **Planifiez** : Définissez les actions correctives

### Bonnes Pratiques

- ✅ Refaire le test après chaque mise à jour majeure
- ✅ Impliquer différentes personnes dans la notation
- ✅ Garder l'historique des tests
- ✅ Comparer les scores dans le temps

- ❌ Ne pas être trop indulgent
- ❌ Ne pas tester uniquement les cas faciles
- ❌ Ne pas ignorer les erreurs critiques
- ❌ Ne pas sauter l'étape documentation

---

## Créer Votre Fichier Excel

### Option 1 : Google Sheets
1. Créez un nouveau Google Sheets
2. Nommez les onglets : "Test 100 Cas", "Scoring", "Dashboard", "Instructions"
3. Copiez les tableaux ci-dessus
4. Ajoutez les formules

### Option 2 : Microsoft Excel
1. Créez un nouveau classeur Excel
2. Ajoutez 4 feuilles avec les noms ci-dessus
3. Reproduisez la structure des tableaux
4. Utilisez les formules SOMME.SI, NB.SI, etc.

### Option 3 : LibreOffice Calc
1. Même procédure que Excel
2. Compatible avec les mêmes formules

---

## Ressources Associées

- [Framework 3 Niveaux](../frameworks/3-niveaux-evaluation.md) - Contexte du test
- [Checklist Qualité Minimum](../checklists/qualite-minimum.md) - Critères non-négociables
- [Exemple Chatbot](../examples/evaluation-chatbot.md) - Cas concret rempli

---

*Dernière MAJ : Novembre 2024 | LaFabriqAI*
