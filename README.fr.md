# DRVCAM

[English](README.md) | [Español](README.es.md) | [العربية](README.ar.md) | [Deutsch](README.de.md) | **Français** | [Italiano](README.it.md) | [日本語](README.ja.md) | [简体中文](README.zh-hans.md)

**Une caméra virtuelle pour appareils Android rootés compatibles.** Choisissez une photo ou une vidéo et présentez-la comme flux caméra des applications que vous sélectionnez, avec lecture en direct et contrôles de cadrage.

[![Dernière version](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=derni%C3%A8re%20version)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![Plateforme](https://img.shields.io/badge/plateforme-Android-3DDC84)](#prérequis)
[![Root requis](https://img.shields.io/badge/root-requis-critical)](#prérequis)
[![Licence](https://img.shields.io/badge/licence-propriétaire-lightgrey)](#licence)

> **Version alpha.** DRVCAM est en développement actif et le comportement peut varier selon l'appareil.

Ce dépôt est la **fiche du module** pour DRVCAM. Il ne contient aucun code source. Page produit, tarifs et documentation complète : **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**.

## Sommaire

- [Captures d'écran](#captures-décran)
- [Fonctionnement](#fonctionnement)
- [Prérequis](#prérequis)
- [Télécharger](#télécharger)
- [Installer](#installer)
- [Formule gratuite et formules payantes](#formule-gratuite-et-formules-payantes)
- [Confidentialité en bref](#confidentialité-en-bref)
- [Questions fréquentes](#questions-fréquentes)
- [Avis de non-responsabilité](#avis-de-non-responsabilité)
- [Licence](#licence)
- [Assistance](#assistance)
- [Journal des modifications](#journal-des-modifications)

## Captures d'écran

| Accueil | Contrôleur flottant |
|---|---|
| ![Écran d'accueil de DRVCAM : aperçu de la source en direct, sélection de l'application cible, source de média et commandes rapides](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-home.webp) | ![Contrôleur flottant superposé à une application caméra](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-controller.webp) |

| Éditeur de média | Presets |
|---|---|
| ![Éditeur de média : lecture, boucle, zoom et rotation](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-editor.webp) | ![Onglet presets de la bibliothèque](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-presets.webp) |

## Fonctionnement

- Utilise une photo ou une vidéo que vous importez comme source caméra d'une application de votre choix, là où l'appareil, l'API caméra et l'application le permettent.
- Vous laisse choisir les applications cibles et ajuster lecture, rotation, effet miroir, zoom et cadrage. Une source Main et deux presets peuvent être enregistrés puis permutés.
- Vous laisse faire basculer une cible configurée entre le flux virtuel et la caméra physique réelle. Certaines applications doivent rouvrir leur caméra avant qu'un changement apparaisse ; DRVCAM vous le signale le cas échéant.
- Propose un contrôleur flottant optionnel qui reste au-dessus de l'application utilisée (nécessite la permission de superposition).
- Laisse le microphone réel inchangé — DRVCAM ne remplace ni ne traite l'audio.

## Prérequis

- Un appareil Android rooté (Magisk ou KernelSU), Android 9 ou ultérieur. Le remplacement de caméra nécessite le root ; sans lui, l'application s'ouvre mais le remplacement n'est pas disponible.
- Un framework de la famille Xposed compatible avec libxposed API 102 — DRVCAM est testé avec [Vector](https://github.com/JingMatrix/Vector) (le successeur de LSPosed), un framework de la famille LSPosed basé sur Zygisk. Un framework sans prise en charge de l'API 102 ne chargera pas le module.
- Une capacité de décodage et graphique suffisante pour le média et l'application choisis.

## Télécharger

Cette fiche propose le **build téléphone pour Android 12 et versions ultérieures** (arm64). Les autres builds — Android 9 à 11 et les images pour émulateur — se trouvent sur **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**, avec un sélecteur qui vous recommande celui qui convient à votre appareil.

Chaque version ici indique son SHA-256 dans les notes de version — vérifiez votre téléchargement avant d'installer.

## Installer

1. Téléchargez et installez l'APK correspondant à votre version d'Android et à votre type d'appareil (ci-dessus).
2. Ouvrez le gestionnaire de votre framework et activez DRVCAM, puis redémarrez si demandé.
3. Ouvrez DRVCAM et accordez le root lorsque c'est demandé. DRVCAM gère la portée des applications choisies directement depuis sa propre interface — rien à ajouter manuellement dans le gestionnaire du framework.
4. Connectez-vous, ou choisissez **Essayer gratuitement** (voir [Formule gratuite et formules payantes](#formule-gratuite-et-formules-payantes)).
5. Importez une photo ou une vidéo dans la Bibliothèque, sélectionnez-la, choisissez une application cible, puis appuyez sur **Enable**. Ouvrez vous-même la caméra de l'application cible.
6. Vérifiez le résultat dans l'application cible. L'aperçu propre à DRVCAM aide à choisir le média ; il ne prouve pas à lui seul que l'application cible a reçu le flux.

**Disable** retire à nouveau la portée de DRVCAM sur la cible.

## Formule gratuite et formules payantes

DRVCAM nécessite un compte DRVCAM et une connexion internet pour la connexion, l'enregistrement de l'appareil et le renouvellement. Une fois connectée, l'application peut continuer de fonctionner hors ligne pendant une durée limitée.

- **Essayer gratuitement** (sans frais) : sources d'image, une application cible.
- **Formules payantes** : sources vidéo, plusieurs applications cibles, le contrôleur flottant et le changement de Camera Source.

Formules, limites d'appareils et tarifs actuels : **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**.

## Confidentialité en bref

- Votre média reste sur votre appareil pour le fonctionnement de la caméra — le service de compte n'a pas besoin de votre média ni des images caméra pour vous connecter.
- Le service de compte traite les données de compte, d'appareil et d'abonnement pour que la connexion et la licence fonctionnent. Les diagnostics ne sont envoyés que si vous le demandez.
- Une application cible peut toujours enregistrer, analyser ou transmettre ce que montre sa caméra ; les pratiques de confidentialité propres à cette application s'appliquent.
- Politique complète : [droidrooter.com/privacy](https://www.droidrooter.com/privacy).

## Questions fréquentes

**Le root est-il nécessaire ?**
Oui. Le remplacement de caméra passe par un hook au niveau système qui nécessite le root et un framework compatible de la famille Xposed.

**Fonctionnera-t-il sur mon appareil ?**
Seules les combinaisons vérifiées sont listées sur la page produit. Appareil, micrologiciel et application caméra varient trop pour garantir la compatibilité à l'avance.

**Puis-je l'utiliser sans me connecter ?**
Oui, avec **Essayer gratuitement** (sources d'image, une application cible). La vidéo et les autres fonctions nécessitent une formule payante.

**J'ai perdu mon mot de passe, que faire ?**
La récupération de compte est manuelle pour l'instant ; utilisez les liens d'[Assistance](#assistance) ci-dessous.

**Où est le code source ?**
Il n'est pas publié ici. Ce dépôt est une fiche de module qui ne distribue que des binaires de version signés.

## Avis de non-responsabilité

DRVCAM est un logiciel alpha, fourni « tel quel » sans garantie d'aucune sorte. Rooter un appareil et installer un framework sans système sont des actions que vous entreprenez à vos propres risques, pouvant affecter la garantie ou la stabilité de votre appareil.

Vous êtes seul responsable du média que vous utilisez, des applications avec lesquelles vous utilisez DRVCAM, et du respect des lois et conditions qui vous sont applicables. Le développeur n'est pas responsable d'un usage illégal, non autorisé ou autrement inapproprié de ce logiciel.

## Licence

DRVCAM est un logiciel propriétaire à code source fermé. Aucune licence de copie, modification, ingénierie inverse ou redistribution de l'application n'est accordée. Le téléchargement et l'installation sont régis par les [Conditions d'utilisation](https://www.droidrooter.com/terms) publiées sur le site du produit.

## Assistance

- Telegram : [@DroidRooter](https://t.me/DroidRooter)
- Formulaire de contact du site : [droidrooter.com/contact](https://www.droidrooter.com/contact)

## Journal des modifications

Consultez les notes de chaque [version](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases) pour connaître les changements.
