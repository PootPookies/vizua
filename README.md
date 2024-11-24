# Vizua - Planification

[Précédement Wave3D](https://jejed8.github.io/wave3d/)

## Concept 
L'expérience est une installation immersive où l'utilisateur joue sur un clavier MIDI et voit des visuels dynamiques se déployer autour de lui en réalité virtuelle. Chaque note déclenche des animations spectaculaires qui réagissent en temps réel, créant un spectacle audiovisuel captivant et interactif.

<img width="1710" alt="Screenshot 2024-11-04 at 3 59 05 PM" src="https://github.com/user-attachments/assets/0d1631bd-a0b8-48c1-8a90-9e10aeeb605e">

### Inspiration

Le projet s'inspire des "Music Visualizers", populaires sur les lecteurs de médias audio des appareils électroniques, particulièrement entre les années 2000 et le début des années 2010.

#### Exemples :
- [Apple iTunes Classic Visualizer](https://www.youtube.com/watch?v=i4JbAm7awCc&list=PLPF1dVJ5LqyQi0A6NYr3UD-zhF91ySM_2&index=2)


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


## Synoptique
![Diagramme sans nom drawio](https://github.com/user-attachments/assets/fb71d4a4-6987-40da-b670-2d7193b85f28)

#### Entrée

- **Clavier MIDI** : Envoie des signaux MIDI au DAW.
- **DAW (Digital Audio Workstation)** :
  - Reçoit le signal MIDI.
  - Modifie les sons (EQ, effets, etc.).
  - Envoie les données audio/MIDI à PyTorch et à TouchDesigner.

#### Analyse AI

- **Framework PyTorch** :
  - Reçoit le signal audio/MIDI modifié du DAW.
  - Analyse le son (détection de motifs, classification d'émotions).
  - Envoie les résultats d'analyse à TouchDesigner via OSC/WebSocket.

#### Communication

- **OSC / WebSocket** :
  - Transporte les données d'analyse de PyTorch vers TouchDesigner en temps réel.
  - Synchronise les échanges de données entre le DAW, PyTorch et TouchDesigner.

#### Création Visuelle

- **TouchDesigner** :
  - Reçoit les données MIDI/audio et les résultats d'analyse de PyTorch.
  - Crée des visuels dynamiques basés sur les notes jouées et l'analyse AI.
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
| Logiciel             | Description Technique                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------|
| TouchDesigner        | Génère des visuels interactifs et les rend en temps réel dans un environnement VR.                     |
| DAW (Ableton/Logic)  | Capture, modifie et traite les signaux MIDI/audio pour enrichir l'expérience sonore.                   |
| PyTorch              | Analyse les caractéristiques du son à l'aide de l'IA et transmet les données interprétées.            |
| OpenVR               | Permet l'intégration et le rendu stéréoscopique de la scène VR et gère le suivi des mouvements.        |
| OSC (Open Sound Control) | Protocole utilisé pour transmettre les données d'analyse et de contrôle en temps réel à TouchDesigner. |
| Oculus Software      | Établit la connexion et le suivi du casque Oculus avec le PC pour une immersion VR optimale.           |

## Plantation

![Desktop - 4](https://github.com/user-attachments/assets/9ed013e4-dcb6-41e3-b014-999a5959998b)









