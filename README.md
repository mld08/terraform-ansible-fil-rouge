# terraform-ansible-fil-rouge

Ce dossier contient les fichiers nécessaires pour déployer l'infrastructure du projet Fil Rouge(Profile App) a travers minikube à l'aide de Terraform et Ansible.

## Structure du dossier

- `main.tf` : Fichier principal de configuration Terraform.
- `variables.tf` : Déclaration des variables utilisées dans le projet.
- `outputs.tf` : Définit les sorties de l'infrastructure.
- `ansible/` : Contient les playbooks et inventaires Ansible pour la configuration post-provisionnement.
- `README.md` : Ce fichier d'explication.

## Prérequis

- [Terraform](https://www.terraform.io/downloads.html) installé
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installé
- [Minikube](https://minikube.sigs.k8s.io/docs/start/) installé et configuré

## Utilisation

1. Initialiser le projet Terraform :
    ```bash
    terraform init
    ```
2. Vérifier le plan d'exécution :
    ```bash
    terraform plan
    ```
3. Appliquer la configuration (Ansible sera exécuté automatiquement via Terraform) :
    ```bash
    terraform apply
    ```

## Notes

- Adaptez les variables dans `variables.tf` selon vos besoins.
- Consultez la documentation officielle de Terraform et Ansible pour plus d'informations.
- Pensez à détruire l'infrastructure après usage :
  ```bash
  terraform destroy
  ```

