**Projet TypeSprint**

1. _Presentation du projet_ :

   TypeSprint est um jeu edducatif qui permet aux jouer d'ameliorer leur vitesse de frappe au clavier et leur
   precision a travers des defis chronometrer de different niveaux
   
2. _Objectifs du projet_ :

    - Ameliorer la vitesse de frappe de l'utilisateur
    - Apprendre la positiom correcte des touches
    - Proposer un jeu simple, rapide et motivant.
    - Mettre en pratiques mes connaissance en HTML, CSS et JavaScript
      
3. _Fonctionalite principales_
   
    i. Affichage des mots

       - Afficher un mot ou une phrase aleatoire a l'ecran.
       - Changer automatiquement de mots apres validation
   
   ii. Zone de saisie

       - champ text ou le joure tape le mot afficher
   
   iii. Systeme de score

       - +1 point pour chaque mot correct.
       - Calcul de :
             -> mot par minute (WPM)
             -> taux de precision

  iv. Chronometre

      - Temps limite
      
  v. Niveaux de difficulte

      - Facil : mots courts
      - Moyen : mots normaux
      - Difficile : mots long
      - Extreme : phrase

4. _Syteme de niveau_

  i. Objectif
     Augmenter progressivemnt la diffficultes pour :
     - ameliorela vitesse de frappe 
     - rendre le jeu plus motivant
     - creer une progression pour lr joueur


  ii. Structure des niveaux

    [niveau1] -> difficulte : facile ; temps : 60s - 50s ; Type_de_mots : mots courts
    [niveau2] -> difficulte : Moyen ; temps : 50s - 40 ; Type_de_mots : mots normaux
    [niveau1] -> difficulte : difficile ; temps : 40s - 30s ; Type_de_mots : mots longs
    [niveau1] -> difficulte : expert ; temps : 30s ; Type_de_mots : phrases

  iii. Logistique de progression : 
    Le jouer passe au niveau suivant si :
     - Score >= MOYENNE (exemple: 10) sinon il recommence le niveau
     
5.  _Interface Utilisateur_

   Elements necessaire :
    
     - nom du joueur
     - Titre du jeu
     - Zone d'affichsge du jeu
     - Champ de saisie
     - Score
     - Chronometre
     - Bouton Start et Reset
     - option Activer/ Desactiver le son

6. _Technologie a utiliser_

    - HTML : structure du jeu
    - CSS : design les mise en page
    - JavaScript : logique du jeu, gestion des score, gestion du temps, generation aleatoire des mots en fonction des nivaux
   
7. _Systeme de comptes joueures (Utilisation localstorage)_

    i. Objetif :

    permettre les joures d'avoir
        - un nom d'utilisateur
        - sauvegareder son score
        - conserver ses performances : 
    
   ii. Solution 
    Utilisation localstorage
        donnees a enregistrer : nom du jouer, Meilleure Score, Vitesse de frappe (WPM) 

   iii. Fonctionnement
        - le jouer  entr sont nom au demarrage.
        - le jeux verifie si le joueur existe
        - si oui , charger ses scores
        - sinon, creer un nouveau profil  

8. _Ajout de sons de vailidation_ 

    i. Objetif : Ajouter un son quand :

        - le mot est correcte
        - erreure de frappe
        - fin de partie (temps ecouler)

9. _Structure du projet_

   TypeSprint/
   |___ index.html
   |___ style.css
   |___ words.js (lste des mots)
   |___ players.js
   |___ sounds/
     |___ correct.mp3
     |___ erroe.mp3
     |___ finish.mp3