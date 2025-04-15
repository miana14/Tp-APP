# Mariana Loureiro Dias

# TP-APP

Une application Flutter pour le suivi et l’enregistrement d’exercices physiques.

## Description

Cette application permet aux utilisateurs d’enregistrer et de suivre leurs activités sportives. Elle propose notamment :

- **Test de Léger** : Mesure du niveau de forme physique à l’aide des données de l’accéléromètre.
- **Sauvegarde des données** : Enregistrement local des résultats, avec possibilité de synchronisation en ligne.
- **Historique** : Visualisation des exercices réalisés.
- **Authentification** : Écran de connexion (si activé).

## Identifiants de test

Pour tester l’application, vous pouvez utiliser le compte suivant :

- **Adresse mail** : `test@test.com`
- **Mot de passe** : `test123`

## Architecture du projet

Le projet est organisé de façon modulaire :

- **`lib/models`** : Modèles de données (ex : `exercice.dart`)
- **`lib/services`** : Services (API, base de données, capteurs)
- **`lib/screens`** : Écrans de l’application (`test_leger_screen.dart`, `home_screen.dart`, etc.)
- **`lib/widgets`** : Widgets personnalisés
- **`lib/routes`** : Gestion des routes/navigation

## Fonctionnalités principales

- **Intégration de l’accéléromètre** : Le fichier `test_leger_screen.dart` utilise `sensor_service.dart` pour mesurer la vitesse et la distance parcourue en temps réel.
- **Sauvegarde locale** : Les résultats sont stockés localement via SQLite (`database_service.dart`).
- **Synchronisation en ligne** : Envoi des données vers une API distante (`api_service.dart`).
- **Gestion de la connectivité** : Vérification de la connexion internet avant l’envoi des données.

## Prise en main

1. **Cloner le dépôt :**
    ```
    git clone https://github.com/miana14/Tp-APP.git
    ```

2. **Installer les dépendances :**
    ```
    flutter pub get
    ```

3. **Lancer l’application :**
    ```
    flutter run
    ```
## Tester l’accéléromètre dans l’émulateur

Pour simuler des mouvements et tester l’accéléromètre dans l’application :

1. **Ouvre le menu "Extended controls"**  
   (Cliquer sur les trois petits points `...` à droite de l’émulateur Android Studio)

2. **Aller dans l’onglet "Sensors"**

3. **Dans la section "Accelerometer"**, modifier les valeurs X, Y ou Z 

## Dépendances principales

- `flutter_localizations` : Support de la localisation
- `connectivity_plus` : Vérification de la connexion réseau
- `sensors_plus` : Accès aux capteurs (accéléromètre)

---
