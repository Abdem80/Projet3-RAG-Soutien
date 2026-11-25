# Journal — Projet 3 : Évaluation d’une RAG locale comme assistant d’études en Techniques de l’informatique

Équipe : Sèdrick Zahn, Abdoulaye Dembele, Catherine Guilene Ngo Ebga

Dépôt : [Projet3-RAG-Soutien](https://github.com/Abdem80/Projet3-RAG-Soutien)

## Tâches et responsables

| Tâche | Responsable | État |
|---|---|---|
| Proposition remise dans Léa | Toute l’équipe | Fait |
| Dépôt GitHub créé, invitation envoyée à l’enseignant | Abdoulaye | Fait (enseignant et Catherine ont accepté ; invitation de Sèdrick en attente) |
| Version A (script Python, Ollama, ChromaDB) | Sèdrick | À faire |
| Version B (n8n, formulaire, webhook) | Abdoulaye | À faire |
| Corpus (nos documents d’études), jeu de questions, BM25, script de tests | Catherine | À faire |
| Fournir ses documents d’études pour le corpus | Toute l’équipe | À faire |
| Faire approuver le sujet révisé | Toute l’équipe | Fait (approuvé le 2026-11-25, notes de cours autorisées) |
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
- **Vérification :** existence du nœud Chroma de n8n vérifiée dans la documentation officielle ; proposition relue par l’équipe.
- **Correction :** aucune.

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

### 2026-11-25 — Révision du sujet après la rencontre avec l’enseignant (toute l’équipe)
- **Décision :** à la demande de l’enseignant, le corpus devient **nos propres documents d’études** (notes, énoncés, procédures, README et journaux de nos projets) au lieu d’une documentation fictive ou publique. Une RAG n’a d’intérêt que sur des documents que le modèle ne connaît pas.
- **Conséquences :** l’utilisateur devient un étudiant en Techniques de l’informatique ; le test 3 porte maintenant sur des questions reformulées (au lieu de questions en français sur des documents en anglais) ; les documents restent en local (`corpus/` exclu du dépôt) et les informations personnelles sont retirées avant l’indexation. Architecture, comparaisons et répartition inchangées.
- **Prochaine étape :** faire approuver la proposition révisée ; rassembler les documents ; suivre le `planning.md`.

### 2026-11-25 — Suivi des accès et mise à jour du journal (Abdoulaye)
- **Résultat :** collaborateurs vérifiés dans GitHub : l’enseignant (Nic365) et Catherine (Guilene-choco92) ont accepté l’invitation ; celle de Sèdrick (5edrickk), envoyée le 2026-11-10, est toujours en attente. Proposition confirmée comme remise dans Léa. Nom complet de Catherine corrigé dans le README.
- **Prochaine étape :** relancer Sèdrick pour qu’il accepte l’invitation ; ajouter une trace de veille issue des notes de version (Ollama, Chroma, n8n).

### 2026-11-25 — Utilisation d’un agent IA (Abdoulaye)
- **Objectif :** relever les incohérences du dépôt et les corriger.
- **Apport retenu :** liste des champs incomplets du README et du journal, vérification des collaborateurs et invitations par l’API GitHub.
- **Vérification :** statuts (remise Léa, relecture, identité du compte de l’enseignant) confirmés par l’équipe avant modification.
- **Correction :** aucune.

### 2026-11-25 — Approbation du sujet révisé (toute l’équipe)
- **Résultat :** l’enseignant a approuvé la révision du sujet. Il autorise l’utilisation de nos notes de cours dans le corpus.
- **Conséquence :** la mention « autorisation à confirmer » est retirée de la proposition ; les documents restent tout de même en local et sont nettoyés de toute information personnelle avant l’indexation.
- **Prochaine étape :** fournir les documents d’ici le 27 novembre ; suivre le `planning.md`.

## Contributions par membre

- **Sèdrick Zahn :** première version de la proposition (besoin, technologie, tests).
- **Abdoulaye Dembele :** adaptation de la proposition pour trois membres, version n8n, veille, création du dépôt GitHub et gestion des accès.
- **Catherine Guilene Ngo Ebga :** révision de la proposition (en-tête, structure, preuve d’utilité, matériel, sources).
