🧾 DKVAI– Analizzatore automatico PDF DKV

dkvAI è un programma che prende i file PDF delle fatture DKV (relative alle spese di carburante, pedaggi e servizi) e genera in automatico resoconti dettagliati in formato tabellare o CSV.
L’obiettivo è automatizzare la gestione dei costi di gasolio e spese aziendali, evitando di dover copiare manualmente i dati da ogni fattura.

⚙️ Funzionalità principali

📂 Estrazione automatica dei dati da file PDF DKV

🧮 Riconoscimento intelligente delle tabelle (carburante, pedaggi, spese accessorie, ecc.)

📊 Creazione di resoconti riepilogativi per data, tipo di spesa o veicolo

💾 Esportazione dei risultati in formato .csv o .xlsx

🕵️‍♂️ Analisi automatica degli importi, IVA e sconti

⚡ Elaborazione multipla di più PDF in un’unica esecuzione

🔧 Installazione
Clona il repository:
git clone https://github.com/alexvandi/dkv.git
cd dkv

Installa le dipendenze:
pip install -r requirements.txt
(Opzionale) Crea un ambiente virtuale Python:
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows

🚀 Utilizzo
Inserisci i file PDF DKV nella cartella input/
Esegui il programma:
python main.py

Troverai i risultati elaborati nella cartella output/ come file .csv o .xlsx
Esempio di output CSV:
Data;Tipo;Importo Netto;IVA;Importo Totale
2025-01-10;Gasolio;78.50;17.27;95.77
2025-01-11;Pedaggio;24.30;5.35;29.65
2025-01-12;Lavaggio;12.00;2.64;14.64

🧩 Architettura
PDF Parser: Estrae le tabelle e normalizza i dati (usa pdfplumber o PyMuPDF)
Analyzer: Calcola totali, medie e sconti per categoria
Exporter: Salva i risultati in CSV o Excel
Interface (CLI o GUI): Permette di selezionare i PDF e visualizzare i risultati

🧪 Test
Esegui i test automatici:
pytest

📄 Licenza
Questo progetto è rilasciato sotto licenza.
Puoi utilizzarlo, modificarlo ma non distribuirlo per scopo di lucro.
