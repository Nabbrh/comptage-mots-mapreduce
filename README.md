# comptage-mots-mapreduce

# Comptage de mots : Python vs pseudo-MapReduce vs Hadoop MapReduce

Comparaison de cinq approches de comptage d'occurrences de mots (Python simple, pseudo-MapReduce,
Hadoop MapReduce, Spark RDD et Spark DataFrame) sur des fichiers de 10 000 à 5 000 000 de lignes.
**Rendu principal : [`comptage_mots.ipynb`](comptage_mots.ipynb)**
(explications, code, tests, comparaisons et conclusion).

## Contenu
- `comptage_mots.ipynb` : notebook complet, exécuté
- `hadoop/` : configuration du cluster Hadoop pseudo-distribué (Docker Compose, image `apache/hadoop:3`)
- `resultats_benchmark.csv` : temps mesurés
- `comparaison_temps.png` : graphique de comparaison

## Reproduire
1. `cd hadoop && docker compose up -d`
2. Ouvrir le notebook et exécuter toutes les cellules (les fichiers de données sont générés automatiquement).
3. `docker compose down` pour arrêter le cluster.
4. PySpark : `pip install "pyspark==3.5.*"` ; Spark 3.5 nécessite Java 8, 11 ou 17 (`JAVA_HOME`).
