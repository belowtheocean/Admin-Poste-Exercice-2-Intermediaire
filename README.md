# Admin-Poste-Exercice-2-Intermediaire

Pour cet exercice, j’ai créé un script bash qui sauvegarde automatiquement le contenu du dossier /home/test/Documents dans /home/test/backups, puis j’ai programmé son exécution quotidienne à 2h du matin. J’ai fait toutes les manipulations depuis PowerShell en SSH sur ma machine Linux.

# 1) Création du script de sauvegarde

J’ai commencé par créer le dossier qui contiendra mes sauvegardes, puis j’ai créé mon script :

<img width="960" height="43" alt="image" src="https://github.com/user-attachments/assets/ddcf44f6-8d11-45ba-be36-7813c33378b0" />

Contenu du script :

<img width="952" height="229" alt="Capture d&#39;écran 2025-11-07 192543" src="https://github.com/user-attachments/assets/aae9369d-d084-418b-afda-d529ba921101" />

J’ai ensuite rendu le script exécutable :

<img width="957" height="23" alt="image" src="https://github.com/user-attachments/assets/14462c89-b78e-48f8-a438-7460016f9dcd" />

Puis j’ai effectué un test manuel :
<img width="957" height="93" alt="image" src="https://github.com/user-attachments/assets/2a91340f-26b1-458b-a416-b06c55e81a9b" />

La sauvegarde s’est bien créée (fichier .tar.gz visible).

# 2) Automatiser l’exécution quotidienne à 2h du matin

J’ai utilisé crontab -e pour configurer la tâche planifiée :

<img width="957" height="206" alt="image" src="https://github.com/user-attachments/assets/ad124411-1ce8-451a-b55f-051886938eaa" />

<img width="958" height="572" alt="image" src="https://github.com/user-attachments/assets/0b424e49-917d-470a-908e-5956ee6a2989" />

Cette ligne permet au script de s’exécuter tous les jours à 02h00 automatiquement.

# Conclusion

J’ai mis en place un système de backup automatisé en bash. Le script archive mon dossier Documents et stocke les sauvegardes dans un dossier dédié. Ensuite, grâce à cron, la sauvegarde se fait tous les jours à une heure précise sans que j’aie besoin d’intervenir.
