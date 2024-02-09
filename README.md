# projetdata

./orchestrateur.sh

sbt clean package

spark-submit --class  main.scala.mnmc.MnMcount C:\Users\ervan\Documents\GitHub\Mnmcount_R\scala\target\scala-2.12\main-scala-mnmc_2.12-1.0.jar









1-	Reformuler besoin clients
	Une interface plus attrayante pour le site d’espace élève 3il en respectant les bonnes pratiques UX /UI design pour une expérience utilisateur améliorée 
	Mettre sur pied un système d’authentification unifié basé sur Microsoft Open ID tout en garantissant la sécurité des données durant la migration du système existant pour le nouveau. Qui veut dire que pour chaque élève ou personnel il puisse se connecter avec les mêmes comptes sur toutes les plateformes
	Créer des comptes spécifiques avec un système d’authentification distinct pour les répondant financiers et les maitres d’apprentissage.
	Sélection d’un CMS convivial pour implémenté des interfaces intuitives pour une consultation des informations plus pertinentes pour les élèves avec une restriction d’accès aux PV des élèves concernés
	Mettre en place un système de publication convivial avec navigation facile pour le personnel
	Intégration d'un système d'upload de documents (PDF) simplifié pour encourager la publication directe sur l'espace élèves.
	Mettre sur pied une interface convivial pour le personnel de l’école leurs facilitant ainsi la mise à jour du contenu.
	L’hébergement du site doit rester externe pour des raisons de sécurité
	L’utilisation du SSH/SFTP pour l’upload des fichiers pour garantir la confidentialité des informations.
	Restreindre la plateforme administrative du système pour des personnes uniquement connecter sur le réseau intranet 
2-	Spécification fonctionnelles et spécification techniques
Spécification fonctionnelle	Spécification technique 	Exigences
Intégration d’une interface utilisateur	Utilisation d’un CMS (Joomla qui est l’un des plus puissants CMS, flexible et convivial)	Respecter la charte graphique de 3iL, etre responsive
Mettre sur pied un système d’authentification avec ID et mot de passe pour les élèves et le personnel de l’ecole	-	Baser sur Microsoft OpenID en utilisant le protocol OAuth 2.0
-	Utilisation du plugin Joomla OAuth 2.0	-	Il doit etre unifier et basé sur Microsoft OpenId
-	Deux champs pour entrer l’email (@3il.fr) et le password
-	
Authentification des comptes spécifique	-	Une table dans la Base de données pour le stockages des données liés aux intervenants	-	Ces comptes doivent être spécifique avec email et mot de passe ayant un compte élève sur lequel il est rattaché
-	Le compte doit avoir un email et un mot de passe différent de @3iL.fr
-	Ces comptes peuvent uniquement consulter
-	Ne s’appuient pas sur Microsoft OpenId
-	Mise en place d’une restriction d’access a la présentation des PV 
-	Mettre en place un système de notification	-	Mettre en place une gestion des privilège (Gestion des roles)	-	Seuls les élèves concernés pourraient voir leurs PV
-	Développer une interface administrative conviviale	-		-	Assurer la haute disponibilité du site
-	Site sécurisé
-	Mise à jour des informations	-	Upload doit se faire via SSH/SFTP	-	Hébergement doit être externe
-	Limiter l’accès administrative du site	-		-	Etre accessible uniquement via les adresses IP de 3iL

