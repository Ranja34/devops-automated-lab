# devops-automated-lab
# DevOps Automated Lab - Étape 1 : Fondations Système & Réseau

Ce projet documente la mise en place d'une infrastructure automatisée et sécurisée. 

##  Spécifications du Laboratoire Local
* **OS du Serveur :** Ubuntu Server 22.04 LTS (VirtualBox)
* **Accès distant :** SSH sécurisé via clé asymétrique Ed25519
* **Serveur Web :** Nginx (Port 80)

##  Procédure de sécurisation SSH
1. Génération de la paire de clés Ed25519 sur le poste client.
2. Exportation de la clé publique via `ssh-copy-id`.
3. Validation de la connexion sécurisée sans mot de passe.

## 🐳 Étape 2 : Conteneurisation de l'infrastructure avec Docker

L'application a été migrée d'un modèle monolithique vers une architecture conteneurisée pour garantir la portabilité et l'isolation des composants.

### 📦 Composants déployés
* **Moteur de conteneurisation :** Docker Community Edition
* **Gestionnaire de déploiement :** Docker-Compose
* **Image utilisée :** Official Nginx (Tag: `latest`)

### 🔌 Gestion des flux réseaux (Mapping)
* **Port Hôte (VM) :** 8080
* **Port Conteneur :** 80
* **Flux :** Le trafic entrant sur le port 8080 de la VM est automatiquement redirigé vers le port 80 isolé du conteneur.

### 🚀 Commande de déploiement accéléré
```bash
docker-compose up -d
```

## 📈 Prochaine Étape
Semaine 3 : Automatisation de toute l'installation (Docker + Configuration) avec Ansible.
