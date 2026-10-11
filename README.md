# TP Deep Learning : outils pour le deep learning

Ce notebook reprend **tous les codes du CM3 « Outils pour le deep learning »** (pages 30 à 77 du
cours), dans l'ordre des diapositives, avec des commentaires en français. Il compare NumPy,
PyTorch, TensorFlow 1.x, TensorFlow 2.x et Keras sur les mêmes exemples. Le numéro de page du
cours est rappelé à chaque section. Les compléments qui ne figurent pas dans le cours sont signalés
par la mention *Ajout*.

## Contenu

| Partie | Pages | Thème |
|---|---|---|
| 1. Graphe de calcul et gradients | 30–35 | Le graphe $c = \sum (x \odot y + z)$ : gradients calculés à la main avec NumPy, puis automatiquement avec TensorFlow et PyTorch, sur CPU et sur GPU |
| 2. PyTorch | 36–46 | Tenseurs, gradients à la main, `autograd`, fonctions autograd personnalisées (`my_relu`), `nn`, optimiseurs (Adam), modules personnalisés (`nn.Module`, `ParallelBlock`) |
| 3. Exemple complet : FashionMNIST | 47–51 | Chargement des données, définition du modèle, fonctions d'entraînement et de test, boucle sur les époques, sauvegarde, rechargement et prédiction |
| 4. Modèles pré-entraînés | 52 | `torchvision.models` pré-entraînés sur ImageNet (`weights="DEFAULT"` remplace `pretrained=True`) |
| 5. TensorFlow, TensorBoard et Keras | 53–60 | TensorFlow avant et après la version 2.0 (`tf.GradientTape`, mode *eager*), journaux TensorBoard, modèle séquentiel Keras |
| 6. Calcul distribué et choix du framework | 61–64 | Résumé : modèle distribué ou données distribuées, comparaison des frameworks |
| 7. TensorFlow 1.x pas à pas | 66–77 | Réseau à deux couches amélioré étape par étape : placeholders, `Variable`, nœud `updates`, optimiseur, perte prédéfinie, `tf.layers.dense` et initialisation de Xavier |
| Bilan | | Tableau comparatif NumPy / TF 1.x / TF 2.x / Keras / PyTorch : type de graphe, calcul des gradients, GPU |

## Installation et utilisation

```bash
git clone https://github.com/Otodji/tp-deep-learning.git
cd tp-deep-learning
pip install -r requirements.txt
jupyter notebook TP_Deep_Learning.ipynb
```

- **GPU facultatif** : les cellules GPU vérifient d'abord qu'une carte est disponible, et
  repassent sur le CPU sinon.
- **FashionMNIST** est téléchargé automatiquement par `torchvision` à la première exécution
  (environ 30 Mo).
- **Code TensorFlow 1.x** (parties 1 et 7) : il tourne avec TensorFlow 2 grâce à
  `tf.compat.v1`, sans installation supplémentaire.
- Le notebook est enregistré presque sans résultats d'exécution. Lance *Run All* pour les
  obtenir. L'entraînement sur FashionMNIST prend quelques minutes sur CPU.

## Auteur

[OTODJI Théophile](https://github.com/Otodji), à partir des codes du cours de deep learning du M2.
