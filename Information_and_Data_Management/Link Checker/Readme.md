# 📑 Portfolioaufgabe: Link Checker in Python

## 🛠️ Arbeitsanweisung

Erstellung eines **Link Checkers** mit entsprechender **Code-Dokumentation in Markdown**.

### 📘 Szenario
Du beginnst neu in einem Unternehmen und wirst unter anderem mit der Pflege der Unternehmenswebseite betraut. Es wurde festgestellt, dass einige Links – insbesondere in den FAQ-Bereichen – nicht mehr funktionieren. Das manuelle Überprüfen aller Links wäre zu zeitaufwendig. Da es sich um eine wiederkehrende Aufgabe handelt, soll ein eigener **Link Checker** entwickelt werden.

### 🔧 Ziel
Entwicklung eines Python-Skripts mit dem Namen `link-checker.py`, welches Links auf Webseiten überprüft und die Ergebnisse dokumentiert.

---

## 🧪 Vorgehensweise

Als Grundlage dient eine Python-Vorlage mit drei wesentlichen Funktionen:

### `get_link_status(link: str) -> tuple`
- **Parameter:** Ein Link als String
- **Rückgabe:** Tupel bestehend aus dem Link und dem ermittelten HTTP-Statuscode

### `extract_http_links(url_list: list[str]) -> dict`
- **Parameter:** Liste von Webseiten-URLs
- **Rückgabe:** Dictionary mit der URL als Key und einer Liste von Tupeln (`(Link, Statuscode)`) als Value

### `save_links_to_markdown(urls: list[str], filepath: str) -> None`
- **Parameter 1:** Liste von URLs
- **Parameter 2:** Pfad zur Ausgabedatei mit `.md`-Endung
- **Funktion:** Erstellt eine Markdown-Datei mit einer Tabelle:
  | Original-URL | Gefundener Link | HTTP-Statuscode |
  |--------------|------------------|------------------|

---

## 🌐 Vorgegebene URLs zur Überprüfung

Folgende Links sollen zur Testung verwendet werden:
- [https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/allgemein](https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/allgemein)
- [https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/personenbezogene-daten](https://www.uni-giessen.de/ub/de/forlehr/fdm/wissenswertes/personenbezogene-daten)

Die URLs können manuell als Liste in das Skript integriert werden. Crawling von Unterseiten ist **nicht erforderlich**.

---

## 📄 Dokumentation

Zusätzlich zum Python-Skript soll eine externe Markdown-Dokumentation (`link-checker-documentation.md`) erstellt werden. Diese enthält:

### 👤 Für Nutzer:innen
- Einfache Anleitung zur Bedienung des Link Checkers
- Erklärung, wie die Markdown-Ausgabe funktioniert

### 👨‍💻 Für Entwickler:innen
- Technische Erklärung des Skripts
- Beschreibung aller Funktionen, Parameter und ihrer Rückgabewerte
- Hinweise zu möglichen Schwächen oder Grenzen der Lösung

---

## ✅ Abgabe und Bewertung

| Kriterium | Punkte |
|----------|--------|
| Funktionierendes Skript mit `.py`-Datei und Markdown-Ausgabe | 4 |
| Abgabe der Markdown-Ausgabe `links.md` | 1 |
| Dokumentation in `link-checker-documentation.md` | 1 |
| Dokumentation für Nutzer:innen verständlich | 3 |
| Dokumentation für Entwickler:innen technisch korrekt und vollständig | 5 |
| Formale Korrektheit (Bezeichner, Variablen etc.) | 1 |
| **Extrapunkt:** Benutzerdefinierte Eingabe von URLs und Ausgabe-Pfad | +1 |

---

## ❗ Alternative Abgabe bei Problemen

Falls Schwierigkeiten bei der Umsetzung bestehen, kann ein erläuternder Text (1–2 Seiten, Deutsch) abgegeben werden, der das eigene Vorgehen und Probleme beim Prompting oder Coden beschreibt.

| Kriterium | Punkte |
|----------|--------|
| Umfang: 1–2 Seiten | 1 |
| Sprachliche/formale Korrektheit | 2 |
| Abgabe des unfertigen Python-Skripts | 2 |
| Chatverlauf mit ChatGPT (optional) | 1 |
| Beschreibung des Vorgehens auf Basis der Aufgabenstellung | 4 |
| Beschreibung der Probleme | 5 |

---

## 📅 Terminplan

- **Start:** Heute, 8:45 Uhr
- **Abgabe:** Dienstag, 30. April 2025, 10:15 Uhr
- **Verbleibende Bearbeitungszeit:** _6 Tage, 13 Stunden_

---

## 📌 Hinweise

- **Eigenständigkeitserklärung** und **Angabe der Hilfsmittel** nicht vergessen (**-3 Punkte**)!
- **Name nicht vergessen** (**-1 Punkt**)!
