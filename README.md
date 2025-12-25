# Atelier 4 : Deep Learning - Modèles Génératifs (AE, VAE, GANs)

**Université Abdelmalek Essaadi** **Faculté des Sciences et Techniques de Tanger** **Master :** MBD (Big Data)  
**Module :** Deep Learning  
**Professeur :** Pr. ELAACHAK LOTFI  

---

## 📋 Description
Ce projet s'inscrit dans le cadre du quatrième laboratoire de Deep Learning. L'objectif principal est de se familiariser avec la bibliothèque **PyTorch** en implémentant et en entraînant différentes architectures de réseaux de neurones profonds pour l'intelligence artificielle générative.

Le laboratoire est divisé en deux parties principales :
1.  **Auto-encodeurs (AE) et Auto-encodeurs Variationnels (VAE)** appliqués au dataset MNIST.
2.  **Réseaux Antagonistes Génératifs (GANs)** appliqués à la génération d'art abstrait.

## 🛠️ Technologies utilisées
* **Langage :** Python
* **Bibliothèques :** PyTorch, Torchvision, Matplotlib, Numpy, Scikit-learn
* **Environnement :**  Google Colab

---

## 1️⃣ Partie 1 : AE et VAE (MNIST)

### 🎯 Objectifs
* Mettre en place une architecture d'Auto-encodeur (AE) standard.
* Mettre en place une architecture d'Auto-encodeur Variationnel (VAE).
* Entraîner les modèles sur le dataset **MNIST** (chiffres manuscrits).
* Comparer les performances (Perte de reconstruction, Divergence KL) et visualiser l'espace latent.

### 🧠 Architectures
* **Auto-Encoder (AE) :**
    * *Encoder* : Réduit la dimension de l'image (784 pixels) vers un espace latent compressé.
    * *Decoder* : Reconstruit l'image à partir du vecteur latent.
    * *Loss* : MSELoss (Mean Squared Error).
* **Variational Auto-Encoder (VAE) :**
    * Introduit une composante probabiliste dans l'espace latent (moyenne `mu` et variance `logvar`).
    * Utilise le "reparameterization trick" pour permettre la rétropropagation.
    * *Loss* : Reconstruction Loss (BCE) + KL Divergence.

### 📊 Résultats
* Comparaison des courbes de perte entre AE et VAE.
* Visualisation de la reconstruction des chiffres.
* Analyse de l'espace latent (t-SNE ou scatter plot) montrant la séparation des classes de chiffres.

---

## 2️⃣ Partie 2 : GANs (Abstract Art Gallery)

### 🎯 Objectifs
* Utiliser des GANs pour générer de nouvelles images artistiques.
* Dataset utilisé : [Abstract Art Gallery](https://www.kaggle.com/datasets/bryanb/abstract-art-gallery).

### 🧠 Architecture GAN
* **Générateur (Generator) :**
    * Prend en entrée un vecteur de bruit aléatoire (z_dim=100).
    * Utilise des couches de **ConvTranspose2d** (déconvolution) pour générer une image RGB 64x64.
    * Activation : ReLU et Tanh pour la sortie.
* **Discriminateur (Discriminator) :**
    * Prend en entrée une image (réelle ou générée).
    * Utilise des couches de **Conv2d** pour classer l'image comme "Réelle" ou "Fausse".
    * Activation : LeakyReLU et Sigmoid pour la sortie.

### ⚙️ Entraînement
* **Optimizers :** Adam (lr=0.0002, betas=(0.5, 0.999)).
* **Fonction de coût :** BCELoss (Binary Cross Entropy).
* **Stratégie :** Entraînement alterné où le générateur essaie de tromper le discriminateur, et le discriminateur essaie de ne pas se faire tromper.

---

## 🚀 Comment exécuter
1.  Cloner ce dépôt :
    ```bash
    git clone [https://github.com/votre-username/votre-repo.git](https://github.com/votre-username/votre-repo.git)
    ```
2.  Ouvrir les notebooks (`atelier-4-partie-1.ipynb` et `atelier-4-partie-2.ipynb`) dans Jupyter, Kaggle ou Google Colab.
3.  S'assurer que l'accélération GPU est activée pour un entraînement plus rapide.
4.  Exécuter les cellules séquentiellement.

## 📝 Auteur
Travail réalisé par **AZARIZ ANAS** 
