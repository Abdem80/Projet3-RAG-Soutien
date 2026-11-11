# Journal — Projet 3 : Évaluation d’une RAG locale pour le soutien informatique

Équipe : Sèdrick Zahn, Abdoulaye Dembele, Catherine Guilene Ngo Ebga

Dépôt : [Projet3-RAG-Soutien](https://github.com/Abdem80/Projet3-RAG-Soutien)

## Tâches et responsables

| Tâche | Responsable | État |
|---|---|---|
| Proposition remise dans Léa | Toute l’équipe | [à faire / fait] |
| Dépôt GitHub créé, invitation envoyée à l’enseignant | Abdoulaye | Fait (invitations en attente d’acceptation : Sèdrick, enseignant) |
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

### 2026-11-10 — Révision de la proposition (Catherine)
- **Résultat :** en-tête complété (noms, lien du dépôt, date), sections réorganisées, preuve d’utilité précisée (16 sur 20 et 5 sur 5), matériel du poste d’essai précisé, dates de consultation des sources ajoutées.
- **Décision :** toute modification majeure du sujet ou du travail prévu sera soumise à l’enseignant.

### 2026-11-11 — Dépôt GitHub et accès (Abdoulaye)
- **Résultat :** dépôt privé créé (https://github.com/Abdem80/Projet3-RAG-Soutien) avec la proposition, le journal, l’énoncé, un README et un `.gitignore` (environnements virtuels, secrets, données locales de ChromaDB et de n8n exclus).
- **Accès :** Catherine (Guilene-choco92) a accepté l’invitation ; invitations envoyées à Sèdrick (5edrickk) et à l’enseignant (nicolas.payre@cegepsherbrooke.qc.ca), en attente d’acceptation.
- **Décision :** une branche et une pull request relue par un autre membre pour chaque tâche (voir README).
- **Prochaine étape :** confirmer l’acceptation des invitations ; commencer les travaux du cours 12.

### 2026-11-11 — Utilisation d’un agent IA (Abdoulaye)
- **Objectif :** initialiser le dépôt Git, le publier sur GitHub et gérer les invitations.
- **Apport retenu :** `.gitignore`, README de départ, création du dépôt privé, invitation de Catherine, suivi de l’état du dépôt.
- **Vérification :** invitations et collaborateurs vérifiés dans GitHub ; l’invitation de l’enseignant a été envoyée par Abdoulaye depuis l’interface web.
- **Correction :** aucune.

## Contributions par membre

- **Sèdrick Zahn :** première version de la proposition (besoin, technologie, tests).
- **Abdoulaye Dembele :** adaptation de la proposition pour trois membres, version n8n, veille, création du dépôt GitHub et gestion des accès.
- **Catherine Guilene Ngo Ebga :** révision de la proposition (en-tête, structure, preuve d’utilité, matériel, sources).
