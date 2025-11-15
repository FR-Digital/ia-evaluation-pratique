# Framework d'Évaluation IA en 3 Niveaux

> **Évaluer votre IA en 3 questions simples, dans l'ordre**

## Le Problème

Votre équipe technique vous présente des métriques comme "92% de précision" ou "F1-score de 0.85". Ces chiffres ne vous disent pas :
- Si l'IA répond réellement aux besoins de vos utilisateurs
- Si elle sera adoptée par vos équipes
- Si elle générera un retour sur investissement

## La Solution : Le Framework 3 Niveaux

Évaluez votre IA en répondant à 3 questions **dans l'ordre** (ne passez pas au niveau suivant sans valider le précédent) :

1. **Niveau 1** : Est-ce que ça marche ? (Tests techniques)
2. **Niveau 2** : Est-ce que c'est utilisé ? (Adoption)
3. **Niveau 3** : Est-ce que ça rapporte ? (ROI)

---

## Niveau 1 : Est-ce que Ça Marche ? 🔧

### Objectif
Vérifier que l'IA fonctionne techniquement et donne des réponses correctes.

### Méthode : Le Test des 100 Cas

Créez une liste de 100 questions/situations représentatives :
- **70 cas normaux** : Questions typiques du quotidien
- **20 cas limites** : Situations ambiguës ou complexes
- **10 cas pièges** : Questions hors sujet ou volontairement difficiles

### Exemple : Chatbot SAV

| Type | Question | Réponse Attendue | Réponse IA | Score |
|------|----------|------------------|------------|-------|
| Normal | "Comment retourner ma commande ?" | Procédure de retour en 3 étapes | "Pour retourner votre commande : 1) Allez sur Mon Compte..." | ✅ 1 pt |
| Limite | "Ma commande n'est pas arrivée mais le tracking dit livré" | Ouvrir une enquête avec le transporteur | "Je comprends votre frustration. Je vais ouvrir une enquête..." | ✅ 1 pt |
| Piège | "Quel est le meilleur restaurant à Paris ?" | Indiquer que c'est hors sujet | "Je peux vous aider uniquement pour vos commandes." | ✅ 1 pt |
| Limite | "Vous pouvez me rembourser ET garder le produit ?" | Refuser poliment | "Malheureusement, notre politique..." | ⚠️ 0.5 pt |

### Système de Scoring

- ✅ **Correcte** = 1 point
- ⚠️ **Partiellement correcte** = 0.5 point
- ❌ **Incorrecte ou dangereuse** = 0 point

**Score total** = (Points obtenus / 100) × 100%

### Seuils de Décision

| Score | Décision | Action |
|-------|----------|--------|
| **> 80%** | ✅ Validé | Passer au Niveau 2 |
| **60-80%** | ⚠️ À améliorer | Corriger les erreurs, retester |
| **< 60%** | ❌ Échec | Stop ou refonte majeure |

### Métriques à Demander à l'Équipe Technique

| Métrique | Seuil Minimum | Ce que ça signifie |
|----------|---------------|---------------------|
| **Précision** | > 70% | Proportion de bonnes réponses |
| **Temps de réponse** | < 5 secondes | Rapidité de l'IA |
| **Taux d'erreur critique** | < 10% | Réponses dangereuses ou fausses |
| **Disponibilité** | > 95% | L'IA est accessible |

### Checklist Niveau 1

- [ ] 100 cas de test créés (70/20/10)
- [ ] Score global > 80%
- [ ] Aucune erreur critique détectée
- [ ] Temps de réponse acceptable
- [ ] Disponibilité > 95%
- [ ] Équipe technique fournit les métriques

**Si validé → Passez au Niveau 2**

---

## Niveau 2 : Est-ce que les Utilisateurs l'Utilisent ? 👥

### Objectif
Vérifier que les vrais utilisateurs adoptent l'IA et en sont satisfaits.

### Méthode : Le Beta Test

**Configuration :**
- **Durée** : 2 à 4 semaines
- **Participants** : 20 à 50 utilisateurs représentatifs
- **Environnement** : Production ou pré-production réaliste

### Métriques Quantitatives à Suivre

