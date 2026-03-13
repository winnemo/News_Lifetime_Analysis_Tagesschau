# News Lifetime Analysis — Tagesschau.de

Analyse der Lebensdauer von Nachrichtenthemen auf Basis des [Awesome Tagesschau](https://huggingface.co/datasets/stefan-it/awesome-tagesschau) Datensatzes (56.896 Artikel, 2005–2025).

**Modul:** Big Data   
**Autoren:** Elezi Kleris · Winnemöller Moritz · Wittmann Fritz  

## Forschungsfragen

- Wie lange bleiben Nachrichtenthemen auf tagesschau.de aktiv?
- Unterscheiden sich Lifetimes nach Ressort (Inland, Ausland, Wirtschaft)?
- Welche Themen sind „Eintagsfliegen", welche „Dauerbrenner"?
- Wie sehen die Verteilungen unterhalb der Aggregationsebene aus?

## Methoden

Drei Ansätze zur Messung von News Lifetimes:

1. **Einfache Lifetime** — Zeitspanne vom ersten bis letzten Artikel pro Tag (Baseline)
2. **Gap-basierte Fenster** — Zusammenhängende Berichterstattungszeiträume (Gap-Schwelle: 14 Tage)
3. **Attention Decay** — Normalisierte Intensität nach dem Peak (vgl. Wu & Huberman, 2007)

## Quickstart

```bash
# Repository klonen
git clone https://github.com/winnemo/News_Lifetime_Analysis_Tagesschau.git
cd News_Lifetime_Analysis_Tagesschau

# Abhängigkeiten installieren
pip install -r requirements.txt

# Notebook starten
jupyter notebook NewsLifetimeAnalysisTagesschau.ipynb
```

## Abhängigkeiten

- Python ≥ 3.10
- pandas
- matplotlib
- seaborn
- huggingface_hub
- jupyter

Siehe `requirements.txt` für die vollständige Liste.

## Datensatz

Der Datensatz wird automatisch über die HuggingFace-API (`snapshot_download`) geladen.  
Quelle: [stefan-it/awesome-tagesschau](https://huggingface.co/datasets/stefan-it/awesome-tagesschau)