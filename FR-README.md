# ANPR-Morocco
-> Lire en [Anglais](https://github.com/Assifar-Karim/ANPR-Morocco/blob/main/README.md) <br/>
ANPR-Morocco est un système de reconnaissance automatique de plaques de voitures marocaines. Ce dépôt github contient trois versions du système qui ont été mises à jour d'une manière incrémentale afin d'obtenir de meilleurs résultats. <br/>
La première version du système se base sur des techniques classiques d'OCR afin d'extraire la plaque d'immatriculation et utilise l'outil Tesseract OCR pour lire les caractères de la plaque extraite. Afin d'augmenter la qualité de l'extraction des plaques, les techniques classiques d'OCR ont été substituées par l'algorithme YoloV4 entrainé à l'aide du Google Open Images Dataset. Finalement, il s'est avéré inefficace d'utiliser les outils Tesseract OCR ou EasyOCR pour la lecture des caractères des plaques donc comme solution à ce problème, la troisième version se base à 100% sur l'algorithme YoloV4 entrainé à l'aide d'un set de données spécifique issue du site web du MSDA de l'université Mohammed VI polytechnique.

#### Tableau des précisions moyennes des deux modèles YoloV4:

| Modèle | YoloV4 pour la détection de plaque | YoloV4 pour la détection de caractères |
|-------|-------------------------------------|----------------------------------------|
| MaP   | 90.17%                              | 81.45%                                 |

#### Comment utiliser le projet
Pour utiliser ce projet, il suffit de télécharger les poids et les fichiers de configurations des modèles du répertoire Models Data puis de télécharger le notebook `Licence_Plate_Recognizer_V3.0` et de l'ouvrir soit sur la plateforme google colaboratory ou sur une instance locale de jupyter notebook.
  Si l'instance de jupyter notebook est locale alors l'utilisateur doit installer YoloV4 et darknet avant d'utiliser le notebook. Pour effectuer cette opération, veuillez vous référer à https://github.com/AlexeyAB/darknet.<br/> 
  Si l'utilisateur décide d'utiliser google colaboratory alors les poids et les fichiers de configurations peuvent être stockés sur un google drive afin de rendre l'utilisation plus facile avec le notebook.

#### Références
 - Lien du jeu de données utilisé pour l'entrainement de la V3: https://msda.um6p.ma/msda_datasets <br/>
 - Lien de la recherche sur laquelle se base la V3 de la reconnaissance de caractères: https://arxiv.org/pdf/2104.08244.pdf
