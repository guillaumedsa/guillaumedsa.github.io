# Cours 1 — Anatomie d'un ordinateur

## Objectifs pédagogiques
- Comprendre les composants clés d'un ordinateur.
- Expliquer comment un programme passe du code source à l'exécution réelle.
- Distinguer mémoire vive et mémoire de stockage.
- Comprendre la différence entre processus et threads.
- Diagnostiquer les causes fréquentes de lenteur ou de crash.

## 1) CPU, RAM, stockage (HDD/SSD) : rôles et interactions
### CPU (processeur)
Le CPU exécute les instructions des programmes. Il calcule, compare, prend des décisions logiques et orchestre les tâches.

### RAM (mémoire vive)
La RAM contient les données et instructions utilisées **maintenant**. Elle est très rapide mais volatile (son contenu disparaît à l'extinction).

### Stockage (HDD/SSD)
Le stockage garde les données **durablement** (système, applications, documents). Le SSD est plus rapide qu'un HDD car il n'a pas de pièces mécaniques.

### Interaction entre les trois
1. Le programme est lu depuis le SSD/HDD.
2. Il est chargé en RAM.
3. Le CPU lit les instructions en RAM et les exécute.
4. Les résultats temporaires restent en RAM, puis peuvent être sauvegardés sur disque.

## 2) Comment un programme s'exécute : de l'électricité au code
1. Le code source (Python/JS/C/...) est interprété ou compilé.
2. L'OS charge le binaire/interpréteur et crée un processus.
3. Le CPU exécute des instructions machine (opcodes).
4. Ces instructions activent des transistors (signaux électriques 0/1).
5. Le programme interagit avec mémoire, fichiers, réseau via le système d'exploitation.

## 3) Mémoire vive vs mémoire permanente
| Critère | RAM | Stockage (SSD/HDD) |
|---|---|---|
| Persistance | Non | Oui |
| Vitesse | Très rapide | Plus lent |
| Usage | Données en cours | Données à long terme |
| Coût/Go | Plus cher | Moins cher |

## 4) Processus et threads : exécution simultanée
### Processus
Un processus est une instance d'un programme en cours d'exécution, avec son espace mémoire isolé.

### Thread
Un thread est un flux d'exécution à l'intérieur d'un processus. Plusieurs threads partagent la mémoire du processus.

### Pourquoi c'est utile
- Processus : isolation et robustesse.
- Threads : parallélisme et réactivité (ex. UI fluide + calcul en arrière-plan).

## 5) Pourquoi ton app "rame" ou "crash"
### Lenteur (rame)
- CPU saturé (calcul trop lourd, boucle inefficace).
- RAM insuffisante (swap disque, gros objets, fuite mémoire).
- I/O lente (disque saturé, réseau lent).
- Trop de processus concurrents.

### Crash
- Exception non gérée.
- Accès mémoire invalide (langages bas niveau).
- Ressources épuisées (RAM, handles, sockets).
- Dépendances cassées ou versions incompatibles.

## Exercice pratique
- Ouvrir le gestionnaire des tâches.
- Lancer un navigateur + éditeur + script Python.
- Observer CPU, mémoire, disque.
- Identifier quel processus consomme quoi et quand.

## Résumé
Un programme est un flux d'instructions exécutées par le CPU, alimenté par la RAM, et persisté sur stockage. Les performances dépendent de l'équilibre entre calcul, mémoire et I/O.
