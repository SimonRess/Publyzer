

# App Name - Ideas

- => **Publyzer**: Eine Wortkreation aus „Publication“ und „Analyzer“, die den analytischen Aspekt betont.

- **ScholarStream**: Betont den kontinuierlichen Fluss von wissenschaftlichen Inhalten.

- **AcadFeed**: Verbindet „Academic“ und „Feed“ und signalisiert so einen Newsfeed für akademische Publikationen.

- **ResearchPulse**: Hebt hervor, dass Sie stets den Puls der Forschung fühlen und aktuelle Trends erkennen.

- **InsightScholar**: Vermittelt, dass die App tiefgehende Einblicke in den Stand der Wissenschaft bietet.

- **KnowFeed**: Kombiniert „Knowledge“ und „Feed“, um die kontinuierliche Versorgung mit Wissen zu verdeutlichen.

- **ResearchRadar**: Stellt dar, dass Ihre App wie ein Radar den aktuellen Stand von Forschungsfragen erfasst.

- **AcadContent**: Fokussiert auf die Bereitstellung von Inhalten aus dem akademischen Bereich.

- **ScienceSync**: Signalisiert, dass die App die neuesten wissenschaftlichen Inhalte synchronisiert und zusammenführt.

- **ResearchFlow**: Unterstreicht den fließenden, kontinuierlichen Zugriff auf Forschungsergebnisse und Publikationen.


# App functionalities

## 1. Automatisches Abrufen von Inhalten:
- Periodisches Abrufen der neuesten Inhalte basierend auf vordefinierten Suchanfragen.
- Web Scraping von spezifischen Webseiten oder Nutzung von APIs zur Datenextraktion.

## 2. Datenverarbeitung und -analyse:
- Kategorisierung der abgerufenen Inhalte nach Themen oder Schlagworten.
- Zusammenfassung der Inhalte zur Hervorhebung der wichtigsten Informationen.
- Beantwortung spezifischer Fragen basierend auf den extrahierten Daten.
  
## 3. Automatisierung und Hosting:
- Periodische Ausführung der Datenabruf- und Verarbeitungsprozesse.
- Hosting des Projekts auf GitHub mit automatisierten Workflows.

## 4. Ausblick

## 4.1 RAG: Vektorisierung  

### 4.2 Veröffentlichung der Insights
- Automatische Erstellung von Research Reports zu Research-Queries / -Topics
- Automitsiche Diskussion neuster Insights per automatisch erstellten KI-Podcasts


# Technology Stack

