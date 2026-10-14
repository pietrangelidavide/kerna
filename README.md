# ENA ONE STUDIO · sito

Sito di una pagina di ENA ONE STUDIO: siti, app e AI. HTML e CSS puri, nessun framework, nessuno script, nessun cookie.

## Contenuto

La cartella `public/` è il sito; fuori ci sono solo questo README e `wrangler.jsonc` (configurazione di Cloudflare).

- `public/index.html`, `public/style.css`: pagina e stile (dati strutturati per Google già dentro la pagina)
- `public/fonts/`: Bricolage Grotesque Regular e Bold, ospitati nel sito (nessuna richiesta a servizi esterni)
- `public/img/`: logo orizzontale e logo con descrittore
- `public/favicon.svg`, `favicon-32.png`, `favicon-192.png`, `favicon-512.png`, `apple-touch-icon.png`, `site.webmanifest`: icone
- `public/og.png`: immagine per le anteprime sui social (1200×630)
- `public/robots.txt`, `public/sitemap.xml`

## Come funziona la pubblicazione

Il sito è su Cloudflare (gratuito, file statici serviti da `public/`, nessuna build). Ogni push su `main` ripubblica il sito.

- Comando di build: vuoto. Comando di deploy: `npx wrangler deploy`.
- Il `name` in `wrangler.jsonc` deve essere uguale al nome del progetto su Cloudflare. Se rinomini il progetto su Cloudflare, cambia anche quello.

## Quando cambi dominio

Gli indirizzi dentro i file puntano al dominio attuale. Con il nuovo dominio, sostituisci il vecchio indirizzo (con `www.`) in tre file: `public/index.html` (canonical, Open Graph, dati strutturati), `public/robots.txt` e `public/sitemap.xml`. Poi su Cloudflare: *Settings* → *Domains & Routes* → *Add* → *Custom domain*, e un reindirizzamento 301 dal dominio senza `www` a quello con `www`. Il vecchio indirizzo, se resta attivo, va reindirizzato (301) al nuovo e tenuto per almeno dodici mesi.

## Prima di dichiarare il lavoro finito

1. **Profilo Instagram.** I pulsanti usano `@ena_one_studio` (link `https://ig.me/m/ena_one_studio`). Se cambi nome utente, sostituisci `ena_one_studio` nei link `ig.me/m/…` e `instagram.com/…` in `index.html`.
2. **Marchio.** Prima di stampare o spendere, fai una ricerca di anteriorità del nome su TMview o UIBM (classi 9, 35 e 42). Non è una consulenza legale.
3. **Piè di pagina.** Aggiungere ragione sociale, partita IVA e sede legale: in fondo a `index.html` c'è un commento che indica il punto. Se aggiungi moduli o strumenti di misura serve anche l'informativa privacy.
4. **Anteprima gratuita.** Il sito dice «prima di impegnarti vedi un'anteprima» senza dire se è gratuita. Se lo è, scrivilo nelle domande frequenti (e nei dati strutturati, nello stesso blocco in cima alla pagina).

## Colori e caratteri

Inchiostro `#0D0F14`, Carta `#F5F6F8`, Segnale `#FFC21A`, Grafite `#5C6270` (`#A3A9B5` su fondo scuro). Regola: un solo accento, il giallo. Caratteri: Bricolage Grotesque Bold per i titoli, Regular per i testi.
