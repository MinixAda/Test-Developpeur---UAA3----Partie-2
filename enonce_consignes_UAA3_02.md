# Test Développeur - UAA3 (Tache 2)
Analyse et Conception d'une Nouvelle Application (DeskLunch)

---

## Contexte de l'épreuve

Suite à votre excellente gestion des correctifs sur *DeskReserve* d'hier, le client (Jean-Marc) est très satisfait de votre ESN. Il a décidé de vous confier l'étude de faisabilité et la conception d'une toute nouvelle application métier "from scratch" pour ses employés.

L'entreprise fait face à un problème logistique avec la commande des repas de midi. Actuellement, tout est géré via un fichier Excel partagé qui génère des erreurs, des retards, et des oublis de paiement. Le client souhaite digitaliser ce processus avec une application baptisée **DeskLunch**.

Votre responsable vous demande de réaliser l'analyse préalable et le dossier de conception technique afin de préparer les futurs développements.

---

## Cahier des Charges (Besoins métiers)

Le client a formulé les besoins suivants lors de la dernière réunion :

> 1. **Deux types d'utilisateurs :** Les Employés (qui commandent) et l'Administrateur (les Ressources Humaines).
> 2. **Gestion des menus (Admin) :** Chaque lundi, l'Admin doit pouvoir saisir dans l'application le menu de la semaine suivante proposé par le traiteur partenaire (Plats, Desserts, Prix).
> 3. **Prise de commande (Employé) :** Les employés se connectent, consultent le menu de la semaine prochaine, et sélectionnent les plats qu'ils souhaitent pour chaque jour de la semaine. 
> 4. **Règle métier stricte (La Deadline) :** Les employés ont jusqu'au **jeudi 16h00** pour valider ou modifier leur commande pour la semaine suivante. Passé ce délai, le panier est verrouillé et plus aucune modification n'est possible.
> 5. **Génération de la commande traiteur (Admin) :** Le jeudi à 16h05, l'Admin se connecte et télécharge un récapitulatif global (liste des plats totaux à préparer) qu'il envoie au traiteur.

---

## Votre Mission

Vous devez rédiger un dossier d'analyse et de conception couvrant les axes suivants :

### 1. Traduction du besoin et Modélisation (UML)
* Traduisez brièvement le cahier des charges en liste de fonctionnalités (ou User Stories).
* Réalisez un **Diagramme Use Case** global de l'application.
* Réalisez **UN diagramme supplémentaire au choix** parmi : *Activité*, *Séquence* ou *État*, pour modéliser le comportement spécifique lié à **la règle de la Deadline du jeudi 16h00**.
* *(Note : Le diagramme de classes n'est pas demandé et ne sera pas évalué).*

### 2. Choix Techniques et Architecture
* Définissez la stack technique que vous prévoyez d'utiliser pour répondre à ce besoin, en vous basant sur votre socle de compétences (.NET, React, MSSQL...).
* Rédigez un court argumentaire justifiant vos choix : pourquoi cette architecture ? Quelles librairies spécifiques (Front et/ou Back) comptez-vous utiliser pour gagner du temps et répondre aux besoins (ex: requêtes HTTP, gestion des états, sécurité, formulaires...) ?

### 3. Stratégie de Déploiement (Docker & CI/CD)
* Rédigez une note de déploiement expliquant comment l'application sera conteneurisée.
* Décrivez la structure de votre application
  - Quels seront les services ? 
  - Quels ports seront exposés ?
* Mentionnez brièvement les étapes clés que devra contenir votre pipeline CI/CD pour automatiser les tests et la création de ces conteneurs.
* *(Note : Vous ne devez pas écrire les fichiers docker ou docker-compose).*

### 4. Procédure de Test
* Rédigez une procédure de test détaillée (étape par étape) pour valider spécifiquement la **Règle n°4 (La Deadline)**. 
* *Exemple d'attente :* Comment le testeur (ou le script) doit-il s'y prendre pour vérifier que l'application bloque bien les commandes après jeudi 16h00, tout en autorisant celles passées à 15h59 ?
* *(Note : Vous ne devez pas coder les tests unitaires !).*

---

## Critères d'Évaluation

* **Compréhension du besoin :** Les étapes de réalisation et les fonctionnalités décrites correspondent au cahier des charges.
* **Modélisation UML :** Les diagrammes respectent le formalisme UML, sont pertinents, et illustrent clairement les flux métiers (spécialement la logique de deadline).
* **Cohérence technique :** Les choix technologiques et les bibliothèques proposées sont justifiés, modernes et adaptés au contexte d'une application web.
* **Maîtrise de l'infrastructure :** La note de déploiement démontre une bonne compréhension de l'écosystème Docker.
* **Qualité de l'assurance qualité (QA) :** La procédure de test est claire, logique, reproductible et couvre les cas nominaux et aux limites.
* **Livrable attendu :** Un document d'analyse structuré (PDF, Word, ou Markdown) et les diagrammes associés. 

_Rappel : Aucun code source n'est demandé pour cette épreuve._