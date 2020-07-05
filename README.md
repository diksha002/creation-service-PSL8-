# creation-service-PSL8-
## Execution du fichier

Ce projet mount et unmount votre usb pendrive.

Dessous contient des `lignes de codes`.

> ETAPES:

 - Cloner le projet d'abord.
 
 - Donner le fichier usbDetectServ le droit d'execution
 ```
   - $chmod u+x usbDetectServ
 ```
 
 - Pour tester que le fichier usbDetect, executer le:
 ```
   - $./usbDetectServ
 ```

- Pour le service:
  - Ouvrez un autre terminal et deplacer vous dans /etc/systemd/system
    ```
    - $cd /etc/systemd/system
    ```
  - copier le fichier usb.service dans ce repertoire
    - Ou creer un autre fichier .service et copier coller le code de usb.service
    ```
      - $sudo nano usb.service
    ```
  - Pour lancer le service sur votre pc, modifier le code dans le fichier .service 
  qui se trouve dans /etc/systemd/system
    ```
    - ExecStart=Votre_path_file_de_votre_fichier_usbDetectServ
    ```
  - Pour lancer le service
    ```
     - $sudo systemctl enable usb
     - $sudo systemctl restart usb
    ```
  - Pour s'assurer si le service se deroule bien
    ```
    - $sudo systemctl status usb
    ```
  - Pour areter le service
    ```
      - $sudo systemctl stop usb
    ```
  
   
  




