# PatchMind : plateforme DevSecOps pour la remédiation automatisée des vulnérabilités

Plateforme qui détecte les vulnérabilités d'un projet, génère des correctifs avec des LLM et les valide automatiquement.

Projet réalisé en binôme avec Rabeb Jerbi (TEK-UP, 2025-2026). Ma contribution : [à compléter : par exemple l'authentification et le RBAC, l'intégration des scanners, le moteur RAG, le CI/CD].

Problème

Le délai moyen de remédiation (MTTR) reste élevé et les outils de scan produisent des résultats dispersés, sans correctif proposé.

Solution
Scanners intégrés : Semgrep (SAST), GitLeaks (secrets), Snyk/OSV (dépendances), OWASP ZAP (DAST).
Remédiation par IA : architecture RAG avec index FAISS (enrichissement CWE / CVE / NVD) et consensus multi-LLM (Gemini, Groq, Ollama).
Validation automatique des correctifs : vérification syntaxique, re-scan de sécurité, détection de régressions, score de confiance.
Plateforme web : authentification, 2FA (TOTP), contrôle d'accès par rôles, gestion de projets, historique, rapports PDF.
CI/CD : pipeline GitHub Actions, analyse d'image Docker avec Trivy.
Pile technique

Python, Flask, SQLAlchemy, SQLite, FAISS, Docker, GitHub Actions.

Méthode

Scrum, 4 sprints (authentification, intégration des outils, remédiation intelligente, optimisation).

Résultats des tests

Taux de réussite de 96,2 %, MTTR moyen de 14,32 secondes, score de confiance moyen de 72,2 %.

Perspectives

Voir le chapitre 5 du rapport.
