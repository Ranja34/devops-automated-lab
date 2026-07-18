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

# DevOps Automated Lab - Étape 2 : Conteneurisation de l'Infrastructure

L'application web a été migrée avec succès d'un modèle monolithique vers une architecture conteneurisée isolée.

## Spécifications Docker
* **Moteur de conteneurisation :** Docker Engine & Docker-Compose
* **Image :** Nginx (Tag: `latest`)
* **Nom du conteneur :** `web_container`

##  Cartographie des Ports Réseau
* **Port externe (VM) :** `8080`
* **Port interne (Conteneur) :** `80`
* **Mécanisme :** Le trafic arrivant sur le réseau privé hôte (`192.168.50.10:8080`) est acheminé vers le port `80` du conteneur Docker.

## Commande d'exécution
```bash
docker-compose up -d
```

## Prochaine Étape
Semaine 3 : Automatisation globale du déploiement du serveur et de Docker via un Playbook **Ansible**.