## 1.Backend: Web Scraping Frameworks
Aufgabe: Abrufen von Inhalten aus Webseiten auf Basis von Search Queries

 **[Scrapy](https://github.com/scrapy/scrapy)**
- Ein weit verbreitetes, robustes und flexibles Framework für Web Crawling und Scraping.
  
**[Beautiful Soup](https://pypi.org/project/beautifulsoup4/)**
- Ideal für kleinere Projekte oder als Ergänzung zu Requests für das Parsen von HTML/XML.
  
**[ScrapegraphAI](https://github.com/ScrapeGraphAI/Scrapegraph-ai)**
- Ein moderner Ansatz, bei dem LLMs (große Sprachmodelle) zur Interpretation und Extraktion von Webinhalten genutzt werden – besonders geeignet, wenn semantische Informationen benötigt werden.

*Alternativen:*
- **Selenium**: Für dynamische Webseiten, die stark auf JavaScript setzen.
- **Requests-HTML**: Für einfachere Projekte, die ein schlankes, aber effektives Rendering von HTML benötigen.


## 2. Backend: Persistenz / Datenspeicherung
Aufgabe: Speichern und Verwalten der extrahierten und verarbeiteten Daten

Relationale Datenbanken:
- **SQLite:** Einfach und ideal für kleinere Projekte bzw. Prototypen.
- **PostgreSQL**: Leistungsstark und ideal für produktionsreife Anwendungen.
- **MySQL**: Eine weit verbreitete Alternative, die robust und skalierbar ist.

NoSQL-Datenbanken:
- **MongoDB**: Für flexible, dokumentenbasierte Speicherung von unstrukturierten Daten.
- **Redis**: Als schneller Cache oder für einfache Key-Value-Speicherlösungen.

ORM/Abstraktion:
- SQLAlchemy: Um den Datenbankzugriff in Python zu vereinfachen und zu abstrahieren.

Cloud Storage:
- Amazon S3, Google Cloud Storage oder Azure Blob Storage: Für die Speicherung großer Datenmengen oder als Backup-Lösung.

Alternative:
- Elasticsearch: Falls auch Volltextsuche über die gespeicherten Inhalte benötigt wird.



## 3. Backend: Datenverarbeitung und -analyse:
Aufgabe: Extrahierte Rohdaten validieren (pydantic und PydanticAI), aufbereiten und in strukturierte Modelle überführen (Pandas) und mittels AI/LLMs analysieren (llamaindex und LangChain).

**Pandas**: 
- Eine Bibliothek zur Datenmanipulation und -analyse, die den Umgang mit Tabellenstrukturen erleichtert.

**pydantic:**
- Ein Python-Paket für Datenvalidierung und Settings-Management mittels Type Hints.
- Es hilft dabei, sicherzustellen, dass Daten (z. B. von Web-Scrapern oder APIs extrahierte Inhalte) einem vordefinierten Schema entsprechen.
- Dies erleichtert die Verarbeitung und Integration der Daten in weitere Verarbeitungsschritte.

**LangChain:** 
- Ein Framework zur Integration großer Sprachmodelle (LLMs) in Anwendungen.
- Es unterstützt Aufgaben wie Zusammenfassungen, Fragebeantwortung und die Orchestrierung von LLM-gestützten Workflows, indem es externe Datenquellen mit dem Modell verknüpft.

**llamaindex**
- Eine Bibliothek (früher bekannt als GPT Index), die es ermöglicht, externe Dokumente und Datenquellen in einen durchsuchbaren Index zu überführen.
- So können LLMs effizient auf umfangreiche, unstrukturierte Daten zugreifen, sie abrufen und verarbeiten – ideal beispielsweise für das Erstellen von Zusammenfassungen oder die Beantwortung spezifischer Fragen aus großen Datensammlungen.

**PydanticAI:**
- Eine Erweiterung von pydantic, die speziell auf den Einsatz im Kontext von KI-Anwendungen abzielt.
- PydanticAI bietet zusätzliche Validierungsfunktionen und Typen, um beispielsweise die Ausgaben von LLMs automatisch gegen vordefinierte Datenmodelle zu prüfen – so lassen sich robuste, vorhersehbare Pipelines zur Datenverarbeitung und -integration aufbauen.


## 4. Frontend: Weboberfläche / UI
Aufgabe: Erstellung einer Weboberfläche zur Verwaltung und Anzeige der extrahierten und verarbeiteten Daten

**Flask:**
- Ein leichtgewichtiges Python-Webframework, ideal für schnelle und einfache Web-UIs.
  
**Django:**
- Ein umfassendes Framework, das sowohl eine robuste Backend-Struktur als auch eingebaute Template-Engines bietet.
  
**FastAPI:**
- Modern und performant, besonders geeignet für RESTful-APIs und interaktive Dokumentation (z. B. mit Swagger UI).
  
**Streamlit:**
- Speziell für Data-Science- und Analyseanwendungen entwickelt – ermöglicht es, interaktive Dashboards schnell zu erstellen.

*Alternative:*
- Dash (von Plotly): Für interaktive Datenvisualisierungen und Dashboards.
- Panel (HoloViz): Für die Erstellung von Web-Apps zur Datenanalyse.



## 4. Automatisierung / CI/CD und Ausführung
Aufgabe: Periodisches Ausführen des Python-Skripts und Deployment über GitHub

**GitHub Actions:**
- Bietet CI/CD-Funktionalitäten, mit denen Sie Workflows für das periodische Ausführen von Aufgaben wie Datenabruf und -verarbeitung einrichten können.

**Docker (optional):**
- Docker: Zur Containerisierung der Anwendung für konsistente Umgebungen – besonders nützlich, wenn Abhängigkeiten (z. B. bestimmte Versionen von Python, Bibliotheken) isoliert und reproduzierbar bereitgestellt werden sollen.



## Overview:
- Web Scraping: Scrapy, Beautiful Soup, ScrapegraphAI, (alternativ Selenium / Requests-HTML)
- UI/Frontend: Flask / Django / FastAPI, alternativ Streamlit, Dash oder Panel
- Persistenz: SQLite, PostgreSQL, MySQL, alternativ MongoDB, Redis, SQLAlchemy, Cloud Storage (S3, GCS, Azure Blob) oder Elasticsearch
- Automatisierung & CI/CD: GitHub Actions, mit/ohne Docker (alternativ Podman), Cron-Jobs oder serverless Lösungen wie AWS Lambda




# Implementierungsschritte:

## 1. Projektinitialisierung:
- Erstellen Sie ein neues Git-Repository und richten Sie die grundlegende Projektstruktur ein.

## 2. Datenabruf:
- Implementieren Sie mit Scrapy oder Beautiful Soup die Logik zum Abrufen von Inhalten basierend auf den definierten Suchanfragen.

## 3. Datenverarbeitung:
- Nutzen Sie Pandas für die Datenaufbereitung.
- Verwenden Sie LangChain zur Integration von LLMs für die Kategorisierung, Zusammenfassung und Fragebeantwortung.

## 4. Automatisierung:
- Richten Sie GitHub Actions ein, um die Scraping- und Verarbeitungsprozesse periodisch auszuführen.
- Alternativ können Sie lokale Cron-Jobs oder externe Dienste nutzen, um die Anwendung in festgelegten Intervallen zu starten.

##5. Hosting und Bereitstellung:
- Nutzen Sie GitHub Pages oder andere Hosting-Dienste, um die Ergebnisse bereitzustellen, falls eine Weboberfläche vorgesehen ist.

## 6. Überwachung und Wartung:
- Implementieren Sie Logging und Error-Handling, um den Betrieb der Anwendung zu überwachen und bei Bedarf Anpassungen vorzunehmen.
