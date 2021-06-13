# AN-2023-Chatbot
Projet de cours semestriels sur un module pour systèmes experr
========================================================================================================================
                                            PROJET SYSTEMES FORMELLES
========================================================================================================================

    Dans le cadre du cour de "Systèmes Formels" (Game Programming [GAP]) et de "Création d'une Intelligence Artificielle"
(Art & Intelligence Artificielle [AIA]), il nous a été demandé de réaliser une application de chatbot pour la santé
(pour la consultation des patient par un chatbot intelligent).

    Il était question pour nous de mettre sur pieds une application qui donnerait la possiblité de se connecter au chatbot par SMS (Shot Message Service) ou par WhatsApp. Nous avons pour cela mise sur pieds une plateforme web qui permet :
    - L'inscription et la gestion des comptes utilisateurs
    - Les modules de consultation par notre bot WhatsApp (partie SMS étant en attente)
    - L'accessibilité aux différentes consultations qu'on aurait eu à faire avec le chatbot (les fichiers des différentes consultations étant sauvegardés).
    - Accessibilité à d'autres contenues sur internet à partir de certains liens.
    - (En début de développement) application PC.


========================================================================================================================
                                                  DEVELOPPEMENT
========================================================================================================================

    * Le projet à été réalisé en Python avec le framework django dans un environnement virtuelle.
    * Les bases de données ont été implementées avec sqlite3.
    * Pour la mise en place du bot WhatsApp, nous avons utilisés twilo, flask et ngrok.

    Nous avons créés un projet django qui contient toute les views et le model de l'application. La base de données est assurée par un fichier dédié (db.sqlite3).


========================================================================================================================
                                            COMMENT LANCER L'APPLICATION
========================================================================================================================

    Pour pouvoir exécuter cette application, il faut avoir :
    - python2 ou python3 installé dans votre machine
    - Télécharger le framework django (pip install django)
    - Créer un environnement virtuel django ()
    - Copier ce projet dans votre environement virtuel
    - Exécuter la commande ===> $ [nom_de_l'environmt_virtu]\Scripts\activate.bat
    - Se positionner dans le projet et lancer la commande   ====> $ py manage.py runserver
    - Un lien http (de la forme http://127.0.0.1:[port].../) sera généré. L'ouvrir dans un navigateur.
    - Et l'application est fonctionnelle et vous êtes diriger vers la page de login.


    Pour pouvoir exécuter le whatsApp chatbot :
    - Lancer l'application ngrok ($ negrok.exe http [port_generer_plus_haut])
    - Une adresse IP sera donnée qui rendra accessible les fonctions du chatbot sur le net. Copier ce lien et le coller  dans le sandbox de votre compte twilo à l'endroit dedié.
    - Sur l'application, après s'être authentifier, naviger dans le dashboard et dans la rubrique des consultations, choisir whatsApp.
    - Cela redirige vers le site de whatsApp et demande si on veut ouvrir une communication avec le chatbot
    - Valider et cela vous ouvrira le chatbot. (Un model d'IA n'a pas été entrainer, car n'étant pas notre travail).

NB : Tous ces tracasseries avec twilo c'est parce que le chatbot de whatsApp est conçu uniquement pour les petites et moyennes entreprises. Il faut avoir un compte whatsApp Business et faire une demande (dans le site de whatsApp) de posséder un chatbot. C'est lorsque whatsApp valide cela qu'il fournit les paramètres d'un bot. Tout ce processus prend du temps et nécessite certains prérequis dont nous ne disposons pas. Twilo nous aide donc à avoir accès gratuitement au chatbot whatsApp pour tester nos applications avant de passer à la version professionnelle.



========================================================================================================================
                                            REPARTITION DES TACHES DU PROJET
========================================================================================================================

* Pages de login et d'inscription avec le contrôle des entrées (Application web et Application PC)
        - WAGSONG DJOMEGNI Michelle Christa (18P231)
        - KOMTCHEU VEIGNE LEUKAM Armand Colin (18P230)

* Réalisation de la page d'acceuil, du dashboard et des styles y contenus
        - ONDOUA Anne Lise Juliane (18P224)
        - ADJAWOUNG MEDONZAP Evabel Nora (18P227)

* Modélisation et mise sur pied de la base de données dans django + gestion des comptes utilisateurs
        - DIGHO DONMEZA TANKEU Jordan (20P442)
        - FONGANG NGOMSEU Loïc Dickel (18P232)

* Gestion de l'interactivité de l'applicaion
        - AVAH Justin Jules Clément (20P450)
        - NLEMEH BANGA Jean Blaise (18P228)
        - ANAGUE TSAFACK Derrick (18P214)


* Mise sur pied du chatbot de whatsApp avec twilo
        - TEUGUIA TADJUIDJE Rodolf Sederis (18P212)
        - DIGHO DONMEZA TANKEU Jordan (20P442)
