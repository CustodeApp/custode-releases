<div align="center">

# Custode

### Votre médiathèque personnelle.

Un serveur multimédia auto-hébergé pour organiser et regarder vos films, séries et vidéos sur tous vos écrans, chez vous comme à distance.

<br>

![Version](https://img.shields.io/badge/serveur-1.2.1-16BFB5?style=flat-square)
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

## Installation

L'installation se fait en deux temps : **le serveur** (sur la machine qui contient vos vidéos), puis **les applications** (sur les écrans où vous regardez).

<details open>
<summary><b>En bref</b></summary>

1. Installez le serveur sur votre NAS, votre PC Windows ou votre serveur Linux.
2. Ouvrez son adresse dans un navigateur, créez le compte administrateur et ajoutez vos dossiers de films et de séries.
3. Installez l'application sur vos écrans : le serveur apparaît tout seul sur le réseau de la maison.

</details>

### 1. Installer le serveur

Choisissez la machine qui contient vos vidéos et qui reste allumée.

| Votre machine | Fichier à télécharger |
|:---|:---|
| PC Windows | `custode-server-windows-amd64.exe` |
| PC ou serveur Linux (Intel/AMD) | `custode-linux-amd64.tar.gz` |
| NAS ARM 64 bits (TerraMaster, etc.) | `custode-server-linux-arm64` |

<details>
<summary><b>Windows</b></summary>

1. Créez un dossier, par exemple `C:\Custode`, et placez-y `custode-server-windows-amd64.exe`.
2. Double-cliquez sur le fichier. Si Windows affiche « Windows a protégé votre ordinateur », cliquez sur **Informations complémentaires** puis **Exécuter quand même**.
3. Si le pare-feu le demande, autorisez l'accès sur les **réseaux privés**.
4. Ouvrez **http://localhost:8096** dans votre navigateur.

La fenêtre du serveur doit rester ouverte. Pour qu'il démarre avec Windows : touches `Windows + R`, tapez `shell:startup`, puis placez dans ce dossier un raccourci vers le fichier `.exe`.

Le port 8096 est déjà pris (Emby ou Jellyfin installé) ? Créez à côté du `.exe` un fichier `custode.json` contenant `{"port": 18096}`, relancez, puis ouvrez http://localhost:18096.

</details>

<details>
<summary><b>Linux (PC ou serveur Intel/AMD)</b></summary>

```sh
tar xzf custode-linux-amd64.tar.gz
cd custode-linux-amd64
sudo mkdir -p /opt/custode
sudo cp custode-server-linux-amd64 custode.json /opt/custode/
sudo chmod +x /opt/custode/custode-server-linux-amd64

# Démarrage automatique
sudo useradd --system --no-create-home custode
sudo chown -R custode:custode /opt/custode
sudo cp custode.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now custode
```

Ouvrez ensuite **http://adresse-de-la-machine:18096**.

- L'utilisateur `custode` doit pouvoir lire vos dossiers de vidéos. Un dossier dans `/home/vous` est souvent fermé aux autres comptes : utilisez le vrai chemin du disque (par exemple `/mnt/medias/films`).
- Pare-feu actif ? Ouvrez `18096/tcp` (accès local), `18443/tcp` (accès à distance) et `18097/udp` (découverte par les applications).
- Le fichier `LISEZMOI.txt` de l'archive détaille chaque étape.

</details>

<details>
<summary><b>NAS ARM 64 bits</b></summary>

1. Activez l'accès SSH dans les réglages de votre NAS.
2. Copiez `custode-server-linux-arm64` dans un dossier du NAS, par exemple `Custode` dans votre dossier personnel.
3. Connectez-vous en SSH, allez dans ce dossier, puis :
   ```sh
   chmod +x custode-server-linux-arm64
   echo '{"port": 18096}' > custode.json
   ./custode-server-linux-arm64 -config custode.json >> custode.log 2>&1 < /dev/null &
   ```
4. Ouvrez **http://adresse-du-nas:18096**.

Les données du serveur (base, images) sont rangées dans le dossier `data` à côté du fichier. Pour un démarrage automatique, ajoutez la commande de l'étape 3 aux tâches au démarrage de votre NAS.

</details>

### 2. Premier lancement

1. À la première ouverture, créez le **compte administrateur** (nom et mot de passe).
2. Ajoutez une **médiathèque** : son type (films, séries…) et son dossier, choisi avec le sélecteur intégré.
3. Custode analyse les fichiers et récupère affiches, résumés et distribution. Comptez quelques minutes pour une grande collection.
4. Dans **Utilisateurs**, créez un compte pour chaque membre de la famille.

### 3. Installer les applications

| Écran | Fichier | Installation |
|:---|:---|:---|
| PC Windows | `Custode-Setup-x.y.z.exe` | Double-clic, puis suivez l'assistant. Si Windows affiche un avertissement : **Informations complémentaires**, puis **Exécuter quand même**. |
| Téléphone Android | `custode-x.y.z.apk` | Ouvrez le fichier sur le téléphone et autorisez l'installation d'applications inconnues quand Android le demande. |
| Android TV | `custode-tv-x.y.z.apk` | Avec l'application gratuite **Downloader** sur la TV, ouvrez le lien du fichier `custode-tv` de la dernière version, puis installez-le. |
| Navigateur | rien à installer | Ouvrez l'adresse du serveur. |

Sur le réseau de la maison, l'application trouve le serveur toute seule (**Serveurs trouvés**). Sinon, saisissez son adresse, par exemple `http://192.168.1.10:18096`.

### 4. Regarder depuis l'extérieur (VIP)

Dans l'interface web, page **Accès à distance** :

- si votre box accepte l'UPnP, le port s'ouvre tout seul ;
- sinon, ouvrez-le sur la box : port **18443** (TCP) vers l'adresse locale du serveur ;
- **Copier les informations** donne l'adresse et l'empreinte de sécurité à envoyer à vos proches.

L'administration du serveur reste accessible uniquement depuis le réseau de la maison.

### Besoin d'aide ?

- **Le serveur n'apparaît pas dans l'application** : vérifiez que les deux sont sur le même réseau et que le port `18097/udp` n'est pas bloqué, ou saisissez l'adresse à la main.
- **Un film est mal reconnu** : ouvrez sa fiche, puis **Corriger l'identification**.
- **Mot de passe administrateur oublié** : sur la page de connexion du site, depuis le réseau de la maison, choisissez **Mot de passe oublié ?** (à partir de la prochaine version).

## Feuille de route

- [x] Lecture directe en qualité originale
- [x] Applications Windows, Android et Android TV
- [x] Accès à distance et partage des informations du serveur
- [x] Profils, accueil personnalisé et contrôle parental
- [x] Interface web en français et en anglais
- [x] Mises à jour automatiques signées
- [x] Guide d'installation
- [ ] Captures d'écran
- [ ] Nouvelles langues
- [ ] Publication sur le Play Store

## Licence

Custode est un logiciel propriétaire. Les fichiers publiés ici sont destinés à l'installation et à la mise à jour de l'application.

---

<div align="center">

**Custode** · Votre collection. Votre serveur. Votre liberté.

</div>
