# Journal — Projet 3 : Évaluation d’une RAG locale pour le soutien informatique

Équipe : Sèdrick Zahn, Abdoulaye Dembele, Catherine [nom de famille]

## Tâches et responsables

| Tâche | Responsable | État |
|---|---|---|
| Proposition remise dans Léa | Toute l’équipe | [à faire / fait] |
| Dépôt GitHub créé, invitation envoyée à l’enseignant | [nom] | [à faire / fait] |
| Version A (script Python, Ollama, ChromaDB) | Sèdrick | À faire |
| Version B (n8n, formulaire, webhook) | Abdoulaye | À faire |
| Corpus, jeu de questions, BM25, script de tests | Catherine | À faire |
| Veille (releases Ollama, Chroma, n8n) | Abdoulaye | En cours |

## Entrées

### 2026-11-10 — Choix du sujet (toute l’équipe)
- **Résultat :** sujet retenu : évaluation d’une RAG locale (Ollama + ChromaDB) pour le soutien informatique, avec deux versions (Python et n8n) et comparaison avec BM25.
- **Décision :** équipe de trois ; ajout de la version n8n et de la comparaison de deux modèles pour adapter l’ampleur au nombre de participants.
- **Prochaine étape :** remettre la proposition au cours 11 et créer le dépôt.

### 2026-11-10 — Veille (Abdoulaye)
- **Outil :** documentation officielle de n8n.
- **Information :** n8n offre un nœud officiel Chroma Vector Store (insertion et récupération de documents, branchement à une chaîne question-réponse).
  Source : https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.vectorstorechroma/
- **Conséquence :** la version B peut interroger la même collection ChromaDB que la version A. ChromaDB sera donc exécuté en mode serveur. Le magasin intégré de n8n (non persistant) reste la solution de repli.

### 2026-11-10 — Utilisation d’un agent IA (Abdoulaye)
- **Objectif :** adapter la proposition au modèle de l’enseignant et répartir le travail à trois.
- **Apport retenu :** structure de la répartition des tâches, ajout de la version n8n et de la comparaison de modèles.
- **Vérification :** existence du nœud Chroma de n8n vérifiée dans la documentation officielle ; proposition relue par l’équipe [à confirmer].
- **Correction :** [s’il y a lieu].

## Contributions par membre

- **Sèdrick Zahn :** première version de la proposition (besoin, technologie, tests).
- **Abdoulaye Dembele :** adaptation de la proposition pour trois membres, version n8n, veille.
- **Catherine [nom de famille] :** [à compléter].
