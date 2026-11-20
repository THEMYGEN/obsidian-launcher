# Obsidian Launcher

Ein Windows-Desktop-Launcher für Minecraft Java Edition mit Microsoft-Anmeldung, mehreren Profilen und Modrinth-Integration.

## Funktionen

- Anmeldung über Microsofts Gerätecode-Seite; das Launcher-Fenster fragt kein Microsoft-Passwort ab.
- Verschlüsselte Speicherung der erneuerbaren Anmeldedaten über Electron `safeStorage`.
- Profile mit eigener Minecraft-Version und Vanilla-, Fabric-, Forge-, NeoForge- oder Quilt-Installation.
- Pro Profil einstellbarer Arbeitsspeicher per Slider; der Maximalwert richtet sich nach dem installierten RAM des PCs (Standard: 2048MB).
- Automatische Installation der offiziellen Minecraft-Dateien, Loader-Bibliotheken und Java-21-Laufzeit beim ersten Start eines Profils.
- Eigenes PNG-Branding im Launcher sowie Windows-ICO für EXE, Fenster und Taskleiste.
- Rahmenloses Launcher-Fenster mit eigenen Minimieren-, Maximieren- und Schließen-Schaltflächen; der angemeldete Spieler wird mit seinem Minecraft-Skin-Kopf angezeigt.
- Launcher-Einstellungen für Deutsch oder Englisch sowie optional ein separates Minecraft-Konsolenfenster beim Start eines Profils. Die Einstellungen werden im Electron-Benutzerordner gespeichert.
- Neuigkeiten-Tab mit Meldungen aus der konfigurierbaren Raw-URL `NEWS_URL` in `src/main.js`, neuesten Einträgen zuerst und optionalen Bannerbildern; Netzwerk- und JSON-Fehler werden direkt im Tab angezeigt.
- Mod Menu wird bei Fabric- und Quilt-Profilen automatisch samt erforderlicher Modrinth-Abhängigkeiten installiert; für Forge und NeoForge ist Mod Menu nicht verfügbar.
- Fortschrittsbalken mit Download-Prozenten und Datenmenge während Minecraft- und Java-Downloads.
- Integrierte Mod-, Ressourcenpaket- und Shader-Verwaltung pro Profil mit Modrinth-Suche, Icons, Aktivieren/Deaktivieren und Löschen. Erforderliche Mod-Abhängigkeiten werden anhand der gewählten Modrinth-Version automatisch in einer mit Minecraft-Version und Loader kompatiblen Version installiert. Icons älterer Mods werden anhand ihrer Dateiprüfsumme auf Modrinth gesucht. Ressourcenpakete können auch in Vanilla-Profilen verwaltet werden; die Shaderverwaltung erscheint nur bei Modloader-Profilen und benötigt zum Spielen einen passenden Shader-Loader wie Iris oder OptiFine.

Zum Spielen benötigst du ein Microsoft-Konto mit einer gültigen Minecraft-Java-Edition-Lizenz. Der Launcher ist nicht von Microsoft, Mojang oder Modrinth herausgegeben oder unterstützt.

Profile und Installationen liegen im Electron-Benutzerordner unter `profiles.json` und `instances/<Profil-ID>`. Die Authentifizierungsdaten werden im selben Benutzerordner separat verschlüsselt gespeichert.
