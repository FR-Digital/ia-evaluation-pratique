# 30 Questions à Poser à Votre Équipe Technique

> **Les bonnes questions pour comprendre si votre IA fonctionne vraiment**

## Le Problème

Votre équipe technique utilise un jargon incompréhensible. Vous ne savez pas quelles questions poser pour évaluer la qualité de votre IA sans passer pour quelqu'un qui ne comprend rien.

## La Solution

Ces 30 questions sont formulées en langage simple, avec les réponses attendues et les signaux d'alerte.

---

## Questions sur la Performance (6 questions)

### 1. Quel est le taux de bonnes réponses ?

**Ce que la réponse devrait contenir :**
- Un pourcentage clair (ex: 78%)
- Sur combien de tests (ex: sur 500 cas)
- La définition de "bonne réponse"

**Signal d'alerte :**
- Réponse vague : "C'est assez bon"
- Pas de chiffre précis
- Test sur peu de cas (< 100)

**Bonne réponse :** "78% de bonnes réponses sur 500 cas de test représentatifs"

**Mauvaise réponse :** "Les résultats sont satisfaisants"

---

### 2. Combien de temps met l'IA à répondre ?

**Ce que la réponse devrait contenir :**
- Temps moyen en secondes
- Temps maximum en secondes
- Conditions du test (charge normale, pic)

**Signal d'alerte :**
- Mesuré uniquement en labo, pas en conditions réelles
- Temps maximum non mentionné
- "Ça dépend"

**Bonne réponse :** "En moyenne 2 secondes, maximum 8 secondes en période de pic"

**Mauvaise réponse :** "C'est quasi instantané"

---

### 3. Combien de fois l'IA se trompe gravement ?

**Ce que la réponse devrait contenir :**
- Taux d'erreurs critiques en %
- Définition d'erreur critique
- Exemples d'erreurs critiques détectées

**Signal d'alerte :**
- Pas de distinction entre erreur mineure et critique
- "Il n'y a pas d'erreurs"
- Pas d'exemples concrets

**Bonne réponse :** "3% d'erreurs critiques (information fausse ou dangereuse) sur 500 tests"

**Mauvaise réponse :** "Elle fait parfois des petites erreurs"

---

### 4. L'IA est-elle disponible 24/7 ?

**Ce que la réponse devrait contenir :**
- Taux de disponibilité en % (ex: 99.5%)
- Historique des pannes
- Système de monitoring

**Signal d'alerte :**
- Pas de SLA défini
- "On n'a jamais eu de panne" (suspect)
- Pas de monitoring

**Bonne réponse :** "99.2% de disponibilité avec monitoring temps réel et alertes automatiques"

**Mauvaise réponse :** "Normalement oui"

---

### 5. Que se passe-t-il si l'IA est surchargée ?

