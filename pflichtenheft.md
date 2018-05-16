# Anforderungs- und Entwurfsspezifikation ("Pflichtenheft")
Cryptocurrency Algotrader, Sasha Koß, Kristoffer Roßbach


<!-- MarkdownTOC -->

- 1 Einführung
  - 1.1 Beschreibung
    - Projektname: Cryptocurrency Algotrade
    - Projektbeschreibung:
  - 1.2 Ziele
    - Anwendungsbereich
    - Motivation
    - Umfang
    - Marktanforderungen
    - Zielgruppe
    - Abgrenzung
- 2 Anforderungen
  - 2.1 Funktionale Anforderungen
  - 2.2 Nicht-funktionale Anforderungen
    - 2.2.1 Rahmenbedingungen
    - 2.2.2 Betriebsbedingungen
    - 2.2.3 Qualitätsmerkmale
  - 2.3 Graphische Benutzerschnittstelle
  - 2.4 Anforderungen im Detail
    - Schablone für User Stories
    - Beispiel 1
    - Beispiel 2
- 3 Technische Beschreibung
  - 3.1 Systemübersicht
  - 3.2 Softwarearchitektur
  - 3.3 Datenmodell
  - 3.4 Abläufe
  - 3.5 Entwurf
- 4 Projektorganisation
  - 4.1 Annahmen
  - 4.2 Verantwortlichkeiten
  - 4.3 Grober Projektplan
- 5 Anhänge
  - 5.1 Glossar
  - 5.2 Referenzen
  - 5.3 Index

<!-- /MarkdownTOC -->



# 1 Einführung

## 1.1 Beschreibung
### Projektname: Cryptocurrency Algotrade
### Projektbeschreibung:
Die Algotrade Software holt sich die aktuelle Handelshistorie einer Crypto-Börse und erstellt anhand dieser Daten eine Candlestick-Chart.
Zeitgleich werden mit den berechneten Candlesticks verschiedene technische Indikatoren ermittelt.

Die Indikatoren werden zur Umsetzung der vom Benutzer konfigurierten Marktstrategie verwendet. Der Benutzer kann die Grenzen für jeden Indikator individuell einstellen und eine Marktentscheidung(Buy/Hold/Sell) damit verknüpfen. Die Positionsgröße wird anhand der Depoteinlage ermittelt, der Benutzer kann dazu einen prozentualen Bereich konfigurieren.

Der Benutzer muss ein Konto mit Einlage auf der jeweiligen Börse besitzen, weil die Algotrade Software die Entscheidungen per API-Request durchführt.



## 1.2 Ziele
### Anwendungsbereich
Der Algotrader wird
### Motivation
Die Blockchain bzw. der Cryptocurrencymarkt befindet sich seit 2015 in einer starken und volatilen Wachstumsphase, deswegen kann ein Einstieg in diesen Markt für risikofreudige Unternehmer lukrativ sein.
### Umfang
Die Software wird im ersten Entwicklungsschritt nur mit der Binance API funktionieren, weil diese kostenlos verwendbar ist und eine vergleichbar gute Performance liefert.
### Marktanforderungen
Der Markt ist noch relativ Jung, dementsprechend schlecht sind vergleichbare Produkte am Markt.

### Zielgruppe
Die Software ist für Anwender konzipiert die ein Grundverständnis von Markttechnik besitzen und eine indivudelle Marktstrategie an einer Cryptobörse umsetzen wollen.
### Abgrenzung
Die Software wird keine weiteren

# 2 Anforderungen

## 2.1 Funktionale Anforderungen
    - Use-Case Diagramme
    - Strukturierung der Diagramme in funktionale Gruppen

## 2.2 Nicht-funktionale Anforderungen

### 2.2.1 Rahmenbedingungen
    - Normen, Standards, Protokolle, Hardware, externe Vorgaben

### 2.2.2 Betriebsbedingungen
    - Vorgaben des Kunden (z.B. Web Browser / Betriebssystem Versionen, Programmiersprache)

### 2.2.3 Qualitätsmerkmale
    - Externe Qualitätsanforderungen (z.B. Performance, Sicherheit, Zuverlässigkeit, Benutzerfreundlichkeit)

## 2.3 Graphische Benutzerschnittstelle
    - GUI-Mockups passend zu User Stories
    - Modellierung der Navigation zwischen den Screens der GUI-Mockups als Zustandsdiagramm

## 2.4 Anforderungen im Detail
    - User Stories mit Akzeptanzkritierien
    - Optional: Name (oder ID) und Priorität ("Must", "Should", "Could", "Won't")
    - Strukturierung der User Stories in funktionale Gruppen

### Schablone für User Stories

| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Wer | Was | Warum | Wann akzeptiert |

### Beispiel 1

| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Benutzer | bei Fehleingabe die Lösung angezeigt bekommen | ich lernen kann | Lösung wird angezeigt |

### Beispiel 2

| **Name**| **In meiner Rolle als**...|   ...**möchte ich**...   | ..., **so dass**... | **Erfüllt, wenn**... | **Priorität**   |
|:-----|:----------:|:-------------------|:-------------|:---------|:----------------|
| Lernen  |Benutzer| bei Fehleingabe die Lösung angezeigt bekommen|ich lernen kann| Lösung wird angezeigt | Muss |


# 3 Technische Beschreibung

## 3.1 Systemübersicht
    - Systemarchitekturdiagramm ("Box-And-Arrow" Diagramm)
    - Schnittstellenbeschreibung
    - Kommunikationsprotokolle, Datenformate

## 3.2 Softwarearchitektur
    - Darstellung von Softwarebausteinen (Module, Schichten, Komponenten)

## 3.3 Datenmodell
    - Konzeptionelles Analyseklassendiagramm

## 3.4 Abläufe
    - Aktivitätsdiagramme für relevante Use Cases
    - Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases

## 3.5 Entwurf
    - Detaillierte UML-Diagramme für relevante Softwarebausteine

# 4 Projektorganisation

## 4.1 Annahmen
    - Nicht durch den Kunden definierte spezifische Annahmen, Anforderungen und Abhängigkeiten
    - Verwendete Technologien (Programmiersprache, Frameworks, etc.)
    - Einschränkungen, Betriebsbedingungen und Faktoren, die die Entwicklung beeinflussen (Betriebssysteme, Entwicklungsumgebung)
    - Interne Qualitätsanforderungen (z.B. Softwarequalitätsmerkmale wie z.B. Erweiterbarkeit)

## 4.2 Verantwortlichkeiten
    - Zuordnung von Personen zu Softwarebausteinen aus Kapitel 3.1 und 3.2
    - Rollendefinition und Zuordnung

## 4.3 Grober Projektplan
    - Meilensteine

# 5 Anhänge

## 5.1 Glossar
    - Definitionen, Abkürzungen, Begriffe

## 5.2 Referenzen
    - Handbücher, Gesetze

## 5.3 Index



