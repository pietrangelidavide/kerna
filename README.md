# Kerna Studio

Sito di una pagina di Kerna Studio, studio di sviluppo software. HTML e CSS puri: nessun framework, nessuno script, nessun cookie.

## Contenuto

Il sito vero e proprio sta nella cartella `public/`; fuori ci sono solo questo README e `wrangler.jsonc` (la configurazione di Cloudflare).

- `public/index.html`, `public/style.css`: la pagina e il suo stile
- `public/fonts/`: Outfit e JetBrains Mono, ospitati nel sito (nessuna richiesta a servizi esterni)
- `public/favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`: icone
- `public/og.png`: immagine per le anteprime sui social (1200×630)
- `public/robots.txt`

## Come metterlo online

L'indirizzo principale è **https://www.kernastudio.com** (già impostato in `canonical`, `og:url` e `og:image` di `public/index.html`); `kernastudio.com` senza www reindirizza lì. Il sito è pensato per **Cloudflare** (gratuito, file statici serviti da `public/`, nessuna build).

1. Cloudflare → *Workers & Pages* → *Create application* → *Connect to Git* → repo `kerna`, branch `main`.
2. Nome del progetto: `kernastudio` (deve essere uguale a `name` in `wrangler.jsonc`; se lo cambi, cambia anche quello).
3. Comando di build: vuoto. Comando di deploy: `npx wrangler deploy` (già quello predefinito).
4. Dopo il primo deploy: *Settings* → *Domains & Routes* → *Add* → *Custom domain* → `www.kernastudio.com` e `kernastudio.com`. Cloudflare crea da solo i record DNS e l'HTTPS.
5. Reindirizzamento: dominio `kernastudio.com` → *Rules* → *Redirect Rules* → modello «Redirect from root to WWW» (301), così chi scrive l'indirizzo senza www arriva a quello principale.

Ogni push su `main` ripubblica il sito. Va bene anche un altro hosting statico (GitHub Pages, Netlify): basta servire la cartella `public/`.

## Da fare

- **Piè di pagina:** aggiungere ragione sociale, partita IVA e sede legale. In fondo a `index.html` c'è un commento che indica il punto.

## Contatto

Il pulsante "Scrivici" apre la chat Instagram di `@kernastudio`. Per cambiare profilo, sostituire `kernastudio` nei link `https://ig.me/m/…` e `https://www.instagram.com/…` in `index.html`.
