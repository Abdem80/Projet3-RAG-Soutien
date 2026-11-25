# Planning — Projet 3 (après la révision du sujet du 25 novembre)

> Dates à ajuster selon les dates réelles des cours 12 à 15 annoncées dans Léa.  
> Règle : chaque tâche terminée = une pull request relue + une entrée dans `journal.md`.

## Vue d’équipe

| Période | Sèdrick (version A) | Abdoulaye (version B, n8n) | Catherine (corpus, tests) | Ensemble |
|---|---|---|---|---|
| **Semaine 1** — 25 nov. au 1er déc. | Ollama + ChromaDB serveur installés ; script d’indexation | Docker + n8n installés ; connexion à Ollama et à ChromaDB ; premier workflow | Documents rassemblés et nettoyés ; `corpus.md` ; conversion en texte | Rencontre avec l’enseignant ; chacun fournit ses documents d’ici le 27 nov. |
| **Semaine 2** — 2 au 8 déc. | Script question-réponse avec sources ; tests 1 à 3 avec `llama3.2:3b` | Workflow RAG complet avec sources ; formulaire ; webhook | **Jeu de 25 questions figé (avant tout test)** ; script de tests ; BM25 | Point d’équipe en milieu de semaine : premiers résultats |
| **Semaine 3** — 9 au 15 déc. | Tests avec `qwen2.5:7b` ; comparaison des modèles | Tests 1 et 2 sur n8n (×3) ; comparaison A et B | Résultats BM25 ; comparaison Cloudflare | Recommandation, rapport, répétition de la démo, preuves locales enregistrées |
| **Après la démo** | Corrections | Corrections | Corrections | `remise.md`, tag `projet3-final` |

**Dépendances :**
- n8n et la version A ont besoin de la **même collection ChromaDB** → Sèdrick indexe, Abdoulaye se branche dessus. Si l’index n’est pas prêt, Abdoulaye teste avec quelques documents dans sa propre collection.
- Les tests ont besoin du **jeu de questions figé** → Catherine le livre au plus tard au début de la semaine 2.

## Détail de la partie d’Abdoulaye (version B — n8n)

### Semaine 1 — Installation et premier workflow
| Jour | Tâche | Résultat vérifiable |
|---|---|---|
| Jour 1 | Installer Docker Desktop et Ollama ; `ollama pull bge-m3` et `ollama pull llama3.2:3b` | `ollama list` affiche les modèles |
| Jour 2 | Lancer n8n avec Docker (volume pour garder les données) ; créer le compte administrateur local | n8n ouvert sur `http://localhost:5678` |
| Jour 3 | Connecter n8n à Ollama avec `http://host.docker.internal:11434` | Un nœud Ollama répond à un message test |
| Jour 4 | Lancer ChromaDB en serveur (ou se brancher sur celui de Sèdrick) ; tester le nœud Chroma Vector Store | Insertion et récupération de 2-3 documents test |
| Jour 5 | Premier workflow : question manuelle → recherche → réponse | Capture d’une réponse ; entrée de journal + 1 trace de veille |

### Semaine 2 — Workflow complet
| Tâche | Résultat vérifiable |
|---|---|
| Brancher le workflow sur la collection commune et faire renvoyer **le nom du document source** | Réponse avec source correcte sur 3 questions |
| Écrire le prompt strict : répondre seulement avec les passages, sinon « information introuvable dans les documents » | Test rapide sur 2 questions sans réponse |
| Déclencheur **Form** : l’étudiant pose sa question dans un formulaire | Capture du formulaire et de la réponse |
| Déclencheur **Webhook** pour que le script de tests de Catherine envoie les questions | Une requête `curl` reçoit une réponse JSON |
| Exporter les workflows en JSON dans `n8n/` ; procédure d’installation dans le README | Pull request relue |

### Semaine 3 — Tests et comparaison
| Tâche | Résultat vérifiable |
|---|---|
| Exécuter les tests 1 et 2 sur la version B, trois fois (via le webhook) | Tableaux de résultats dans `resultats/version-b/` |
| Noter les temps de réponse et le temps passé à installer et à modifier n8n | Mesures dans le tableau |
| Rédiger la comparaison version A / version B | Section du rapport à son nom |
| Préparer la partie n8n de la démo (scénario normal par formulaire + question sans réponse) et enregistrer une vidéo de secours | Vidéo et captures dans les preuves |

### Pièges connus
- Depuis le conteneur, `localhost` ne mène pas à Ollama : utiliser `host.docker.internal`.
- Le Simple Vector Store de n8n perd ses données au redémarrage : à n’utiliser qu’en repli.
- Noter les versions de n8n, d’Ollama et des modèles **avant** les tests (veille).
- Aucun document personnel ni secret dans le dépôt : les documents restent dans `corpus/`.
