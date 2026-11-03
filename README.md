# Baustellen-Webcam
Offizielles Git-Repo des Informatik Projektes

## Allgemein zu tun:

README.md updaten und wichtiges eintragen
Jeden Schritt des Projektes dokumentieren (z.B. Word Datei)

## Team A

  ### Zu tun:
    - 3D Box Druckfertigstellen und drucken
  ### Das hier ist bereits erledigt
    - Einrichtung des Rasberry Pi und Einrichtung der Kamera. Rehosten des Server -> Umebenennung neues Password und Co.

## Team B

  ### Zu tun:
    -XXX
  ### Das hier ist bereits erledigt
    -XXX
    
## Team C - Server & Website:

  ### Zu tun:
    - eigenes Testnetz für beide Pis einrichten
      -> LAN-Kabel für SFTP und Kommunikation zwischen Server und Kamera-Pi. WLAN ausschließlich für einen SFTP Upload der Daten auf eine Website (später)
    - Zeitraffer script erstellen
    - Webseite für das aktuelle Bild designen und bauen (evtl. auch Zeitraffer als live feature) -> wie stark müssen wir die Bilder komprimieren?
  ### Das hier ist bereits erledigt:
    - website folder und template wurden für später erstellt
    - server auf raspberry pi wurde aufgesetzt und bereinigt + der server wurde komplett neu aufgesetzt
    - erste testwebsite zum laufen bekommen (intern über gleiches netzwerk abrufbar)
    - das git-repo wurde auf den Server geklont und kann nun mit `git pull` gepullt werden
    - SFTP-Upload wurde für den user "webcam-upload" datenschutzkonform eingerichtet
    - über SFTP hochgeladene Bilder werden auf der Webseite angezeigt (sofern Name="aktuell.jpg")
    - Langfristige Pläne ausgearbeitet -> Bilder & Zeitraffer-Video vom Server per SFTP an Web-Server und Schulserver - dort werden sie dann angezeigt

## Grobe Übersicht, wie alles funktioniert:

1. Kamera-Pi macht Bilder und verpixelt diese
2. Bilder werden per SFTP sicher an den Server-Pi geschickt
3. Auf dem Server-Pi werden diese verarbeitet, sortiert und in das Zeitraffervideo eingefügt (alternativ Zeitraffervideo erst auf den Web-Servern aktualisieren -> effizientere Datenmengen)
4. Das neuste Bild und das bisherige Video werden von Server-Pi per SFTP an einen Web-Server geschickt, auf dem dann die Website verfügbar ist
5. Zusätzlich dazu werden die Bilder an den Schulserver geschickt und auf der Schulwebsite angezeigt
6. Die letzten 10 [oder X Anzahl] Bilder und das Video werden dann auf der Website angezeigt
  
   Bei neuen Bilder: Ältere werden vom Server gelöscht um Speicherplatz zu schaffen (oder Seperat irgendwo gespeichert)
