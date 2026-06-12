# L'Enigmista 🔍

PWA per scovare (e nascondere) messaggi dentro i testi, in italiano. Parte della collezione PezzaliAPP.

**100% gratuita**: nessuna API, nessun server, nessun tracciamento, nessun costo.
Tutta l'analisi avviene nel browser e l'app funziona anche offline.

## Cosa fa

**Decifra** — incolla un articolo o un testo qualsiasi (tre esempi inclusi: articolo, poesia, lettera):
- **Anagrammi**: parole del testo le cui lettere formano altre parole
- **Acrostici**: parole nascoste nelle iniziali di frasi, righe e parole
- **Frase nascosta**: trova il frammento più corto che contiene tutte le lettere di una frase cercata
- **Oracolo**: parole che emergono leggendo una lettera ogni N
- **Condividi i risultati** con un tocco (Web Share / copia negli appunti)
- Box "Perché trovo quasi sempre qualcosa?" che spiega l'effetto statistico

**Scrittoio** — nascondi tu un messaggio: scrittura guidata frase per frase,
con verifica in tempo reale (tessere verdi/rosse) e suggerimento sulla prossima lettera.

**Anagrammi** — dato un nome o una frase (4–18 lettere), trova anagrammi
di una o due parole usando tutte le lettere.

Dizionario incorporato: ~60.000 parole italiane dalla lista open source
[napolux/paroleitaliane](https://github.com/napolux/paroleitaliane).

## Pubblicazione su GitHub Pages

1. Carica tutti i file di questa cartella nella radice della repo `enigmista`
2. Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, cartella `/ (root)`
3. L'app sarà su `https://<tuo-utente>.github.io/enigmista/`
4. Da smartphone: apri l'URL → "Aggiungi a schermata Home" per installarla

## Privacy

Nessun dato lascia il dispositivo: niente analytics, niente cookie, niente richieste di rete
dopo il primo caricamento. Il service worker conserva l'app in cache per l'uso offline.

## Struttura

```
index.html      app completa (dizionario incluso)
manifest.json   manifest PWA
sw.js           service worker (cache offline, v1.2)
icons/          icone 192/512 + apple-touch-icon
LICENSE         MIT
```

## Licenza

MIT — vedi [LICENSE](LICENSE).
