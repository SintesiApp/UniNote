# 📁 UNINOTE — Cartella progetto

Tutto quello che riguarda l'app **UniNote** organizzato in un unico posto.

---

## 📂 Struttura cartelle

```
UNINOTE/
├── app/
│   └── UniNote.html          ← FILE PRINCIPALE, versione attuale dell'app
├── documentazione/
│   └── DISTRIBUZIONE.md      ← Come pubblicare su Windows/Android/iOS
└── versioni-precedenti/
    ├── JWLFusion_v1.html     ← Prima versione (nome prima del rebranding)
    └── JWLMerge_v1.0_Python.zip  ← Primissima versione (Python desktop, abbandonata)
```

---

## 🌐 Dove è pubblicata l'app

**Netlify (online, link da condividere):**
https://uninote-app.netlify.app

**GitHub (codice sorgente):**
https://github.com/maxritaoliva-source/UniNote

---

## ℹ️ Cos'è UniNote

App web (PWA) che unisce file di backup `.jwlibrary` di JW Library
provenienti da dispositivi diversi (iPhone, Android, Windows),
creando un unico file con tutte le note, evidenziazioni e segnalibri,
senza duplicati.

**Caratteristiche principali:**
- 100% locale — nessun dato inviato a server esterni
- Funziona su Windows, Android, iPhone (browser o installata come app)
- Gestione conflitti: tieni A, tieni B, tieni entrambe, o unisci il testo
- Pulsante "Unisci tutto" per risolvere conflitti in blocco
- Donazioni volontarie via Ko-fi (ko-fi.com/jocher)

---

## 🔧 Come aggiornare l'app online

1. Modifica `app/UniNote.html`
2. Vai su **app.netlify.com** → progetto **uninote-app** → **Deploys**
3. Trascina il file aggiornato
4. Il sito si aggiorna in 1-2 minuti

---

## 📝 Note tecniche

- Stack: HTML singolo file, JSZip + SQL.js (via CDN) per leggere/scrivere `.jwlibrary`
- Nessuna build richiesta — è un file pronto all'uso
- Service Worker incluso per funzionamento offline dopo il primo caricamento