3-	Cahier des charges
3.1 Contexte
Le site de 3iL est une plateforme mise en place depuis 2016 dédier aux élèves, répondant financiers et maitre d’apprentissage. Il constitue l’affichage générale de l’école qui permet de consulter un ensemble de documents et fichiers pour la scolarité, les PVs, les bulletins de notes, compétences et relevés d’absences, des liens divers (dont l’emploi du temps).
3.2 Problématique
Le site ne répond plus aux attentes de l’écoles sur différents points comme notamment :
-	L’esthétique du site qui ne correspond plus aux canons actuels 
-	L’authentification INE/date de naissance n’est pas modifiable 
-	Le CMS utilisé n’est pas suffisamment user-friendly pour le personnel administratif de l’école chargé de mettre à jour le contenu, notamment pour tout ce qui est upload de documents (PDF). Cela incite à faire des diffusions par mail au lieu d’une publication sur l’espace élèves. Ce qui pose le problème des versions successives. 
-	La présentation des PV de jury n’est pas restreinte à ce qui concerne directement l’élève 
-	Un maître d’apprentissage ayant plusieurs élèves de l’école doit se connecter autant de fois qu’il a d’alternants
3.2 Objectif Global
Mettre sur pied un site qui va optimiser l'utilisation de l'espace élève, tout en assurant une esthétique moderne, une sécurité renforcée, et une expérience utilisateur améliorée pour toutes les parties prenantes, y compris le personnel administratif, les élèves, et les maîtres d'apprentissage pour l’école 3iL.
3. 3 Contraintes 
3. 3.1 Normes de Sécurité :
-	Respect strict des normes de sécurité en vigueur pour protéger les données sensibles des élèves, répondants financiers et maitre d’apprentissage.
-	Utilisation de protocoles sécurisés pour toutes les communications, notamment lors des mises à jour.
3.3.2 Migration des Données :
- Développement d'un plan de migration pour transférer les données des élèves en cours et des anciens élèves.
- Minimisation des interruptions de service pendant la période de transition.
3.3.3 Lancement pour la Rentrée en Septembre 2024 :
- Planification rigoureuse pour assurer le déploiement du nouveau site avant la rentrée de septembre 2024.
- Coordination avec toutes les parties prenantes pour une transition fluide.
3.4 - Livrables projet et produit
3.4.1 Livrable projet
Organigramme de premiers niveau 
 
3.5	Budget
3.6	Délais
4	Estimation des couts
Besoins matériels	
Besoins immatériels	-	Analyse et rédaction des documents
-	Hébergement externes -	
Fond de roulement	-	Développement du site
Trésorerie	

5	Rétroplanning globale


-	Contexte 
-	Objectifs
-	Spécification f
-	Spécification t
-	Contraintes
-	Exigences 
-	Livrable projet et produit
-	Délais
-	Cout
-	Annexe
Estimation des couts
Phase	Activités	Heures Estimées	Taux Horaires (€)	Coût par Activité (€)	Coût Total de la Phase (€)
Analyse des Besoins et Conception	Études et réunions avec les parties prenantes	20	100	2 000	
Analyse des besoins utilisateur		30	100	3 000	
Conception de l'architecture et de l'interface utilisateur		40	100	4 000	
Rédaction de spécifications techniques		30	100	3 000	12 000
Développement et Tests	Développement backend (serveur, base de données)	200	100	20 000	
Développement frontend (interface utilisateur)		150	100	15 000	
Intégration de l'authentification Microsoft OpenID		50	100	5 000	
Tests (fonctionnels, de charge, de sécurité)		100	100	10 000	50 000
Migration des Données et Formation	Migration des données existantes	50	100	5 000	
Formation du personnel		20	100	2 000	7 000
Déploiement et Support	Déploiement du site	20	100	2 000	
Support initial	30	100	3 000	5 000	
Coûts Totaux					74 000
Contingence (10% pour imprévus)					7 400
Coût Total Estimé du Projet					81 400

Rétro planning global
Analyse des risques 
Risques	Probabilité d’apparition	Impact
La migration des données peut prendre plus de temps que prévu
	Forte	Très élevé
Les données sensibles pourraient être exposées en raison de vulnérabilités de sécurité
	Faible	Très élevé
Risque de dépassement budgétaire
	Faible	Faible
Dépassement des délais
	Faible	Elevé
Problème de compatibilité avec le navigateur	Faible	Elevé
Problème de performance 	Faible	Faible
Limitation du CMS	Faible	Faible
Non-adoption par les utilisateurs	Faible	Elevé 
Problème d’intégration des composants du site	Faible	Moyen
Erreurs de conception	Moyenne	Elevé

Matrice de choix pour choisir les fournisseurs
Critères	Pondération (1-10)	Entreprise
Délais		
Cout		
CMS proposée		
Méthodologie de gestion de projet		
Notoriété		
Expérience du fournisseur dans projet similaire		
Nombres de projets à son actif		
Intégration avec système existant		
Alignement avec les besoins spécifique de 3iL		
Conformité aux normes de design actuel		
Support maintenance		

Pour ces critères, le fournisseur répondant au plus aux attentes et critères aura la pondération la plus élevé

De proposer une liste de contrôles à effectuer pour valider la conformité de la solution livrée avec la demande.

