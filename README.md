# 🕵️ Red Decoder (Tactical Edition)

> Transformez votre smartphone en outil de décryptage optique. Révélez les messages cachés invisibles à l'œil nu.

![Version](https://img.shields.io/badge/version-1.0.0-red)
![Tech](https://img.shields.io/badge/tech-HTML5%20%7C%20Canvas%20API-orange)
![License](https://img.shields.io/badge/license-MIT-blue)

## 📖 À propos

**Red Decoder** est une application web (Web App) conçue pour reproduire numériquement l'effet des filtres en plastique rouge utilisés dans les jeux de société, les escape games et les emballages secrets.

Contrairement à un simple filtre CSS, cette application utilise l'API **Canvas** pour analyser chaque pixel du flux vidéo en temps réel. Elle applique un seuil de contraste dynamique (thresholding) pour séparer l'encre cyan (message caché) du bruit rouge (camouflage).

L'interface est stylisée avec une esthétique "Tactical / Spy" pour une immersion totale.

## ✨ Fonctionnalités

* **⚡ Traitement Temps Réel :** Analyse pixel par pixel sans latence.
* **🎚️ Seuil Ajustable (Slider) :** Permet d'adapter la sensibilité du filtre selon la luminosité ambiante (indispensable pour que ça marche partout).
* **❄️ Mode Freeze (Gel) :** Fige l'image pour lire le code tranquillement sans trembler.
* **🔦 Support Flash :** Active la lampe torche du téléphone pour éclairer la carte.
* **📱 Interface Tactique :** HUD (Head-Up Display), lignes de scan et effets visuels.
* **🌐 PWA Ready :** Fonctionne directement dans le navigateur (Chrome, Safari, Firefox) sur iOS et Android.

## 🚀 Démo

Accédez à l'application ici : **[INSÉRER VOTRE LIEN NETLIFY/GITHUB PAGES ICI]**

*(Note : L'application nécessite un accès caméra et doit obligatoirement être hébergée en HTTPS).*

## 🛠️ Comment l'utiliser

1.  Ouvrez l'application sur votre smartphone.
2.  Autorisez l'accès à la caméra.
3.  Pointez votre téléphone vers une image codée (bruit rouge + texte cyan).
4.  Utilisez le **slider** en bas pour ajuster le contraste jusqu'à ce que le message apparaisse en noir sur fond rouge.
5.  Appuyez sur le **cercle central** pour figer l'image (Freeze).

## 🧪 La Science (Comment ça marche ?)

Ce projet utilise le principe de la **colorimétrie soustractive** :

1.  **Le Support :** L'image est composée d'un message en **Cyan** (Vert + Bleu) et d'un camouflage en **Rouge** sur fond Blanc.
2.  **Le Filtre Physique :** Un plastique rouge bloque les longueurs d'onde vertes et bleues.
3.  **L'Algorithme Numérique :**
    * L'algorithme parcourt chaque pixel.
    * Si le niveau de Rouge est élevé (Fond blanc ou Camouflage rouge) ➔ Le pixel devient **Rouge Vif**.
    * Si le niveau de Rouge est faible (Encre Cyan) ➔ Le pixel devient **Noir**.
    * Le **Slider** définit la limite mathématique entre "faible" et "élevé".

## 🎨 Créer vos propres énigmes (Tuto Krita/Photoshop)

Pour que l'application fonctionne, vous devez créer vos images selon ces règles colorimétriques précises :

1.  **Le Message (Calque 1) :**
    * Couleur : **Cyan Pur** (`#00FFFF` ou RGB: 0, 255, 255).
    * Forme : Texte ou schéma.
2.  **Le Camouflage (Calque 2 - Au-dessus) :**
    * Couleur : **Rouge Pur** (`#FF0000` ou RGB: 255, 0, 0).
    * Forme : Bruit aléatoire, lignes entrecroisées ou formes géométriques.
    * *Astuce :* Le camouflage doit être dense mais laisser voir le blanc par endroits.
3.  **Le Fond :** Blanc (`#FFFFFF`).

## 💻 Installation Locale

Si vous souhaitez modifier le code :

1.  Clonez ce dépôt.
2.  Le projet consiste en un fichier unique `index.html`.
3.  Pour tester sur mobile, vous devez servir le fichier via un serveur local **sécurisé (HTTPS)** ou via votre IP locale.
    * *VsCode Live Server :* Clic droit sur `index.html` > "Open with Live Server".

## 🤝 Contribution

Les contributions sont les bienvenues ! N'hésitez pas à ouvrir une *Issue* ou à proposer une *Pull Request* pour améliorer l'algorithme de détection ou l'interface.

## 📄 Licence

Distribué sous la licence MIT. Voir le fichier `LICENSE` pour plus d'informations.

---

*Développé avec passion pour les amateurs d'énigmes et d'espionnage.* 🕵️‍♂️
