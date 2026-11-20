AYMARD Thomas								**INF3-FI**  
BIEJ Thomas  
HACHICHA Adam  
RALU--LEROY Clara  
PERES Thomas

**Cahier des charges**   
Application Web \- Calcul Distribué


# SOMMAIRE

- [Introduction](#introduction)  
    
- [Enoncé](#enoncé)  
  - [Description du problème à résoudre](#description-du-problème-à-résoudre)  
  - [Contexte](#contexte)
  - [Objectifs](#objectifs)

- [Pré-requis](#prérequis)
  - Connaissances requises
  - Ressources matérielles  
  - Ressources logicielles
  - Identifiants obligatoires


- [Priorités](#priorités)

# Introduction

Ce document constitue le cahier des charges pour le projet SAE IN5SA01.

L’objectif est de définir précisément les besoins exprimés dans le sujet officiel, de cadrer le travail du groupe en détaillant les fonctionnalités attendues, de fixer les contraintes techniques, ainsi que de servir de référence commune entre la maîtrise d'œuvre et la maîtrise d’ouvrage.

La structure de ce cahier des charges est comme suit : une introduction, posant le cadre et les objectifs de celui-ci; un énoncé, décrivant le problème à résoudre, le contexte et les objectifs de la solution; les pré-requis au projet, étant les compétences et ressources matérielles nécessaires; et enfin les priorités, définissant le hiérarchisation des développements selon leur importance.

Les documents référencés sont les suivant : 

- Énoncé de la SAE IN5SA01 (PDF en ligne et version papier)  
- Supports de cours (Programmation avancé)

# Enoncé

### **Description du problème à résoudre** 
La gestion de système distribué est un enjeu stratégique pour les chercheurs. Cependant, elle peut rapidement devenir complexe avec l’augmentation du nombre de machines. L’information sur les équipements peut être peu accessible et non centralisée, ce qui rend sa mise à jour difficile.  

Pour y remédier, il est essentiel de développer une application web distribuée, permettant à différents utilisateurs d’accéder à des fonctionnalités adaptées à leur rôle, et ce en assurant la centralisation, la fiabilité et la sécurité des données.

### **Contexte** 

Le projet SAE IN5SA01, consiste à développer une application web qui permettra à des chercheurs de réserver 1 à 4 RPI pour effectuer des calculs distribués.

Les technologies principales imposées sont : ...

Il faut également utiliser un dépôt GitHub partagé avec les enseignants, contenant le code et la documentation.

### **Objectifs**

L’objectif principal du projet est de développer une application Web permettant à des chercheurs de réserver une ou plusieurs machines appartenant à une ferme de calcul composée de quatre Raspberry Pi 4\. L’application devra permettre :

* d’identifier un utilisateur ;  
  * de consulter les Raspberry Pi disponibles ;  
  * de consulter les réservations existantes ;  
  * de sélectionner entre 1 et 4 Raspberry Pi ;  
  * de choisir une période de réservation ;  
  * d’enregistrer une réservation ;  
  * d’empêcher plusieurs utilisateurs de réserver le même Raspberry Pi sur une même période ;  
  * de modifier ou annuler une réservation ;  
  * de conserver les informations relatives aux réservations ;  
  * de connaître l’état ou la disponibilité des Raspberry Pi.

Une fois les machines réservées, le chercheur pourra les utiliser pour effectuer ses calculs distribués. Le lancement et l’exécution du calcul ne constituent donc pas directement le rôle principal de l’application Web. Le programme Python fourni par les enseignants permettra principalement de tester le fonctionnement de la ferme de calcul et l’utilisation simultanée de plusieurs Raspberry Pi.

### **Prérequis**

La réalisation du projet nécessite :

* l’accès au Raspberry Pi 5 attribué au groupe ;  
* l’accès aux quatre Raspberry Pi 4 de la ferme de calcul ;  
* les adresses IP des différentes machines ;  
* la configuration réseau fournie par les enseignants ;  
* les identifiants ou clés permettant les connexions aux Raspberry Pi ;  
* le choix d’un système d’exploitation commun pour les Raspberry Pi 4 ;  
* le programme Python de démonstration du calcul distribué ;  
* un dépôt GitHub partagé avec les enseignants ;  
* une base de données permettant d’enregistrer les utilisateurs, les Raspberry Pi et les réservations.


### **Questions à poser au client**

Utilisateurs

* Existe-t-il plusieurs rôles autre que chercheur et techniciens ?  
* Si oui, quels droits ont-ils ?

Réservations

* Peut t-on réserver à l’avance une tâche?  
  * Jusqu’à combien de temps à l’avance peut-on réserver ?  
  * Une réservation peut-elle être annulée à tout moment ?  
  * Une réservation peut-elle être modifiée ?  
* Un chercheur peut-il effectuer plusieurs réservations simultanément ?  
* Doit-on conserver l’historique des anciennes réservations ?

Raspberry Pi

* \~ Les quatre Raspberry Pi sont-ils considérés comme équivalents ?  
* Le chercheur peut-il préciser les Raspberry Pi qu’il souhaite ou seulement leur nombre ?  
* Quel système d’exploitation doit être installé sur les Raspberry Pi 4 ?

Accès aux machines

* Comment le chercheur accède-t-il aux Raspberry Pi après sa réservation ?  
* L’accès se fait-il directement en SSH ?  
* Les identifiants d’accès sont-ils permanents ou différents pour chaque utilisateur ?  
* Faut-il empêcher techniquement un utilisateur d’accéder à un Raspberry Pi qu’il n’a pas réservé ?  
* L’application doit-elle seulement gérer les réservations ou également contrôler les accès aux machines ?

Application Web

* Quelles technologies sont imposées ou interdites ?  
* L’application est-elle accessible uniquement depuis le réseau de l’IUT ?  
* Une interface administrateur est-elle nécessaire ?  
* L’utilisateur doit-il voir un calendrier des réservations ?  
* Doit-il recevoir une confirmation après avoir effectué une réservation ?

### **Priorités**

Priorité 1 — Fonctionnalités indispensables

* installation et configuration des Raspberry Pi ;  
* communication réseau entre le RPI5 et les RPI4 ;  
* application Web accessible ;  
* identification des utilisateurs ;  
* affichage des Raspberry Pi ;  
* consultation de leur disponibilité ;  
* création d’une réservation ;  
* réservation de plusieurs Raspberry Pi ;  
* choix d’une période de réservation ;  
* détection et interdiction des conflits de réservation ;  
* stockage des données dans une base de données.

Priorité 2 — Fonctionnalités importantes

* modification d’une réservation ;  
* annulation d’une réservation ;  
* consultation de ses réservations ;  
* historique des réservations ;  
* gestion de l’état des Raspberry Pi ;  
* interface administrateur.

Priorité 3 — Améliorations

* affichage sous forme de calendrier ;  
* notifications ou confirmations ;  
* statistiques d’utilisation des Raspberry Pi ;  
* amélioration de l’ergonomie de l’application

