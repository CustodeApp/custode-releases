<div align="center">

<img src="assets/custode512.png" alt="Custode" width="170">

# Custode

### Votre médiathèque personnelle.

Un serveur multimédia auto-hébergé pour organiser et regarder vos films, séries et vidéos sur tous vos écrans, chez vous comme à distance.

<br>

![Version](https://img.shields.io/badge/serveur-1.1.2-16BFB5?style=flat-square)
![Self Hosted](https://img.shields.io/badge/self--hosted-oui-16BFB5?style=flat-square)
![Platform](https://img.shields.io/badge/apps-Windows%20%7C%20Android%20%7C%20Android%20TV%20%7C%20Web-16BFB5?style=flat-square)

<br>

**Votre collection. Votre serveur. Votre liberté.**

</div>

---

## Présentation

Custode transforme un NAS, un PC Windows ou un serveur Linux en médiathèque personnelle. Il analyse vos dossiers, reconnaît les films et les séries, récupère affiches, résumés et distribution, puis diffuse vos fichiers dans leur qualité d'origine vers le navigateur, l'application Windows, le téléphone Android ou la télévision Android TV.

Vos fichiers restent chez vous : pas de compte en ligne obligatoire, pas de cloud.

## Fonctionnalités

### Médiathèque
- **Reconnaissance automatique** des films, séries, saisons et épisodes, avec affiches, fonds, résumés, genres et distribution.
- **Plusieurs médiathèques** : films, séries, dessins animés, documentaires, concerts et spectacles, fichiers personnels.
- **Navigation rapide** : tri, filtres par genre, décennie et « non vus », barre alphabétique, taille des vignettes réglable.
- **Pages acteurs** avec leur filmographie présente sur votre serveur.
- **Correction de l'identification** quand un titre a été mal reconnu.
- **Badges de qualité** (résolution, HDR, audio) et sous-titres intégrés ou externes.
- **Sélecteur de dossiers** intégré pour ajouter une médiathèque sans taper de chemin.

### Lecture
- **Lecture directe** : les fichiers sont envoyés tels quels, sans réencodage ni perte de qualité.
- **Conversion facultative** avec ffmpeg pour les appareils qui ne lisent pas un format.
- **Reprise de lecture** et rangée « Continuer à regarder ».
- **Épisode suivant** automatique, lecture aléatoire ou en boucle.
- **Liste « À voir »** et historique de visionnage.

### Comptes et profils
- **Plusieurs utilisateurs**, chacun avec sa progression, son accueil personnalisé et sa photo de profil.
- **Contrôle parental** : limite d'âge par compte, à partir des classifications des films et séries.
- **Gestion des droits** : administrateur, utilisateurs, téléchargements autorisés ou non.

### Accès à distance
- **Accès depuis l'extérieur** sans configuration compliquée : détection de l'adresse publique, saisie manuelle possible, bouton « Copier les informations » pour les partager.
- **Connexion sécurisée** avec certificat épinglé.
- **Découverte automatique** des serveurs sur le réseau local.

### Applications
- **Navigateur web** : interface complète, en français et en anglais.
- **Windows** : application native, lit tous les formats courants (MKV, HEVC…).
- **Android** : application téléphone avec la même interface.
- **Android TV** : application pensée pour la télécommande, avec menus par appui long et écran d'accueil personnalisé.

### Administration
- **Tableau de bord** et suivi de l'activité en cours.
- **Sauvegardes automatiques** de la base, chaque nuit et avant chaque migration.
- **Mises à jour automatiques et signées** : le serveur et les applications proposent la nouvelle version, l'utilisateur accepte ou refuse. Chaque fichier est vérifié par signature numérique avant installation.

### Formules
- **Gratuite** : toutes les fonctions essentielles de la médiathèque.
- **VIP** : fonctions avancées, dont le téléchargement de vidéos pour les regarder hors ligne.

## Plateformes

| Composant | Plateformes |
|:---|:---|
| Serveur | NAS (Linux ARM64, testé sur TerraMaster), Linux x86-64, Windows, Docker |
| Applications | Navigateur web, Windows, Android, Android TV |

## Téléchargement

Toutes les versions sont disponibles dans la section **[Releases](https://github.com/CustodeApp/custode-releases/releases/latest)** :

| Fichier | Pour |
|:---|:---|
| `Custode-Setup-x.y.z.exe` | Application Windows |
| `custode-x.y.z.apk` | Application Android (téléphone) |
| `custode-tv-x.y.z.apk` | Application Android TV |
| `custode-server-linux-arm64` | Serveur pour NAS ARM64 |
| `custode-linux-amd64.tar.gz` | Serveur Linux standard (avec service systemd) |
| `custode-server-windows-amd64.exe` | Serveur Windows |

Une fois installés, le serveur et les applications vous préviennent eux-mêmes des nouvelles versions.

## Feuille de route

- [x] Lecture directe en qualité originale
- [x] Applications Windows, Android et Android TV
- [x] Accès à distance et partage des informations du serveur
- [x] Profils, accueil personnalisé et contrôle parental
- [x] Interface web en français et en anglais
- [x] Mises à jour automatiques signées
- [ ] Captures d'écran et documentation d'installation
- [ ] Nouvelles langues
- [ ] Publication sur le Play Store

## Licence

Custode est un logiciel propriétaire. Les fichiers publiés ici sont destinés à l'installation et à la mise à jour de l'application.

---

<div align="center">

<img src="assets/custode512.png" width="55" alt="Custode">

**Custode** · Votre collection. Votre serveur. Votre liberté.

</div>
