# Checklist Qualité Minimum

> **Ce qu'il FAUT avoir avant de lancer votre IA - Non négociable**

## Pourquoi Cette Checklist ?

Avant de présenter votre IA aux utilisateurs ou de la mettre en production, certains critères sont **absolument essentiels**. Cette checklist vous évite les échecs coûteux et les mauvaises surprises.

---

## La Checklist

### 1. Performance Technique ✅

- [ ] **Précision > 70%** sur un jeu de test représentatif
  - *Pourquoi :* En dessous, l'IA se trompe trop souvent et perd la confiance des utilisateurs
  - *Comment vérifier :* Demandez le rapport de test avec les métriques détaillées

- [ ] **Temps de réponse < 5 secondes**
  - *Pourquoi :* Les utilisateurs abandonnent après 5s d'attente
  - *Comment vérifier :* Faites des tests en conditions réelles (pas en labo)

- [ ] **Disponibilité > 95%**
  - *Pourquoi :* Une IA qui tombe souvent ne sera pas utilisée
  - *Comment vérifier :* Demandez les SLA et le monitoring mis en place

- [ ] **Aucune erreur critique détectée**
  - *Pourquoi :* Une seule erreur grave peut ruiner la réputation
  - *Comment vérifier :* Revue des cas de test échoués avec classification de criticité

### 2. Sécurité et Conformité ✅

- [ ] **Données sensibles protégées**
  - *Pourquoi :* RGPD, réputation, responsabilité légale
  - *Comment vérifier :* Audit de sécurité, chiffrement vérifié

- [ ] **Pas de biais discriminatoire**
  - *Pourquoi :* Risques légaux et éthiques majeurs
  - *Comment vérifier :* Tests sur différents groupes démographiques

- [ ] **Traçabilité des décisions**
  - *Pourquoi :* Pouvoir expliquer pourquoi l'IA a répondu X
  - *Comment vérifier :* Logs complets et interprétables

- [ ] **Conformité RGPD**
  - *Pourquoi :* Amendes jusqu'à 4% du CA
  - *Comment vérifier :* DPO consulté, consentements en place

### 3. Utilisabilité ✅

- [ ] **Interface intuitive**
  - *Pourquoi :* Si c'est compliqué, personne ne l'utilisera
  - *Comment vérifier :* Test avec 5 utilisateurs novices

- [ ] **Messages d'erreur clairs**
  - *Pourquoi :* L'utilisateur doit comprendre quoi faire en cas de problème
  - *Comment vérifier :* Scénarios d'erreur testés

- [ ] **Possibilité de corriger l'IA**
  - *Pourquoi :* L'IA fait des erreurs, il faut pouvoir les signaler
  - *Comment vérifier :* Mécanisme de feedback intégré

- [ ] **Documentation utilisateur**
  - *Pourquoi :* Les utilisateurs doivent savoir comment utiliser l'outil
  - *Comment vérifier :* Guide disponible et testé

### 4. Robustesse ✅

- [ ] **Plan de rollback**
  - *Pourquoi :* Pouvoir revenir en arrière si ça ne marche pas
  - *Comment vérifier :* Procédure documentée et testée

- [ ] **Monitoring en place**
  - *Pourquoi :* Détecter les problèmes avant les utilisateurs
  - *Comment vérifier :* Alertes configurées, dashboard visible

- [ ] **Fallback humain**
  - *Pourquoi :* L'IA ne peut pas tout gérer
  - *Comment vérifier :* Escalade vers humain testée

- [ ] **Tests de charge réalisés**
  - *Pourquoi :* L'IA doit tenir sous la charge réelle
  - *Comment vérifier :* Rapport de tests de performance

### 5. Business Readiness ✅

- [ ] **Objectif business clair**
  - *Pourquoi :* Sans objectif, impossible de mesurer le succès
  - *Comment vérifier :* KPIs définis et mesurables

- [ ] **Budget maintenance prévu**
  - *Pourquoi :* L'IA nécessite un entretien continu
  - *Comment vérifier :* Ligne budgétaire validée

- [ ] **Équipe de support identifiée**
  - *Pourquoi :* Quelqu'un doit gérer les problèmes
  - *Comment vérifier :* Responsables nommés avec disponibilité

- [ ] **Communication aux utilisateurs préparée**
  - *Pourquoi :* Les utilisateurs doivent être informés et formés
  - *Comment vérifier :* Plan de communication validé

---

## Scoring

**Comptez vos ✅ :**

| Score | Statut | Action |
|-------|--------|--------|
| **20/20** | 🟢 Prêt | Lancez en production |
| **16-19** | 🟡 Presque prêt | Corrigez les manques |
| **12-15** | 🟠 Risqué | Remettez en question le lancement |
| **< 12** | 🔴 Non prêt | Stop, retournez en développement |

---

## Ce Qui N'est PAS Négociable

Ces 5 points sont des **bloquants absolus** :

1. ❌ Précision < 60%
2. ❌ Erreurs critiques non résolues
3. ❌ Non-conformité RGPD
4. ❌ Pas de plan de rollback
5. ❌ Pas de monitoring

**Si un seul de ces points est rouge, NE LANCEZ PAS.**

---

## Utilisation

1. Imprimez cette checklist
2. Parcourez chaque point avec votre équipe technique
3. Documentez les preuves de validation
4. Si < 16/20, retardez le lancement
5. Refaites la checklist avant chaque mise à jour majeure

---

## Ressources Associées

- [Framework 3 Niveaux](../frameworks/3-niveaux-evaluation.md) - Pour aller plus loin
- [Checklist Pré-Production](pre-production.md) - Vérifications techniques détaillées
- [Questions à l'Équipe Technique](../guides/questions-equipe-technique.md) - Pour creuser chaque point

---

*Dernière MAJ : Novembre 2024 | LaFabriqAI*
