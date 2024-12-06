# Vizua

[Précédement Wave3D](https://jejed8.github.io/wave3d/)

## Concept

L'expérience est une installation immersive où l'utilisateur joue sur un clavier MIDI et voit des visuels dynamiques se déployer autour de lui en réalité virtuelle. Chaque note déclenche des animations spectaculaires qui réagissent en temps réel, créant un spectacle audiovisuel captivant et interactif.

<img width="1710" alt="Screenshot 2024-11-04 at 3 59 05 PM" src="https://github.com/user-attachments/assets/0d1631bd-a0b8-48c1-8a90-9e10aeeb605e">

### Inspiration

Le projet s'inspire des "Music Visualizers", populaires sur les lecteurs de médias audio des appareils électroniques, particulièrement entre les années 2000 et le début des années 2010.

L'idée est de moderniser les visualiseurs de musique en intégrant la réalité virtuelle, offrant ainsi une expérience plus immersive pour contempler un visualiseur audio.

#### Exemples :

- [Apple iTunes Classic Visualizer](https://www.youtube.com/watch?v=i4JbAm7awCc&list=PLPF1dVJ5LqyQi0A6NYr3UD-zhF91ySM_2&index=2)
- [Xbox 360 music visualizer](https://www.youtube.com/watch?v=tjI4dYWsFbM)

## Scénario interactif

```mermaid
flowchart TD
    n5["début"] -- choix --> n4["Mode performance"] & n3["Mode libre"]
    n4 --> n6["Début chrono 60s"]
    n3 --> n7["Manipulation de clavier"]
    n6 --> n8["Manipulation de clavier"]
    n7 --> n9["Visuel ondes jouées"]
    n8 --> n10["Visuel ondes jouées"]
    n9 --> n11["terminer"]
    n10 --> n12["fin chrono"]
    n11 --> n14["retourner aux choix"]
    n11 -- retour mode de sélection --> n5
    n12 --> n15["terminer"] & n16["recommencer"]
    n16 --> n6
    n15 --> n17["écouter performance"] & n14
    n14 -- moins de 2min --> n5
    n17 --> n16
```

## Devis

### Location / emprunt

- Caque VR (oculus)
- Ordinateur (Étant capable de supporter les requis logiciel)
- Haut-Parleur Surround x4
- Console de son
- Clavier MIDI
- Chariot avec roulette pour la mobilité de l'installation
- Écran (moniteur) pour l'affichage de la vue en VR

## Plantation

Comme le côté visuel de l'expérience se situe en réalité virtuelle, cela permet à l'installation d'être facilement déplacer.

#### Vue de coté

![Desktop - 5](https://github.com/user-attachments/assets/d22e469b-8029-4118-9d44-ba18b9e93709)

#### Vue de dessus

![Desktop - 4](https://github.com/user-attachments/assets/6cbf4efd-efd2-457d-ad18-af37fd2828d1)

## Composantes

**Ordinateur :**

- Gère l'intégratation des autres composantes,
- Reçois les données envoyées par le clavier MIDI,
- Traite et analyse le son,
- Opère les visuel pour le casque VR,
- Envoie le son vers les Hauts-parleurs,
  -Envoie les données vidéo au moniteur,

**Clavier MIDI :**

- Permet à l'interacteur d'intéragir avec l'installation,
- Envoie les données MIDI à l'ordinateur,

**Moniteur :**

- Reçoit les données vidéo de l'ordinateur,
- Permet aux spectateur de participer à l'installation avec une recopie d'écran du casque VR,

**Console de son :**

- Permet d'envoyer les données sonore vers les hauts-parleurs,
- Gère le volume,

**Haut-parleurs :**

- Permet le son à l'installation,

**Chariot :**

- Aide à la mobilité de l'installation,
- Abrites les composantes (ordinateur, console de son, moniteur),

**Casque VR :**

- Environement visuel de l'installation,
- Permet à l'interacteur d'intéragir avec l'installation,

## Synoptique

### Schéma

<img width="1230" alt="Screenshot 2024-11-24 at 4 39 27 PM" src="https://github.com/user-attachments/assets/904b8e23-26bb-4b0a-8103-822b99ce38c6">

### Description de la synoptique

#### Entrée

- **Clavier MIDI** : Envoie des signaux MIDI au DAW.
- **DAW (Digital Audio Workstation)** :
  - Reçoit le signal MIDI.
  - Modifie les sons (EQ, effets, etc.).
  - Envoie les données audio/MIDI à TouchDesigner.

#### Création Visuelle

- **TouchDesigner** :
  - Reçoit les données MIDI/audio.
  - Crée des visuels dynamiques basés sur les notes jouées.
  - Intègre des éléments 3D et de l'instancing pour des visuels complexes.

#### Rendu VR

- **OpenVR CHOP/TOP** :
  - Configure l'environnement de rendu stéréoscopique.
  - Relie les mouvements du casque VR et des contrôleurs à la caméra virtuelle et aux interactions visuelles.
- **Scène 3D** :
  - Adapte l'espace visuel pour l'immersion totale.
  - Synchronise les éléments visuels avec les mouvements et les interactions de l'utilisateur.

#### Interactions et Retours

- **Contrôleurs VR** :
  - Permettent à l'utilisateur de manipuler et interagir avec les visuels.
  - Envoient des signaux à TouchDesigner pour déclencher des animations ou modifier les éléments visuels.
- **Feedback visuel et haptique** :
  - Affiche des réponses visuelles et, si possible, des retours haptiques via les contrôleurs.

#### Résumé du Flux

**Clavier MIDI ➔ DAW ➔ Analyse par PyTorch ➔ Transmission OSC/WebSocket ➔ TouchDesigner ➔ Rendu VR (OpenVR).**

**Interaction utilisateur (contrôleurs) ➔ TouchDesigner ➔ Feedback en temps réel.**

### Liste des logiciels

| Logiciel            | Description Technique                                                                           |
| ------------------- | ----------------------------------------------------------------------------------------------- |
| TouchDesigner       | Génère des visuels interactifs et les rend en temps réel dans un environnement VR.              |
| DAW (Ableton/Logic) | Capture, modifie et traite les signaux MIDI/audio pour enrichir l'expérience sonore.            |
| OpenVR              | Permet l'intégration et le rendu stéréoscopique de la scène VR et gère le suivi des mouvements. |
| Oculus Software     | Établit la connexion et le suivi du casque Oculus avec le PC pour une immersion VR optimale.    |

## Intégration optionelle

### Analyse du son par l'intelligence artificielle (AI)

Cette intégration au projet permettrait une analyse sonore plus approfondie et poussée grâce à l'utilisation de frameworks d'intelligence artificielle. Des outils comme PyTorch seraient utilisés pour créer ou adapter des frameworks existants. Les données résultant de cette analyse seraient transmises via des protocoles de communication tels qu'OSC ou WebSocket vers TouchDesigner. Cette approche donnerait naissance à des visuels plus uniques et captivants.

#### Analyse AI

- **Framework PyTorch** :
  - Reçoit le signal audio/MIDI modifié du DAW.
  - Analyse le son (détection de motifs, classification d'émotions).
  - Envoie les résultats d'analyse à TouchDesigner via OSC/WebSocket.

#### Communication

- **OSC / WebSocket** :
  - Transporte les données d'analyse de PyTorch vers TouchDesigner en temps réel.
  - Synchronise les échanges de données entre le DAW, PyTorch et TouchDesigner.

#### Synoptique avec cette intégration

<img width="1219" alt="Screenshot 2024-11-24 at 4 44 58 PM" src="https://github.com/user-attachments/assets/e11f6d17-cf89-4cad-9446-73d135d1441a">
