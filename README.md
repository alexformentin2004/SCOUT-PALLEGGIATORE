# Scout Palleggiatore

Web app PWA indipendente, progettata per lo scouting di un palleggiatore da iPhone.

## Pubblicazione su GitHub Pages

1. Crea un repository pubblico, per esempio `scout-palleggiatore`.
2. Carica **il contenuto** di questa cartella nella radice del repository (`index.html`, `app.js`, `sw.js`, `manifest.webmanifest`, icone).
3. In **Settings → Pages → Build and deployment** seleziona **Deploy from a branch**, ramo `main`, cartella `/ (root)`.
4. Apri l'URL HTTPS pubblicato. Su iPhone, apri in Safari e usa **Condividi → Aggiungi alla schermata Home**.

## Funzionalità

- Quattro fondamentali: Alzata, Difesa, Muro, Battuta.
- Disegno con il dito, coordinate metriche e salvataggio automatico.
- Alzate: tipologia, Perfetta/Bassa/Corta/Lunga, sei esiti incluso Errore palleggiatore.
- Difesa: valutazione manuale, zona di riferimento (4,5;3,5), raggio 1,1 m.
- Muro: scelta posizione lungo la rete e tre esiti.
- Battuta: cinque esiti.
- Set, partite, punteggio facoltativo, annulla ultima azione, archivio e cancellazione.
- Statistiche per set, partita e storico, mappe dei punti di arrivo e grafico schematico delle alzate.
- Backup e ripristino JSON; stampa o salvataggio PDF tramite funzione di stampa del browser.
- Offline dopo la prima apertura su HTTPS.

## Note importanti

- I dati vengono memorizzati **solo sul dispositivo** con IndexedDB. Esportare regolarmente il backup JSON.
- I simboli geometrici #, +, /, - delle alzate sono calcolati usando i raggi concordati, ma non sono spacciati per voto tecnico finale: il peso di Bassa/Corta/Lunga non è stato definito. `=` viene assegnato a Errore palleggiatore.
- Il grafico laterale mostra frequenza e destinazione; **non** misura l'altezza fisica delle alzate.
- Per creare un PDF: aprire Statistiche, scegliere il filtro, toccare **PDF / Stampa** e selezionare l'opzione PDF nella schermata di stampa del dispositivo.
- La PWA non sincronizza automaticamente i dati tra iPhone e PC.