**Ce que la réponse devrait contenir :**
- Comportement sous charge (temps de réponse, file d'attente)
- Résultats des tests de charge
- Plan de scalabilité

**Signal d'alerte :**
- Pas de test de charge réalisé
- "On verra le moment venu"
- Pas de plan B

**Bonne réponse :** "Tests réalisés jusqu'à 10x la charge normale, temps de réponse reste < 10s"

**Mauvaise réponse :** "L'infrastructure devrait tenir"

---

### 6. L'IA s'améliore-t-elle avec le temps ?

**Ce que la réponse devrait contenir :**
- Mécanisme d'apprentissage
- Fréquence des mises à jour
- Comment les améliorations sont mesurées

**Signal d'alerte :**
- "Elle apprend toute seule" (dangereux)
- Pas de validation humaine des améliorations
- Pas de versioning

**Bonne réponse :** "Réentraînement mensuel sur nouveaux cas validés, avec tests avant déploiement"

**Mauvaise réponse :** "Elle apprend continuellement"

---

## Questions sur la Fiabilité (6 questions)

### 7. Comment savez-vous quand l'IA ne sait pas ?

**Ce que la réponse devrait contenir :**
- Score de confiance
- Seuil de confiance défini
- Comportement quand l'IA n'est pas sûre

**Signal d'alerte :**
- L'IA répond toujours, même quand elle ne sait pas
- Pas de score de confiance
- Pas d'escalade vers humain

**Bonne réponse :** "Si confiance < 70%, l'IA propose de transférer à un humain"

**Mauvaise réponse :** "L'IA fait toujours de son mieux"

---

### 8. L'IA peut-elle inventer des informations fausses ?

**Ce que la réponse devrait contenir :**
- Mécanismes anti-hallucination
- Sources de vérité définies
- Tests d'hallucination réalisés

**Signal d'alerte :**
- "Non, elle ne peut pas" (faux)
- Pas de garde-fous
- Pas de test spécifique

**Bonne réponse :** "Oui c'est un risque. On l'atténue avec vérification des sources et tests hebdomadaires"

**Mauvaise réponse :** "Non, notre IA est fiable"

---

### 9. Quand l'IA a-t-elle été testée pour la dernière fois ?

**Ce que la réponse devrait contenir :**
- Date précise
- Type de tests réalisés
- Résultats documentés

**Signal d'alerte :**
- Tests datant de plus de 3 mois
- "Au moment du développement"
- Pas de tests réguliers planifiés

**Bonne réponse :** "Dernier test complet il y a 2 semaines, résultats documentés"

**Mauvaise réponse :** "Au début du projet"

---

### 10. Que se passe-t-il si l'IA tombe en panne ?

**Ce que la réponse devrait contenir :**
- Plan de continuité
- Procédure de rollback
- Temps de rétablissement estimé

**Signal d'alerte :**
- Pas de plan B
- "Ça n'arrivera pas"
- Temps de rétablissement > 4 heures

**Bonne réponse :** "Fallback vers version précédente en 30 min, ou redirection vers équipe humaine"

**Mauvaise réponse :** "On appellera le support technique"

---

### 11. Les réponses sont-elles cohérentes ?

**Ce que la réponse devrait contenir :**
- Même question = même réponse ?
- Tests de cohérence réalisés
- Gestion des variations de formulation

**Signal d'alerte :**
- "Elle peut varier ses réponses" (risqué)
- Pas de test de cohérence
- Réponses contradictoires possibles

**Bonne réponse :** "Pour les questions factuelles, cohérence de 95% sur tests répétés"

**Mauvaise réponse :** "Elle essaie d'être cohérente"

---

### 12. Pouvez-vous expliquer pourquoi l'IA a répondu ça ?

**Ce que la réponse devrait contenir :**
- Niveau d'explicabilité (boîte noire vs interprétable)
- Logs des décisions
- Outils d'investigation disponibles

**Signal d'alerte :**
- "C'est trop complexe à expliquer"
- Boîte noire totale
- Pas de logs

**Bonne réponse :** "On peut tracer les sources utilisées et les règles appliquées pour chaque réponse"

**Mauvaise réponse :** "C'est de l'IA, c'est comme ça"

---

## Questions sur les Données (6 questions)

### 13. Sur quelles données l'IA a-t-elle été entraînée ?

**Ce que la réponse devrait contenir :**
- Volume de données (ex: 50 000 exemples)
- Type de données (textes, images, etc.)
- Période couverte
- Source des données

**Signal d'alerte :**
- Données trop anciennes (> 2 ans)
- Volume insuffisant (< 1000)
- Sources non vérifiées

**Bonne réponse :** "50 000 conversations de support des 2 dernières années, anonymisées"

**Mauvaise réponse :** "Beaucoup de données"

---

### 14. Les données sont-elles représentatives ?

**Ce que la réponse devrait contenir :**
- Couverture des cas d'usage réels
- Équilibre entre différentes catégories
- Biais identifiés et corrigés

**Signal d'alerte :**
- Pas d'analyse des biais
- Données uniquement des cas faciles
- Pas de diversité

**Bonne réponse :** "Analyse de biais réalisée, correction pour sous-représentation des cas complexes"

**Mauvaise réponse :** "On a pris ce qu'on avait"

---

### 15. Comment sont protégées les données personnelles ?

**Ce que la réponse devrait contenir :**
- Techniques d'anonymisation
- Conformité RGPD
- Lieu de stockage
- Accès restreints

**Signal d'alerte :**
- "C'est géré par le cloud"
- Pas d'anonymisation
- Stockage hors UE sans accord

**Bonne réponse :** "Données anonymisées, chiffrées, stockées en UE, accès audité"

**Mauvaise réponse :** "C'est sécurisé"

---

### 16. L'IA utilise-t-elle des données actualisées ?

**Ce que la réponse devrait contenir :**
- Fréquence de mise à jour des données
- Processus de rafraîchissement
- Gestion de l'obsolescence

**Signal d'alerte :**
- Données figées depuis le développement
- Pas de processus de mise à jour
- "Elle apprend en continu" sans contrôle

**Bonne réponse :** "Base de connaissances mise à jour mensuellement, validée par experts"

**Mauvaise réponse :** "Les données sont récentes"

---

### 17. Que fait l'IA avec les nouvelles interactions ?

**Ce que la réponse devrait contenir :**
- Conservation ou non des échanges
- Utilisation pour amélioration
- Consentement des utilisateurs

**Signal d'alerte :**
- Tout est stocké sans consentement
- Réentraînement automatique sans validation
- Pas de politique claire

**Bonne réponse :** "Interactions conservées 6 mois pour analyse, utilisateurs informés, opt-out possible"

**Mauvaise réponse :** "On garde tout pour améliorer"

---

### 18. L'IA a-t-elle accès à des données qu'elle ne devrait pas voir ?

**Ce que la réponse devrait contenir :**
- Périmètre d'accès défini
- Contrôles d'accès en place
- Audit de sécurité

**Signal d'alerte :**
- Accès trop large "pour simplifier"
- Pas de cloisonnement
- Pas d'audit

**Bonne réponse :** "Accès limité au périmètre défini, audit trimestriel, logs d'accès"

**Mauvaise réponse :** "Elle a accès à ce dont elle a besoin"

---

## Questions sur les Coûts (6 questions)

### 19. Combien coûte chaque réponse de l'IA ?

**Ce que la réponse devrait contenir :**
- Coût unitaire en euros
- Décomposition (compute, API, stockage)
- Variation selon la complexité

**Signal d'alerte :**
- "C'est inclus dans le forfait" sans détail
- Coût très variable sans explication
- Pas de tracking des coûts

**Bonne réponse :** "0.15€ par requête en moyenne, principalement coût API"

**Mauvaise réponse :** "C'est compétitif"

---

### 20. Le coût va-t-il augmenter avec l'usage ?

**Ce que la réponse devrait contenir :**
- Projection de coûts à volume cible
- Économies d'échelle possibles
- Plafonnement ou pas

**Signal d'alerte :**
- "Ça dépend du fournisseur"
- Pas de projection
- Coûts linéaires sans optimisation

**Bonne réponse :** "Coût augmente avec usage mais effet d'échelle dès 10k requêtes/mois"

**Mauvaise réponse :** "Normal que ça augmente"

---

### 21. Quel est le coût de maintenance annuel ?

**Ce que la réponse devrait contenir :**
- Budget maintenance prévu
- Ce que ça inclut (monitoring, updates, support)
- Équipe dédiée ou non

**Signal d'alerte :**
- "C'est compris dans le développement"
- Pas de budget prévu
- Sous-estimé (< 20% du dev initial)

**Bonne réponse :** "20% du coût de développement par an, incluant monitoring et mises à jour"

**Mauvaise réponse :** "Minimal"

---

### 22. Sommes-nous dépendants d'un fournisseur externe ?

**Ce que la réponse devrait contenir :**
- Liste des dépendances (API, cloud, etc.)
- Risques associés
- Plan de sortie si nécessaire

**Signal d'alerte :**
- Vendor lock-in total
- Pas de plan B si le fournisseur augmente ses prix
- "C'est le leader du marché"

**Bonne réponse :** "Dépendance API OpenAI, alternative testée, migration possible en 3 mois"

**Mauvaise réponse :** "On utilise les meilleurs"

---

### 23. Quels coûts cachés avez-vous identifiés ?

**Ce que la réponse devrait contenir :**
- Liste des coûts indirects (formation, intégration)
- Coûts de conformité
- Coûts de changement

**Signal d'alerte :**
- "Il n'y en a pas" (naïf)
- Pas d'analyse des coûts indirects
- Surprise à chaque nouvelle dépense

**Bonne réponse :** "Formation équipe : 5k€, audit sécurité : 10k€, temps d'intégration : 2 semaines"

**Mauvaise réponse :** "On a tout prévu"

---

### 24. Comment optimiser les coûts sans dégrader la qualité ?

**Ce que la réponse devrait contenir :**
- Leviers d'optimisation identifiés
- Trade-offs possibles
- Roadmap d'optimisation

**Signal d'alerte :**
- "C'est déjà optimisé"
- Pas de marge de manœuvre
- Qualité sacrifiée pour économiser

**Bonne réponse :** "Cache des réponses fréquentes (-30% coût), modèle plus léger pour cas simples"

**Mauvaise réponse :** "C'est le prix du marché"

---

## Questions sur les Risques (6 questions)

### 25. Quels sont les pires scénarios ?

**Ce que la réponse devrait contenir :**
- Liste des risques majeurs
- Probabilité et impact
- Plans de mitigation

**Signal d'alerte :**
- "Il n'y en a pas"
- Pas d'analyse des risques
- Trop optimiste

**Bonne réponse :** "3 risques majeurs : panne prolongée, fuite de données, réponses inappropriées. Mitigations en place."

**Mauvaise réponse :** "On n'a pas identifié de risques"

---

### 26. L'IA peut-elle dire quelque chose d'inapproprié ?

**Ce que la réponse devrait contenir :**
- Filtres de contenu en place
- Tests sur contenus sensibles
- Procédure si ça arrive

**Signal d'alerte :**
- "Non, c'est impossible"
- Pas de filtres
- Pas de procédure d'incident

**Bonne réponse :** "Filtres sur insultes, illégalité. Si incident : log, retrait, investigation"

**Mauvaise réponse :** "Notre IA est bien élevée"

---

### 27. Que se passe-t-il si quelqu'un manipule l'IA ?

**Ce que la réponse devrait contenir :**
- Tests d'attaques adverses
- Protection contre le jailbreak
- Monitoring des tentatives

**Signal d'alerte :**
- "Ce n'est pas un problème"
- Pas de tests d'attaque
- Pas de détection

**Bonne réponse :** "Tests de prompt injection réalisés, détection en place, logs des tentatives"

**Mauvaise réponse :** "Nos utilisateurs sont bienveillants"

---

### 28. L'IA peut-elle discriminer certains utilisateurs ?

**Ce que la réponse devrait contenir :**
- Tests de biais réalisés
- Métriques de fairness
- Plan de correction si biais détecté

**Signal d'alerte :**
- "L'IA est neutre"
- Pas de test de biais
- Pas de diversité dans les données d'entraînement

**Bonne réponse :** "Tests de biais sur genre, âge, origine. Biais détecté et corrigé sur X"

**Mauvaise réponse :** "L'IA traite tout le monde pareil"

---

### 29. Êtes-vous prêts pour un audit externe ?

**Ce que la réponse devrait contenir :**
- Documentation complète
- Traçabilité des décisions
- Conformité réglementaire

**Signal d'alerte :**
- "Quel audit ?"
- Documentation incomplète
- Pas de traçabilité

**Bonne réponse :** "Documentation complète, logs accessibles, conformité RGPD vérifiée"

**Mauvaise réponse :** "Pourquoi on serait audités ?"

---

### 30. Quel est le plan si l'IA est retirée demain ?

**Ce que la réponse devrait contenir :**
- Plan de continuité business
- Alternative manuelle
- Temps de transition

**Signal d'alerte :**
- "On ne peut pas se passer de l'IA"
- Pas de plan de secours
- Dépendance totale

**Bonne réponse :** "Retour au process manuel possible en 48h, équipe formée"

**Mauvaise réponse :** "L'IA ne sera pas retirée"

---

## Utilisation

1. **Imprimez cette liste** avant votre réunion avec l'équipe technique
2. **Posez 5-10 questions** selon votre priorité (performance, coûts, risques)
3. **Notez les réponses** et évaluez-les
4. **Signaux d'alerte ?** Creusez ou demandez des preuves
5. **Bonnes réponses ?** Demandez la documentation

## Ressources Associées

- [Framework 3 Niveaux](../frameworks/3-niveaux-evaluation.md) - Contexte pour ces questions
- [Checklist Qualité Minimum](../checklists/qualite-minimum.md) - Ce qui est non-négociable
- [Template Rapport Qualité](../templates/rapport-qualite.md) - Pour documenter les réponses

---

*Dernière MAJ : Novembre 2024 | LaFabriqAI*
