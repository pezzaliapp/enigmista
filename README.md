# L'Enigmista 🔍

PWA per scovare (e nascondere) messaggi dentro i testi, in italiano. Parte della collezione PezzaliAPP.

## Cosa fa

**Decifra** — incolla un articolo o un testo qualsiasi:
- **Anagrammi**: parole del testo le cui lettere formano altre parole
- **Acrostici**: parole nascoste nelle iniziali di frasi, righe e parole
- **Frase nascosta**: trova il frammento più corto che contiene tutte le lettere di una frase cercata
- **Oracolo**: parole che emergono leggendo una lettera ogni N

**Scrittoio segreto** — nascondi tu un messaggio:
- *Scrivo io, guidami*: scrittura assistita frase per frase, con verifica in tempo reale
- *Riscrivi tu il mio testo*: l'AI riscrive il tuo testo nascondendo il messaggio nelle iniziali delle frasi, con verifica automatica

Dizionario incorporato: ~60.000 parole italiane dalla lista open source
[napolux/paroleitaliane](https://github.com/napolux/paroleitaliane). Funziona offline.

## Pubblicazione su GitHub Pages

1. Carica tutti i file di questa cartella nella radice della repo `enigmista`
2. Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, cartella `/ (root)`
3. L'app sarà su `https://<tuo-utente>.github.io/enigmista/`
4. Da smartphone: apri l'URL → "Aggiungi a schermata Home" per installarla

## Nota sulla riscrittura AI

La funzione "Riscrivi tu il mio testo" chiama l'API Anthropic. Nella versione che gira dentro
Claude funziona automaticamente; sulla versione web/PWA serve una chiave API personale,
da inserire in "Impostazioni AI" (resta in memoria, non viene salvata). Tutto il resto
dell'app funziona senza chiave e senza connessione.

## Struttura

```
index.html      app completa (dizionario incluso)
manifest.json   manifest PWA
sw.js           service worker (cache offline)
icons/          icone 192/512 + apple-touch-icon
```
