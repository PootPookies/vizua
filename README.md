# Vizua

[Précédement Wave3D](https://jejed8.github.io/wave3d/)

## Concept

L'expérience est une installation immersive où l'utilisateur joue sur un clavier MIDI et voit des visuels dynamiques se déployer autour de lui en réalité virtuelle. Chaque note déclenche des animations spectaculaires qui réagissent en temps réel, créant un spectacle audiovisuel captivant et interactif.

<img width="1710" alt="Screenshot 2024-11-04 at 3 59 05 PM" src="https://github.com/user-attachments/assets/0d1631bd-a0b8-48c1-8a90-9e10aeeb605e">

<!-- ![vizua](https://github.com/user-attachments/assets/8b64af8a-739f-4319-8b70-d7ac6e8ca225) -->

### Inspiration

Le projet s'inspire des "Music Visualizers", populaires sur les lecteurs de médias audio des appareils électroniques, particulièrement entre les années 2000 et le début des années 2010.

L'idée est de moderniser les visualiseurs de musique en intégrant la réalité virtuelle, offrant ainsi une expérience plus immersive pour contempler un visualiseur audio.

#### Exemples :

- [Apple iTunes Classic Visualizer](https://www.youtube.com/watch?v=i4JbAm7awCc&list=PLPF1dVJ5LqyQi0A6NYr3UD-zhF91ySM_2&index=2)
- [Xbox 360 music visualizer](https://www.youtube.com/watch?v=tjI4dYWsFbM)
- [Folding Space - Generative Modular Ambient](https://www.youtube.com/watch?v=6JeZR13dLLI)

## Moodboard
![moodboard_visuel](https://github.com/user-attachments/assets/e66e0001-dc04-472f-a116-b22a92569dc7)


## Scénario interactif

<img height="500px" src="https://github.com/user-attachments/assets/8c6d00b4-db89-41f6-b4a0-23018423e6c2" alt="Interaction"
>
## Gestion d'équipe 

![diagramme_taches](https://github.com/user-attachments/assets/50cee5a7-040e-40d2-9885-c0ad2a641291)

## Échéancier

<img width="1127" alt="planification_temps" src="https://github.com/user-attachments/assets/cea34dab-4069-49c9-82e1-824088a112db" />

---

## Devis

**Devis pour l'installation immersive Vizua**

| **Équipement**                        | **Description**                                                                       | **Prix estimé** |
| ------------------------------------- | ------------------------------------------------------------------------------------- | --------------- |
| Matériel pour l'installation physique | Supports et fixations pour maintenir l'équipement en place et faciliter l'agencement. | 135,00 CAD      |

**Équipement fourni par l'école pour l'installation immersive Vizua**

| **Équipement**                        | **Description**                                                                          |
| ------------------------------------- | ---------------------------------------------------------------------------------------- |
| Haut-parleurs surround x4             | Système de son surround pour une expérience immersive complète.                          |
| Console de son                        | Console permettant de gérer et diriger le son vers les haut-parleurs.                    |
| Écran (Moniteur)                      | Écran pour afficher la vue en VR pour les spectateurs.                                   |
| Chariot avec roulette                 | Chariot pour la mobilité de l'installation et pour héberger les équipements.             |
| Câbles et connecteurs divers          | Câbles HDMI, USB, audio, alimentation et autres connecteurs nécessaires pour le montage. |
| Support pour Casque VR                | Support pour ranger et organiser le casque VR de manière pratique.                       |
| Matériel pour l'installation physique | Supports et fixations pour maintenir l'équipement en place et faciliter l'agencement.    |

---

### Location / emprunt

- 🎹 Clavier MIDI
- 🎛️ Console audio (facultative si tout est géré par l'ordinateur).
- 🔊 Haut-parleurs (minimum 4 pour un son surround).
- 💻 Ordinateur
- 🥽 Casque VR
- 🖥️ Moniteur externe (pour le public).
- 🖥️ DAW: Ableton Live ou Logic Pro.
- 🔧 PlugData ou PureData : Traitement MIDI/audio.
- 🌀 TouchDesigner : Visualisations interactives.
- 🔗 Oculus Software : Gestion du casque VR.

## Plantation

Comme le côté visuel de l'expérience se situe en réalité virtuelle, cela permet à l'installation d'être facilement déplacer.

## Zone de plantation

![gestion_emplacement](https://github.com/user-attachments/assets/177daa44-8fdc-40c9-82bb-6dd5230f785f)

#### Vue de coté

![Desktop - 5](https://github.com/user-attachments/assets/d22e469b-8029-4118-9d44-ba18b9e93709)

#### Vue de dessus

![Desktop - 4](https://github.com/user-attachments/assets/6cbf4efd-efd2-457d-ad18-af37fd2828d1)

---

## Composantes

**Clavier MIDI:**

- C’est l’interface principale pour l’utilisateur.
- Permet de jouer des notes et des accords qui génèrent à la fois des sons (via le DAW) et des animations visuelles (via PlugData/PureData et TouchDesigner).
- Envoie des signaux MIDI à l’ordinateur pour traitement.

**Haut-parleurs :**

- Diffusent le son produit par le DAW pour créer une expérience immersive.

**Console de son :**

- Permet d'envoyer les données sonore vers les hauts-parleurs,
- Gère le volume,

**Haut-parleurs :**

- Permet le son à l'installation,

  **Supports pour haut-parleurs**

  -Placés stratégiquement pour offrir une diffusion sonore équilibrée.

**Ordinateur :**

- C’est le cœur de l’installation.
- Gère tous les logiciels et traite les signaux MIDI/audio.
- Génère les visuels dans TouchDesigner en réponse aux données MIDI.
- Transmet les visuels au casque VR et les sons aux haut-parleurs.

**Moniteur :**

- Reçoit les données vidéo de l'ordinateur,
- Permet aux spectateur de participer à l'installation avec une recopie d'écran du casque VR,

**Casque VR :**

- Permet une immersion totale en affichant les visuels générés par TouchDesigner dans un environnement virtuel.
- Suit les mouvements de la tête de l’utilisateur pour ajuster les perspectives visuelles.

**Chariot :**

- Aide à la mobilité de l'installation,
- Abrites les composantes (ordinateur, console de son, moniteur),

**Câblage :**

Connecte toutes les composantes entre elles (clavier, casque, haut-parleurs).
Assure une alimentation stable.

---

## Synoptique

### Schéma

<img width="1123" alt="mermaid" src="https://github.com/user-attachments/assets/c9f545fd-83d7-4427-95d6-e34df8259d4b">

---

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

**Clavier MIDI ➔ DAW ➔ Transmission OSC/WebSocket ➔ TouchDesigner ➔ Rendu VR (OpenVR).**

**Interaction utilisateur (contrôleurs) ➔ TouchDesigner ➔ Feedback en temps réel.**

### Liste des logiciels

| Logiciel                                     | Description Technique                                                                            |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| TouchDesigner                                | Génère des visuels interactifs et les rend en temps réel dans un environnement VR.               |
| DAW (Ableton/Logic)                          | Capture, modifie et traite les signaux MIDI/audio pour enrichir l'expérience sonore.             |
| PlugData ou PureData                         | Traduit les signaux MIDI/audio en paramètres visuels exploitables par TouchDesigner.             |
| OpenVR                                       | Permet l'intégration et le rendu stéréoscopique de la scène VR et gère le suivi des mouvements.  |
| Oculus Software                              | Établit la connexion et le suivi du casque Oculus avec le PC pour une immersion VR optimale.     |
| OSC (Open Sound Control)                     | Transmet les données MIDI/audio entre le DAW, PlugData/PureData, et TouchDesigner en temps réel. |
| MIDI Monitor (macOS) ou MIDI-OX (Windows)    | Visualise les signaux MIDI pour vérifier la configuration et détecter les erreurs.               |
| Virtual Audio Cable (ou équivalent)          | Permet de router l’audio entre différents logiciels si nécessaire.                               |
| Soundflower (macOS) ou Voicemeeter (Windows) | Gère les flux audio pour un monitoring précis et avancé.                                         |
---

## Produit Minimum Viable

### Interactivité

L’interacteur doit être en mesure d’entendre les notes qu’il joue au clavier et de voir un visuel apparaître dans le casque.

### Visuel

Afin que le visuel soit intéressant, il doit au moins y avoir des animations cohérentes et en lien avec les sons joués par l’interacteur.

### Matériel

Le matériel suivant est nécessaire pour que l’installation soit au minimum viable :

1. Casque de réalité virtuelle
2. Haut-parleurs stéréo
3. Clavier MIDI
4. Ordinateur avec les bons requis logiciels
5. Câblage requis

### Sonore

L’interacteur doit être en mesure d’entendre les sons qu’il joue à partir du clavier MIDI.

---
## Évaluation des risques du projet

### R1 : Les animations visuelles pourraient souffrir de ralentissements ou de latence lors de l’interaction avec le clavier MIDI. 
**Priorité : Élevée**  
**Solution** : Optimiser les performances dans TouchDesigner et effectuer des tests rigoureux pour garantir une fluidité dans le traitement des données MIDI et l'affichage des visuels en temps réel.

### R2 : Les haut-parleurs risquent de produire des décalages sonores ou des distorsions pendant les tests interactifs.  
**Priorité : Moyenne**  
**Solution** : Effectuer des tests de calibrage audio et ajuster les présets sonores avant l’intégration finale.

### R3 : Le casque VR pourrait provoquer des problèmes de compatibilité ou d’affichage non prévus.  
**Priorité : Élevée**  
**Solution** : Tester le matériel sur plusieurs systèmes et configurations d’ordinateur pour identifier les problèmes potentiels.

### R4 : Risque de perte de synchronisation entre les éléments visuels et sonores lors de changements dynamiques.  
**Priorité : Élevée**  
**Solution** : Améliorer la gestion des événements temps réel dans le moteur graphique et audio.

### R5 : Le clavier MIDI pourrait manquer de sensibilité ou ne pas capter certaines nuances de jeu.  
**Priorité : Moyenne**  
**Solution** : Configurer les capteurs et vérifier leur calibration pour s’adapter à une large plage d’expressivité.

### R6 : Les variations de dynamique ou de rythme pourraient provoquer des bugs ou ralentir les évolutions visuelles.  
**Priorité : Moyenne**  
**Solution** : Tester les différents cas de variations rythmiques pour évaluer leur impact sur les visuels.

### R7 : Les utilisateurs pourraient éprouver des difficultés à comprendre les interactions possibles dans l’espace immersif.  
**Priorité : Faible**  
**Solution** : Fournir des indications visuelles ou sonores intuitives pour guider l’utilisateur.

![risques](https://github.com/user-attachments/assets/fa78ba27-3acf-4deb-bebc-2ea8f9f2efd4)

![matrice_risques](https://github.com/user-attachments/assets/40cac427-1336-4d6e-8c84-d6e71b1b11d3)

---


