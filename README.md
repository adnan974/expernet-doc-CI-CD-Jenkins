# Jenkins-CI/CD

Ce document a pour but d'expliquer ce qu'est Jenkins, comment l'installer ainsi que la notion de CI/CD

## CI/CD - Définition et avantages

CI/CD est un accronyme qui veut dire: Continuous Integration/Continuous Delivery/Deployement.

Le CI/CD représente une suite d'étape (pipeline) qui permet d'automatiser  le build, les test, le deploiement d'une application dans un serveur.

Si on rentre un peu plus dans les détails, dans CI/CD, on distingue 3 notions distinctes:
#### CI(Continuous Integration):
C'est une suite d'étape qui va s'éxécuter après le push d'un code dans un repository. Généralement, un CI service se déclenchera après le push et exécutera un script dans un CI serveur.

Par exemple, imaginons qu'une équipe de 2 developpeurs veulent travailler sur un projet et qu'ils ont mis en place un systeme d'intégration continu. Lorsqu'ils vont push leur code sur un repository, un CI service(gitHub Action, Jenkins etc...) sera déclenché. Ce service entrainera une suite d'actions qui va lancer des commandes à partir du code qui été push. génréralement le code sera build et testé sur un serveur pour voir si tout fonctionne correctement.
Ensuite il sera déployé automatiquement dans le serveur de production.

#### CD(Continuous Delivery):
C'est une extension de la Continuous Integration. Elle permet de rendre certains processus de deploiement automatique. Cette étape n'est pas à 100% automatique. L'homme peut encore intervenir dans un des étapes du déploiement.  

Si on reprend l'exemple ci-dessous, non seulement le code sera build et testé (CI) mais une fois que ces étapes sont passées, certains processus de déploiement seront aussi executés automatiquement. (CD) 


#### CD(Continuous Deployment): 

C'est le niveau au dessus du contiuous Delivery. Le continuous deployment rend le processsus de déploiement à 100% automatique. Aucunne intervention de l'homme n'est requise.

#### Le CI/CD apporte plusieurs avantages:

* Le developpeur n'a plus besoin de compiler, générer un executable, aller sur un serveur et installer une application. 
Tout est automatisé à travers un script. Le developpeur gagne du temps tout en évitant les erreurs humaines ou les oublis qu'il peut y avoir.
* Les bugs sont detectés plus rapidement et plus tôt car chaque push entraîne le deploiement et le test du code.
* Le developpeur a un feedback rapide du code qu'il a push.
* Les erreurs critiques dans un projet sont minimisées.
	


## Jenkins - à quoi ça sert ?

## Jenkins - Installation (Windows)   
    
#### 1 - Téléchargement  

Allez sur la page officielle de Jenkins, dans la section téléchargement : https://www.jenkins.io/download/
Sélectionnez la version LTS correspondant à votre système d'exploitation  (dans notre ca, Windows 10 x64).

#### 2 - Lancer l'installation  

Une fois le téléchargement terminé, lancez l'installeur et suivez les différentes étapes.
Lors de la 2e étape, pour une installation en local (tests), sélectionnez la première option (Run service as LocalSystem)

#### 3 - Lancer Jenkins  

Une fois l'installation terminée, Jenkins est installé sur votre machine en tant que service et démarre automatiquement en même temps que Windows. Ouvrez un navigateur et allez sur localhost, sur le port que vous avez configuré pendant l'installation (ex : http://localhost:8080).
Lors de la première installation de Jenkins, un mot de passe a été généré. La page vous indique le path où se trouve ce mot de passe. Ouvrez une commade windows et utilisez la commande TYPE + path-vers-mot-de-passe afin d'afficher celui-ci

```bash
type [path-to-password]
```
## Troubleshooting - problèmes communs et solutions

## Comparatif avec les technologies similaires
Voici une liste exhaustive des "concurrents" de Jenkins.

#### Bitbucket
* Payant : 3$/mois pas open source
* Plateforme : web
* Support : 
	* Support en ligne
* Fonctionnalités : 
	* Contrôle des sources
 	* Contrôles/Permissions d'accès
 	* Débogage
 	* Définition des priorités
 	* Déploiement continu
 	* Développement d'applications web
 	* Développement de logiciel
 	* Développement mobile
 	* Gestion des tests
 	* Livraison continue

#### Anypoint Platform
* Gratuit mais pas open source
* Plateforme : 
	* web 
	* windows
	* mac
* Support : 
	* Base de connaissances
	* FAQ
	* Forum
	* Support en ligne
	* Support téléphonique
	* Tutoriels vidéo
* Fonctionnalités : 30

#### GitLab
* Payant : 4$/mois
* Plateforme : web et iphone
* Support : 
	* Base de connaissances
	* FAQ
	* Forum
* Fonctionnalités : 47

#### Buddy
* Payant : 75$/mois
* Plateforme : Web
* Support : 
	* en ligne 
	* et téléphonique
* Fonctionnalités : 34

#### Bitrise
#### CircleCI
* Payant : 30$/mois pas open source
* Plateforme : web et windows
* Support : 
	* Base de connaissances
	* FAQ
	* Forum
	* Support en ligne
	* Support téléphonique
	* Tutoriels vidéo
* Fonctionnalités : 3

#### TeamCity
#### Travis CI
* Payant : 69$/mois open source
* Plateforme : web
* Support : 
	* Base de connaissances
	* FAQ
	* Forum
	* Support en ligne
* Fonctionnalités : 20

#### Cyclr
* Payant : 599$/mois pas open source
* Plateforme : web
* Support : 
	* Base de connaissances
	* Support en ligne
	* Tutoriels vidéo 
* Fonctionnalités : 
	* Agrégation et publication de données
	* Analytique
	* Assemblage par glisser-déposer
	* Automatisation des processus métiers
	* Contrôle d'accès
	* Déploiement continu
	* Développement collaboratif
	* ETL (Extract Transform Load)
	* Gestion des tests
	* Livraison continue

#### Semaphone
* Payant : 20$/mois
* Plateforme : web
* Support : 
	* Base de connaissances
	* Support en ligne
* Fonctionnalités : 
	* Débogage
	* Déploiement continu
	* Gestion de la configuration
	* Gestion des autorisations
	* Gestion des tests
	* Journal de génération
	* Livraison continue

#### Codeship
* Payant : 49$/mois
* Plateforme : web
* Support : 
	* Support en ligne
* Fonctionnalités : 
	* Contrôle des sources
	* Contrôles/Permissions d'accès
	* Débogage
	* Déploiement continu
	* Développement de logiciel
	* Gestion de la configuration
	* Gestion des tests
	* Gestion du déploiement
	* Journal de génération
	* Livraison continue

#### Appcircle
* Payant : 49$/mois
* Plateforme : web et mobile
* Support : 
	* Support en ligne
* Fonctionnalités : 
	* Débogage
	* Déploiement continu
	* Gestion de la configuration
	* Gestion des autorisations
	* Gestion des tests
	* Journal de génération
	* Livraison continue

#### StarfishETL
* Payant : 200$/mois
* Plateforme : web et windows
* Support : 
	* Support en ligne
* Fonctionnalités : 
	* Accès mobile
	* Analyse de données
	* Analyse des performances
	* Compatible avec divers languages de programmation
	* Contrôle de qualité des données
	* Conversion de bases de données
	* Correspondance et fusion
	* Déploiement continu
	* Gestion des tests
	* Livraison continue
 		
#### Delphix
#### AWS CloudFormation

## Notre avis

## Sources
