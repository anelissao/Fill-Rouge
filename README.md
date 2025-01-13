# Fill-Rouge

# Cahier des Charges : debriefing.com

## 1. Contexte
Debriefing.com est une plateforme en ligne dédiée à l'évaluation entre pairs. Elle permet aux enseignants de créer des sujets de briefs et d'associer aléatoirement des étudiants pour corriger les travaux les uns des autres. Le système vise à simplifier le processus d'évaluation tout en encourageant une analyse critique entre étudiants.

---

## 2. Objectifs
- Automatiser la répartition des corrections entre pairs.
- Fournir un cadre structuré pour l'évaluation.
- Permettre aux enseignants de superviser et d'analyser les résultats.

---

## 3. Fonctionnalités principales

### 3.1 Enseignant
1. Création de sujets de brief avec description et critères d'évaluation.
2. Assignation manuelle ou automatique des pairs pour correction.
3. Visualisation des résultats des évaluations.

### 3.2 Étudiant
1. Consultation des sujets de brief et des livrables.
2. Correction structurée des travaux de pairs, section par section :
   - Instructions de correction.
   - Questions avec choix « Oui/Non » pour validation ou invalidation.
   - Commentaires ou retours facultatifs.
3. Validation ou non de la mise en situation de l'évalué.
4. Réception des commentaires de l’évaluateur.
5. Feedback sur l’évaluation reçue.

---

## 4. Contraintes techniques

### Technologies autorisées
- **Front-end :** HTML, CSS (ou TailwindCSS), JavaScript, ReactJS.
- **Back-end :** PHP, Laravel.
- **Base de données :** SQL.
- **Outils de conception :** UML, Figma.
- **Gestion de version :** Git.

### Contraintes spécifiques
- Système compatible avec les navigateurs modernes.
- Conception responsive pour mobile et desktop.

---

## 5. Sécurité
- Authentification sécurisée via mots de passe ou SSO.
- Protection contre les attaques XSS et CSRF.
- Cryptage des données sensibles.

---

## 6. Bonus
### 6.1 Système d'examen en ligne (optionnel)
Un module d'examen en ligne peut être intégré pour permettre aux enseignants de créer des tests pour la classe. Les fonctionnalités incluent :
1. Création et assignation d'examens à une classe.
2. Mode plein écran obligatoire pour minimiser les risques de triche.
3. Désactivation du clic droit et des raccourcis clavier pour bloquer les tentatives de copie ou de recherche.
4. Surveillance des changements d'onglets pour détecter les comportements suspects.
5. Chronomètre strict pour gérer la durée de l’examen.
6. Rapports détaillés pour les enseignants après chaque session d'examen.

**Exemple de sécurité anti-triche :**
- Surveillance des onglets :
```javascript
document.addEventListener("visibilitychange", () => {
    if (document.hidden) {
        alert("Vous avez quitté l'onglet de l'examen. Veuillez revenir immédiatement.");
    }
});
```
- Mode plein écran obligatoire :
```javascript
function startExam() {
    document.documentElement.requestFullscreen().catch(() => {
        alert("Veuillez activer le mode plein écran pour continuer l'examen.");
    });
}
```

---

## 7. Livrables
1. Code source complet (hébergé sur GitHub).
2. Documentation technique (UML, Figma).
3. Manuel utilisateur pour enseignants et étudiants.

---

## 8. Planning

### Phase 1 : Analyse et Conception
- Durée : 2 semaines.
- Livrables : Diagrammes UML, wireframes.

### Phase 2 : Développement
- Durée : 4 semaines.
- Livrables : Fonctionnalités principales.

### Phase 3 : Tests et Déploiement
- Durée : 2 semaines.
- Livrables : Plateforme fonctionnelle, rapport de tests.

---

## 9. Conclusion
Debriefing.com se positionne comme un outil essentiel pour l'évaluation entre pairs. L’ajout du module bonus d'examen en ligne renforce son utilité dans un cadre académique tout en montrant les compétences techniques de son développeur.