| Métrique | Comment la Calculer | Seuil Minimum |
|----------|---------------------|---------------|
| **Taux d'utilisation** | Nb utilisateurs actifs / Nb total utilisateurs | > 50% |
| **Fréquence** | Nb moyen d'utilisations par jour par utilisateur | > 1 fois/jour |
| **Durée moyenne** | Temps passé par session | > 2 minutes |
| **Taux d'abandon** | % d'utilisateurs qui arrêtent en cours de route | < 30% |
| **Thumbs up/down** | Ratio de feedbacks positifs | > 60% positifs |

### Métriques Qualitatives

**Satisfaction globale** (échelle 1-5)
- 5 = Excellent, je recommande
- 4 = Bon, quelques améliorations possibles
- 3 = Correct, mais pas convaincu
- 2 = Décevant
- 1 = Inutilisable

**Seuil minimum** : Moyenne > 3.5/5

**Entretiens utilisateurs** (5-10 personnes)
- Ce qu'ils aiment
- Ce qui les frustre
- Ce qui manque
- S'ils utiliseraient en production

### Seuils de Décision

| Résultat | Décision | Action |
|----------|----------|--------|
| Adoption > 50%, Satisfaction > 3.5/5 | ✅ Validé | Passer au Niveau 3 |
| Adoption 30-50%, Satisfaction 3-3.5/5 | ⚠️ À améliorer | Itérer 2-4 semaines |
| Adoption < 30%, Satisfaction < 3/5 | ❌ Échec | Stop ou refonte UX |

### Signaux d'Alerte

| Signal | Cause Probable | Action |
|--------|----------------|--------|
| Faible adoption | L'IA n'est pas utile ou pas accessible | Vérifier le besoin réel |
| Fort abandon | Réponses trop lentes ou frustrantes | Améliorer la performance |
| Satisfaction basse | Réponses incorrectes ou incomplètes | Retourner au Niveau 1 |
| Pas de retour | Utilisateurs indifférents | Revoir la proposition de valeur |

### Checklist Niveau 2

- [ ] Beta test de 2-4 semaines réalisé
- [ ] 20-50 utilisateurs ont participé
- [ ] Taux d'adoption > 50%
- [ ] Satisfaction moyenne > 3.5/5
- [ ] Thumbs up > 60%
- [ ] Taux d'abandon < 30%
- [ ] Entretiens utilisateurs réalisés
- [ ] Problèmes majeurs identifiés et résolus

**Si validé → Passez au Niveau 3**

---

## Niveau 3 : Est-ce que Ça a un Impact Business ? 💰

### Objectif
Mesurer la valeur business réelle de l'IA et calculer le ROI.

### Méthode : L'A/B Test

**Configuration :**
- **Durée** : 1 à 3 mois
- **Groupes** :
  - Groupe A : Avec l'IA
  - Groupe B : Sans l'IA (méthode actuelle)
- **Taille** : Minimum 100 utilisateurs par groupe

### KPIs à Comparer

| KPI | Groupe A (avec IA) | Groupe B (sans IA) | Amélioration |
|-----|-------------------|-------------------|--------------|
| Temps de réponse moyen | 2 min | 8 min | **-75%** |
| Satisfaction client | 4.2/5 | 3.5/5 | **+20%** |
| Volume traité/jour | 150 tickets | 50 tickets | **+200%** |
| Résolution 1er contact | 85% | 60% | **+25%** |

### Calcul du ROI

**Formule :**
```
ROI = (Gains - Coûts) / Coûts × 100
```

**Exemple Concret : Chatbot SAV**

| Élément | Montant | Détail |
|---------|---------|--------|
| **GAINS** | | |
| Réduction temps agents | 120 000 € | 2 agents économisés × 60k€/an |
| Augmentation satisfaction | 30 000 € | Moins de churn client |
| Volume supplémentaire | 30 000 € | Plus de tickets traités |
| **Total Gains** | **180 000 €** | |
| **COÛTS** | | |
| Développement | 50 000 € | Initial |
| Infrastructure | 15 000 € | Serveurs/cloud |
| Maintenance | 20 000 € | Support annuel |
| Formation équipes | 10 000 € | Onboarding |
| Licences | 10 000 € | Logiciels tiers |
| **Total Coûts** | **105 000 €** | |
| **ROI** | **(180k - 105k) / 105k × 100 = 71%** | |

