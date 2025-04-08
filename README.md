# Easy AI Starter Kit 2025: Automate Your Workflows with n8n (Offline & For Everyone)

## 📖 Projektbeschreibung
Das **Easy AI Starter Kit 2025** ist ein einfaches, sofort einsatzbereites Setup für [n8n](https://n8n.io/), eine Plattform, mit der du deine täglichen Arbeitsabläufe automatisieren kannst – ganz ohne Programmierkenntnisse! Entwickelt von M.Kamrau , basiert dieses Projekt auf dem offiziellen [n8n Docker-Compose-Starter-Kit](https://docs.n8n.io/hosting/installation/docker/), das jedoch nur HTTP unterstützt. Dieses Setup erweitert das n8n-Starter-Kit um HTTPS-Unterstützung (für sichere Verbindungen), verwendet `Docker` (einer Art Werkzeugkasten für Software), und ist offline nutzbar. Es enthält eine Datenbank (PostgreSQL) und KI-Funktionen (via Ollama), um deine Aufgaben smarter zu erledigen.

Dieses Starter-Kit ist für **jedermann** gedacht: Egal, ob du ein kleines Unternehmen führst, in der IT arbeitest oder einfach nur deine persönlichen Prozesse automatisieren möchtest – du kannst es auf einem Server oder einem guten PC nutzen, mit Windows, Linux oder macOS. Es ist perfekt, um deine Arbeitsabläufe zu digitalisieren (z. B. Daten organisieren, Benachrichtigungen senden) und zu automatisieren, auch ohne Internetverbindung. Das Setup ist ein Lernprojekt und dient als Ausgangspunkt für deine eigenen Ideen – es ist nicht für den produktiven Einsatz gedacht, sondern als Basis für Anpassungen.

### Warum dieses Starter-Kit?
- **Für jedermann**: Du brauchst keine Programmierkenntnisse – folge einfach den Schritten und starte!
- **Einfachheit**: Wähle dein Betriebssystem, installiere ein paar Tools, und automatisiere deine Arbeit in wenigen Schritten.
- **Flexibilität**: Funktioniert auf Windows, Linux oder macOS, auf einem Server oder einem guten PC.
- **Digitalisierung**: Verwandle manuelle Prozesse (z. B. Daten sortieren, E-Mails senden) in automatische Abläufe.
- **Offline-Nutzung**: Arbeite ohne Internet – ideal für sichere Umgebungen oder Orte ohne Netz.

## 🔥 Funktionen
- ✅ Offline nutzbar: Keine Internetverbindung nach der Einrichtung erforderlich
- ✅ Sicher: Mit HTTPS (verschlüsselte Verbindung) für deine Daten
- ✅ Einfache Datenbank: Speichert deine Daten lokal (mit PostgreSQL)
- ✅ KI-Unterstützung: Nutze KI (via Ollama) für smarte Aufgaben
- ✅ Flexibel: Funktioniert auf Windows, Linux, macOS – auf Servern oder PCs

## 🛠 Voraussetzungen
- Ein Computer (Server oder guter PC) mit einem Betriebssystem deiner Wahl (Windows, Linux, macOS)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (für Windows/macOS) oder [Docker](https://docs.docker.com/engine/install/) (für Linux) – ein Werkzeug, um Software in "Boxen" (Containern) auszuführen
- [OpenSSL](https://www.openssl.org/) (für sichere Verbindungen, oft schon installiert)
- [Visual Studio Code](https://code.visualstudio.com/) (optional, um Dateien zu bearbeiten)
- Ubuntu (nur für Windows-Nutzer, über den Microsoft Store)

## 🚀 Schnellstart: Automatisiere deine Arbeit in wenigen Schritten (Offline nutzbar)
Diese Schritte zeigen dir, wie du von einem frisch aufgesetzten Computer zu einem laufenden Automatisierungssystem kommst – auch ohne Internet (nach der Einrichtung). Die Anleitung ist für Windows detailliert, aber die Schritte sind auf Linux und macOS ähnlich.

1. **Betriebssystem einrichten**  
   - Wähle ein Betriebssystem (Windows, Linux, macOS) und installiere es auf deinem Computer (Server oder guter PC).  
   - **Für Windows**:  
     - Lade das [Windows 11 Installationsmedium](https://www.microsoft.com/de-de/software-download/windows11) herunter.  
     - Erstelle ein bootfähiges USB-Laufwerk mit Tools wie [Rufus](https://rufus.ie/).  
       ![Rufus USB Setup](https://via.placeholder.com/600x400.png?text=Rufus+USB+Setup)  
       *(Hinweis: Füge hier einen Screenshot von Rufus ein.)*  
     - Starte den PC vom USB-Laufwerk und folge den Anweisungen zur Installation.  
     - Aktiviere Windows mit deinem Product Key.  
     - Aktiviere die Windows-Features für Docker:  
       - Öffne *Systemsteuerung > Programme > Programme und Features > Windows-Features aktivieren oder deaktivieren*.  
       - Aktiviere *Windows-Subsystem für Linux (WSL)* und *Plattform für virtuelle Computer*.  
         ![Windows Features](https://via.placeholder.com/600x400.png?text=Windows+Features+WSL)  
         *(Hinweis: Füge hier einen Screenshot der Windows-Features ein.)*  
       - Starte den PC neu.  
   - **Für Linux/macOS**: Installiere dein bevorzugtes System (z. B. Ubuntu Server, macOS) und aktualisiere es.

2. **Ubuntu für WSL installieren (nur Windows)**  
   - Öffne den [Microsoft Store](https://www.microsoft.com/store/apps) und suche nach *Ubuntu* (z. B. Ubuntu 22.04 LTS).  
     ![Microsoft Store Ubuntu](https://via.placeholder.com/600x400.png?text=Microsoft+Store+Ubuntu)  
     *(Hinweis: Füge hier einen Screenshot des Microsoft Stores mit Ubuntu ein.)*  
   - Klicke auf *Installieren* und warte, bis die Installation abgeschlossen ist.  
   - Starte Ubuntu über das Startmenü, um die Erstkonfiguration abzuschließen (Benutzername und Passwort festlegen).  
     ![Ubuntu Setup](https://via.placeholder.com/600x400.png?text=Ubuntu+Setup)  
     *(Hinweis: Füge hier einen Screenshot der Ubuntu-Erstkonfiguration ein.)*

3. **Updates installieren**  
   - **Windows**: Öffne *Einstellungen > Windows Update*, klicke auf *Nach Updates suchen* und installiere alle Updates.  
     ![Windows Update](https://via.placeholder.com/600x400.png?text=Windows+Update)  
     *(Hinweis: Füge hier einen Screenshot der Windows Update-Seite ein.)*  
   - **Linux**: Führe `sudo apt update && sudo apt upgrade -y` aus (für Ubuntu).  
   - **macOS**: Gehe zu *Systemeinstellungen > Softwareupdate* und installiere alle Updates.  
   - Starte das System neu, falls erforderlich.

4. **Docker installieren**  
   - **Windows/macOS**: Lade [Docker Desktop](https://www.docker.com/products/docker-desktop/) herunter, installiere es und starte es.  
     - **Windows**: Gehe in Docker Desktop zu *Settings > Resources > WSL Integration*.  
       - Aktiviere *Enable integration with my default WSL distro*.  
       - Aktiviere die Integration mit Ubuntu (Schalter auf *On*).  
         ![Docker WSL Integration](https://via.placeholder.com/600x400.png?text=Docker+WSL+Integration)  
         *(Hinweis: Füge hier den tatsächlichen Pfad zu deinem Screenshot ein.)*  
       - Klicke auf *Apply & Restart*.  
   - **Linux**: Installiere Docker und Docker Compose:  
     - Folge der Anleitung für [Docker](https://docs.docker.com/engine/install/) und [Docker Compose](https://docs.docker.com/compose/install/).  
     ![Docker Desktop](https://via.placeholder.com/600x400.png?text=Docker+Desktop+Start)  
     *(Hinweis: Füge hier einen Screenshot von Docker Desktop nach dem Start ein.)*

5. **Visual Studio Code installieren (optional)**  
   - Lade [Visual Studio Code](https://code.visualstudio.com/) herunter und installiere es, falls du Dateien bearbeiten möchtest.  
     ![VS Code Install](https://via.placeholder.com/600x400.png?text=VS+Code+Install)  
     *(Hinweis: Füge hier einen Screenshot der VS Code-Installationsseite ein.)*

6. **Dieses Projekt herunterladen oder ein eigenes Setup erstellen**  
   - **Option 1: Dieses Projekt herunterladen**  
     - Lade das Projekt als ZIP von GitHub herunter: [Download-Link](https://github.com/MKamrau/n8n-ai-starter-kit-https/archive/refs/heads/main.zip).  
       ![GitHub Download](https://via.placeholder.com/600x400.png?text=GitHub+Download+ZIP)  
       *(Hinweis: Füge hier einen Screenshot der GitHub-Download-Seite ein.)*  
     - Entpacke es und öffne den Ordner in einem Terminal (Windows: Eingabeaufforderung oder PowerShell; Linux/macOS: Terminal).  
     - Wechsle in den Ordner:  
       ```bash
       cd Pfad/zum/Ordner
       ```
   - **Option 2: Eigenes Setup erstellen**  
     Erstelle eine Datei namens `docker-compose.yml` mit folgendem Inhalt:  
     ```yaml
     version: '3.8'
     services:
       n8n:
         image: n8nio/n8n
         ports:
           - "5678:5678"
         volumes:
           - ./certs:/certs
         environment:
           - N8N_PROTOCOL=https
           - N8N_SSL_KEY=/certs/n8n.key
           - N8N_SSL_CERT=/certs/n8n.crt
           - OLLAMA_HOST=http://host.docker.internal:11434
       ollama:
         image: ollama/ollama
         ports:
           - "11434:11434"
     ```
     **Hinweis**: `host.docker.internal` ermöglicht die Kommunikation zwischen n8n und Ollama. Du kannst dies in der Datei oder in einer `.env`-Datei anpassen:  
     ```env
     OLLAMA_HOST=http://host.docker.internal:11434
     ```

7. **Alles für Offline-Nutzung vorbereiten**  
   - Lade die benötigten Software-Pakete (Docker-Images) herunter, solange du online bist:  
     ```bash
     docker pull n8nio/n8n
     docker pull ollama/ollama
     docker pull postgres
     ```
     ![Docker Pull](https://via.placeholder.com/600x400.png?text=Docker+Pull+Images)  
     *(Hinweis: Füge hier einen Screenshot des Terminals mit `docker pull` ein.)*  
   - Optional: Speichere die Images, um sie auf einem Offline-System zu nutzen:  
     ```bash
     docker save -o n8n.tar n8nio/n8n
     docker save -o ollama.tar ollama/ollama
     docker save -o postgres.tar postgres
     ```
     Auf einem Offline-System kannst du sie laden:  
     ```bash
     docker load -i n8n.tar
     docker load -i ollama.tar
     docker load -i postgres.tar
     ```

8. **Sichere Verbindung einrichten (HTTPS)**  
   - Erstelle einen Ordner für Zertifikate und generiere ein Zertifikat:  
     ```bash
     mkdir certs
     openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
         -keyout certs/n8n.key \
         -out certs/n8n.crt \
         -subj "/C=DE/ST=Hessen/L=Frankfurt/O=Max Mustermann/OU=IT/CN=n8n.local"
     ```
     ![OpenSSL Cert](https://via.placeholder.com/600x400.png?text=OpenSSL+Certificate+Creation)  
     *(Hinweis: Füge hier einen Screenshot des Terminals mit dem OpenSSL-Befehl ein.)*

9. **Setup starten**  
   - Starte das Setup mit Docker:  
     ```bash
     docker-compose up -d
     ```
     ![Docker Compose Up](https://via.placeholder.com/600x400.png?text=Docker+Compose+Up)  
     *(Hinweis: Füge hier einen Screenshot des Terminals mit `docker-compose up -d` ein.)*  
   - **Hinweis**: Nach dem Start funktioniert alles offline, da alle Pakete lokal verfügbar sind.

10. **n8n im Browser öffnen**  
    - Öffne deinen Browser und gehe zu `https://n8n.local:5678`.  
    - Du siehst eine Warnung wegen des Zertifikats – das ist normal, da es selbst erstellt ist. Klicke auf *Erweitert* und *Weiter zu n8n.local*.  
      ![Browser Warning](https://via.placeholder.com/600x400.png?text=Browser+Certificate+Warning)  
      *(Hinweis: Füge hier einen Screenshot der Browser-Warnung ein.)*  
      ![n8n Interface](https://via.placeholder.com/600x400.png?text=n8n+Interface)  
      *(Hinweis: Füge hier einen Screenshot der n8n-Oberfläche ein.)*

11. **KI-Funktionen nutzen (Ollama)**  
    - Lade ein KI-Modell, solange du online bist:  
      ```bash
      docker exec -it <ollama-container-name> ollama pull llama3
      ```
      (Ersetze `<ollama-container-name>` durch den Namen deines Ollama-Containers, den du in Docker Desktop siehst.)  
      ![Ollama Pull](https://via.placeholder.com/600x400.png?text=Ollama+Pull+Model)  
      *(Hinweis: Füge hier einen Screenshot des Terminals mit `ollama pull` ein.)*  
    - Öffne Docker Desktop (oder das Terminal), gehe zu deinem Ollama-Container und liste die Modelle:  
      ```bash
      ollama ls
      ```
      ![Ollama List](https://via.placeholder.com/600x400.png?text=Ollama+List+Models)  
      *(Hinweis: Füge hier einen Screenshot des Terminals mit `ollama ls` ein.)*

## 🌟 Beispiele: Was du automatisieren kannst (auch offline)
Mit n8n kannst du viele Aufgaben automatisieren – hier ein paar Ideen:
- **Daten organisieren**: Sortiere Daten aus Tabellen (z. B. Excel, CSV) und speichere sie in einer Datenbank.  
  ![Data Sorting](https://via.placeholder.com/600x400.png?text=n8n+Data+Sorting+Workflow)  
  *(Hinweis: Füge hier einen Screenshot eines n8n-Workflows für Datenorganisation ein.)*  
- **Benachrichtigungen**: Lass dich informieren, wenn neue Dateien in einem Ordner auftauchen (z. B. per Skript).  
  ![Notification Workflow](https://via.placeholder.com/600x400.png?text=n8n+Notification+Workflow)  
  *(Hinweis: Füge hier einen Screenshot eines n8n-Workflows für Benachrichtigungen ein.)*  
- **KI-Unterstützung**: Nutze Ollama, um Texte zu erstellen (z. B. Berichte) oder Daten zu analysieren.  
  ![AI Workflow](https://via.placeholder.com/600x400.png?text=n8n+AI+Workflow)  
  *(Hinweis: Füge hier einen Screenshot eines n8n-Workflows mit Ollama ein.)*  
- **Prozesse vereinfachen**: Automatisiere wiederkehrende Aufgaben, wie das Umbenennen von Dateien oder das Erstellen von Backups.  
  ![File Automation](https://via.placeholder.com/600x400.png?text=n8n+File+Automation+Workflow)  
  *(Hinweis: Füge hier einen Screenshot eines n8n-Workflows für Dateiautomatisierung ein.)*

## 📂 Projektstruktur
```
easy-ai-starter-kit/
├── certs/              # Zertifikate (n8n.key, n8n.crt)
├── docker-compose.yml  # Setup-Datei für Docker
├── .env.example       # Beispiel-Datei für Einstellungen
└── README.md          # Diese Anleitung
```

## 🎓 Lernprozess und Quellen

### Was ich gelernt habe
- **Automatisierung leicht gemacht**: Mit n8n kannst du Prozesse automatisieren, ohne programmieren zu müssen.  
  Quelle: [n8n Beginner Course (1/9) – Introduction to Automation](https://youtu.be/4BVTkqbn_tY?si=itn7mGDsaY6mgmrw) von [Nate Herk](https://www.youtube.com/@nateherk)  
- **Sichere Verbindungen**: Wie man mit OpenSSL sichere Verbindungen einrichtet.  
  Quelle: [OpenSSL Dokumentation](https://www.openssl.org/docs/man1.1.1/man1/req.html)  
- **Offline-Nutzung**: Wie man Software (Docker) so einrichtet, dass sie ohne Internet funktioniert.  
  Quellen:  
  - [n8n Self Hosting Tutorial](https://youtu.be/TFTLMQLozCI?si=cpaJ6GOO_2lN4WAP) von [n8n](https://www.youtube.com/@n8n)  
  - [Build a Siri-activated AI Agent using n8n and Apple Shortcuts](https://youtu.be/Jgouaas1fUE?si=zU5zhoD3y9y2CFgk) von [Cole Medin](https://www.youtube.com/@ColeMedin)  

### Woher die Inhalte stammen
- Das Setup basiert auf dem offiziellen [n8n Docker-Compose-Starter-Kit](https://docs.n8n.io/hosting/installation/docker/), das jedoch nur HTTP unterstützt. Dieses Projekt fügt HTTPS hinzu, um die Sicherheit zu erhöhen.  
- Die Zertifikatserstellung basiert auf OpenSSL-Befehlen aus der offiziellen Dokumentation.  
- Die Idee, Arbeitsabläufe zu automatisieren, wurde durch Cole Medins Beispiele inspiriert.

**Empfehlung**: Schaut euch meine Quellen an – sie erklären alles Schritt für Schritt, auch wenn sie online sind!

## 🔧 Einschränkungen und Hinweise
- **Lernprojekt**: Dieses Setup ist ein Beispiel und nicht für den professionellen Einsatz gedacht.
- **Sicherheit**: Die Zertifikate sind selbst erstellt – für echte Projekte solltest du offizielle Zertifikate (z. B. von Let’s Encrypt) nutzen.
- **Verbesserungsideen**: Vorgefertigte Automatisierungen oder ein einfacher Leitfaden für n8n könnten es noch besser machen.

## ℹ️ Über dieses Projekt
Entwickelt von M. Ka. als Lernprojekt, um jedermann die Möglichkeit zu geben, Arbeitsabläufe 2025 einfach zu automatisieren – sicher, offline und mit KI-Unterstützung.

## 📚 Quellenübersicht
- [n8n Dokumentation](https://docs.n8n.io/)  
- [Docker Compose Referenz](https://docs.docker.com/compose/compose-file/)  
- [OpenSSL Dokumentation](https://www.openssl.org/docs/)  
- YouTube: [Nate Herk](https://www.youtube.com/@nateherk)  
  - [n8n Beginner Course](https://youtu.be/4BVTkqbn_tY?si=itn7mGDsaY6mgmrw)  
- YouTube: [Cole Medin](https://www.youtube.com/@ColeMedin)  
  - [Siri-activated AI Agent with n8n](https://youtu.be/Jgouaas1fUE?si=zU5zhoD3y9y2CFgk)  
- YouTube: [n8n](https://www.youtube.com/@n8n)  
  - [n8n Self Hosting Tutorial](https://youtu.be/TFTLMQLozCI?si=cpaJ6GOO_2lN4WAP)

---
