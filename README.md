# Meine Sprüche – iPhone Web-App

Diese kleine App zeigt auf Knopfdruck einen zufälligen Spruch an.

## Dateien

- `index.html` – die eigentliche App
- `manifest.webmanifest` – App-Name, Farben und Icons
- `sw.js` – sorgt für Offline-Funktion
- `icon-192.png`
- `icon-512.png`
- `apple-touch-icon.png`

## Eigene Sprüche eintragen

Öffne `index.html` und suche nach:

    const sprueche = [

Dort kannst du die vorhandenen Texte ändern, löschen oder ergänzen.

Wichtig:
- Jeder Spruch steht in Anführungszeichen.
- Zwischen zwei Sprüchen steht ein Komma.

Beispiel:

    const sprueche = [
      "Mein erster Spruch.",
      "Mein zweiter Spruch.",
      "Mein dritter Spruch."
    ];

## Kostenlos mit GitHub Pages veröffentlichen

1. Erstelle auf GitHub ein neues öffentliches Repository, z. B. `spruch-app`.
2. Lade ALLE Dateien aus diesem Ordner direkt in das Repository hoch.
3. Öffne im Repository `Settings` → `Pages`.
4. Wähle bei `Source` / `Build and deployment`:
   - `Deploy from a branch`
   - Branch: `main`
   - Ordner: `/ (root)`
5. Speichere die Einstellung.
6. Öffne anschließend die von GitHub Pages angezeigte Adresse.

## Auf dem iPhone installieren

1. Öffne die GitHub-Pages-Adresse in Safari.
2. Tippe auf das Teilen-Symbol.
3. Wähle `Zum Home-Bildschirm`.
4. Falls angezeigt, aktiviere `Als Web-App öffnen`.
5. Tippe auf `Hinzufügen`.

Danach erscheint die App mit eigenem Icon auf deinem Home-Bildschirm.

## Offline-Nutzung

Nachdem du die App mindestens einmal mit Internetverbindung geöffnet hast,
werden die nötigen Dateien gespeichert. Danach kann die App auch ohne
Internetverbindung funktionieren.

## Änderungen veröffentlichen

Wenn du später Sprüche oder Design änderst, lade einfach die geänderte
`index.html` erneut zu GitHub hoch.

Wenn alte Inhalte auf dem iPhone sichtbar bleiben, ändere in `sw.js`
diese Zeile:

    const CACHE_NAME = "spruch-app-v1";

zum Beispiel in:

    const CACHE_NAME = "spruch-app-v2";

Dadurch wird der Offline-Cache erneuert.