### Seuils de Décision

| Résultat | Décision | Action |
|----------|----------|--------|
| ROI > 50% | ✅ Go Production | Déployer à grande échelle |
| ROI 0-50% | ⚠️ Acceptable | Optimiser avant scale-up |
| ROI < 0% | ❌ Non rentable | Pivoter ou arrêter |
| Payback > 18 mois | ⚠️ Risqué | Réduire les coûts |

### Checklist Niveau 3

- [ ] A/B test de 1-3 mois réalisé
- [ ] Minimum 100 utilisateurs par groupe
- [ ] KPIs mesurés des deux côtés
- [ ] ROI calculé et documenté
- [ ] Payback period < 18 mois
- [ ] Amélioration KPI > 10%
- [ ] Validation par la finance
- [ ] Plan de déploiement prêt

**Si validé → Go Production !**

---

## Quand Arrêter un Projet IA

### Règles Claires

| Situation | Seuil | Décision | Justification |
|-----------|-------|----------|---------------|
| 🔴 **Niveau 1 échoue** | Score < 60% | **STOP immédiat** | L'IA ne fonctionne pas techniquement |
| 🟡 **Niveau 2 échoue** | Adoption < 30% après 2 itérations | **STOP ou pivot** | Les utilisateurs n'en veulent pas |
| 🟢 **Niveau 3 décevant** | ROI < 0% après 6 mois | **STOP ou réduire** | Pas de valeur business |

### Questions à Se Poser Avant d'Arrêter

1. A-t-on bien compris le besoin utilisateur ?
2. Le problème est-il technique ou d'usage ?
3. Y a-t-il un pivot possible ?
4. Quels apprentissages tirer ?

---

## Résumé Visuel

```
┌─────────────────────────────────────────────────────┐
│                   ÉVALUATION IA                     │
│                  Framework 3 Niveaux                │
└─────────────────────────────────────────────────────┘
                          │
                          ▼
            ┌─────────────────────────┐
            │    NIVEAU 1 : MARCHE    │
            │    Est-ce que ça marche?│
            │    Score > 80% ?        │
            └─────────────────────────┘
                    │           │
                   OUI         NON
                    │           │
                    ▼           ▼
            ┌──────────┐  ┌──────────┐
            │ Continuer│  │   STOP   │
            └──────────┘  │  ou      │
                    │     │ Améliorer│
                    │     └──────────┘
                    ▼
            ┌─────────────────────────┐
            │   NIVEAU 2 : UTILISÉ    │
            │   Adoption > 50% ?      │
            │   Satisfaction > 3.5/5 ?│
            └─────────────────────────┘
                    │           │
                   OUI         NON
                    │           │
                    ▼           ▼
            ┌──────────┐  ┌──────────┐
            │ Continuer│  │ Améliorer│
            └──────────┘  │   UX     │
                    │     └──────────┘
                    ▼
            ┌─────────────────────────┐
            │   NIVEAU 3 : RAPPORTE   │
            │   ROI > 0% ?            │
            │   Payback < 18 mois ?   │
            └─────────────────────────┘
                    │           │
                   OUI         NON
                    │           │
                    ▼           ▼
            ┌──────────┐  ┌──────────┐
            │    GO    │  │ Optimiser│
            │PRODUCTION│  │ ou STOP  │
            └──────────┘  └──────────┘
```

---

## Ressources Associées

- [Grille d'Évaluation Excel](../templates/grille-evaluation.xlsx) - Template pour le Test des 100 Cas
- [Questions à l'Équipe Technique](../guides/questions-equipe-technique.md) - 30 questions business-friendly
- [Checklist Qualité Minimum](../checklists/qualite-minimum.md) - Non-négociables
- [Exemple Chatbot](../examples/evaluation-chatbot.md) - Cas complet documenté

---

*Dernière MAJ : Novembre 2024 | Framework développé par LaFabriqAI basé sur les meilleures pratiques d'évaluation IA*
