Pour installer SSH sur Ubuntu, vous pouvez suivre ces étapes :

1. **Mettre à jour la liste des paquets** :
   Ouvrez un terminal et exécutez la commande suivante pour mettre à jour la liste des paquets disponibles :
   ```sh
   sudo apt update
   ```

2. **Installer le serveur OpenSSH** :
   Utilisez la commande suivante pour installer le serveur OpenSSH :
   ```sh
   sudo apt install openssh-server
   ```

3. **Vérifier le statut du service SSH** :
   Une fois l'installation terminée, vous pouvez vérifier si le service SSH est en cours d'exécution avec la commande suivante :
   ```sh
   sudo systemctl status ssh
   ```

   Vous devriez voir une sortie indiquant que le service SSH est actif et en cours d'exécution.

4. **Démarrer et activer le service SSH** :
   Si le service SSH n'est pas en cours d'exécution, vous pouvez le démarrer avec la commande suivante :
   ```sh
   sudo systemctl start ssh
   ```

   Pour s'assurer que le service SSH démarre automatiquement au démarrage du système, utilisez la commande suivante :
   ```sh
   sudo systemctl enable ssh
   ```

5. **Configurer le pare-feu (si nécessaire)** :
   Si vous utilisez `ufw` (Uncomplicated Firewall), vous devez autoriser les connexions SSH. Vous pouvez le faire avec les commandes suivantes :
   ```sh
   sudo ufw allow ssh
   sudo ufw enable
   ```

6. **Se connecter via SSH** :
   Pour se connecter à un serveur Ubuntu via SSH, utilisez la commande suivante à partir d'un autre ordinateur :
   ```sh
   ssh username@ip_address
   ```

   Remplacez `username` par votre nom d'utilisateur et `ip_address` par l'adresse IP de votre serveur Ubuntu.

En suivant ces étapes, vous devriez être en mesure d'installer et de configurer SSH sur votre système Ubuntu.
