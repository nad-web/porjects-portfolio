# Link Checker Dokumentation
  ***Bearbeitet von Noorullah Adel, Matrikelnummer: -------, am 24.04.2025*** <br>
<span style="background-color: yellow">Portfolioaufgabe Markdown</span>

 
## Inhaltsverzeichnis

- [Einführung](#einführung)
- [Nutzung als Endnutzer](#nutzung-als-endnutzer)
  - [Voraussetzungen](#voraussetzungen)
  - [Verwendung](#verwendung)
  - [Beispiel](#beispiel)
- [Nutzung für Programmierer](#nutzung-für-programmierer)
  - [Funktionen](#funktionen)
    - [`get_link_status(link)`](#get_link_statuslink)
    - [`extract_http_links(urls)`](#extract_httplinksurls)
    - [`save_links_to_markdown(urls, file_path)`](#save_links_to_markdownurls-file_path)
  - [Beispiel](#beispiel-1)
  - [Grenzen und Schwächen](#grenzen-und-schwächen)
- [Fazit](#fazit)
- [Autor](#autor)
- [Hilfsmittel](#hilfsmittel)
- [Eigenständigkeitserklärung](#eigenständigkeitserklärung)

## Einführung

Der Link Checker ist ein Python-Skript, das HTTP-Links von einer oder mehreren Webseiten extrahiert und deren Status überprüft. Das Ergebnis wird in einer Markdown-Tabelle gespeichert. Diese Dokumentation richtet sich sowohl an Endnutzer, die ihre Links einfach überprüfen möchten, als auch an Programmierer, die die Funktionen des Skripts nachnutzen möchten.

## Nutzung als Endnutzer

### Voraussetzungen

Um den Link Checker zu verwenden, müssen Sie Python installiert haben. Außerdem benötigen Sie die folgenden Bibliotheken:
- `requests`
- `beautifulsoup4`
- `markdown`

Sie können diese Bibliotheken mit `pip` installieren:

 
```bash 
pip install requests beautifulsoup4 markdown
 
``` 

### Verwendung

1. **Skript herunterladen**: Laden Sie das Skript herunter und öffnen Sie es in einem Texteditor.
2. **URLs definieren**: Ändern Sie die Liste `urls` im Skript, um die Webseiten anzugeben, von denen Sie die Links überprüfen möchten.
3. **Ausgabedatei definieren**: Ändern Sie den Dateinamen im Aufruf der Funktion `save_links_to_markdown`, um die gewünschte Ausgabedatei anzugeben.
4. **Skript ausführen**: Führen Sie das Skript aus, indem Sie im Terminal den Befehl `python script_name.py` ausführen (ersetzen Sie `script_name.py` durch den Namen Ihres Skripts).

### Beispiel

 
```python 
urls = ['https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/allgemein',
        'https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/personenbezogene-daten']
save_links_to_markdown(urls, 'links.md')
 
``` 

Nach dem Ausführen des Skripts wird eine Datei `links.md` erstellt, die eine Markdown-Tabelle mit den überprüften Links und ihren Statuscodes enthält.

## Nutzung für Programmierer

### Funktionen

#### `get_link_status(link)`

Diese Funktion überprüft den Status eines Links.

- **Parameter**:
  - `link` (str): Der zu überprüfende Link.
- **Rückgabewert**:
  - Ein Tupel `(link, status_code)`, wobei `status_code` der HTTP-Statuscode des Links ist.

#### `extract_http_links(urls)`

Diese Funktion extrahiert alle HTTP-Links von einer oder mehreren Webseiten und überprüft deren Status.

- **Parameter**:
  - `urls` (list): Eine Liste von URLs, von denen die Links extrahiert werden sollen.
- **Rückgabewert**:
  - Ein Dictionary, das die URLs als Schlüssel und eine Liste von Tupeln `(link, status_code)` als Werte enthält.

#### `save_links_to_markdown(urls, file_path)`

Diese Funktion extrahiert die Links von den angegebenen URLs, überprüft deren Status und speichert das Ergebnis in einer Markdown-Datei.

- **Parameter**:
  - `urls` (list): Eine Liste von URLs, von denen die Links extrahiert werden sollen.
  - `file_path` (str): Der Pfad zur Ausgabedatei.
- **Rückgabewert**:
  - Kein Rückgabewert. Das Ergebnis wird direkt in die angegebene Datei geschrieben.

### Beispiel

 
```python 
urls = ['https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/allgemein',
        'https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/personenbezogene-daten']
save_links_to_markdown(urls, ‘links.md')
 
``` 

### Grenzen und Schwächen

- **HTTP-Links**: Das Skript extrahiert nur HTTP-Links (`http://` oder `https://`).
- **Performance**: Bei einer großen Anzahl von Links kann das Skript langsam werden. Es wird empfohlen, die Anzahl der Links zu begrenzen oder asynchrone Anfragen zu verwenden, um die Performance zu verbessern.

## Fazit

Der Link Checker ist ein nützliches Tool, um den Status von Links auf Webseiten zu überprüfen. Es kann sowohl von Endnutzern als auch von Programmierern verwendet werden, um die Integrität von Links zu gewährleisten.

## Autor
Noorullah Adel, Matrikelnummer: 8220190
## Hilfsmittel
Zur Unterstützung und Bearbeitung der Aufgabe wurden folgende Hilfsmittel genutzt:
* Python-Programmiersprache
* Python-Bibliotheken (requests,beautifulsoup4,markdown)
* Visual Studio Code als IDE "Entwicklungsumgebung"
* KI-Tools

## Eigenständigkeitserklärung

