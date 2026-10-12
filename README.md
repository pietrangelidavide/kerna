# Kerna Studio

Sito di una pagina di Kerna Studio, studio di sviluppo software. HTML e CSS puri: nessun framework, nessuno script, nessun cookie.

## Contenuto

- `index.html`, `style.css`: la pagina e il suo stile
- `fonts/`: Outfit e JetBrains Mono, ospitati nel sito (nessuna richiesta a servizi esterni)
- `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`: icone
- `og.png`: immagine per le anteprime sui social (1200×630)
- `robots.txt`

## Come metterlo online

Il dominio è **kernastudio.com** (già impostato in `canonical`, `og:url` e `og:image` di `index.html`). Il sito è pensato per **Cloudflare Pages** (gratuito): `index.html` sta nella radice della repo, quindi non serve nessuna impostazione di build.

1. Cloudflare → *Workers & Pages* → *Create* → *Pages* → *Connect to Git* → repo `kerna`, branch `main`.
2. Comando di build: vuoto. Cartella di output: vuota (la radice).
3. Dopo il primo deploy: *Custom domains* → *Set up a custom domain* → `kernastudio.com` (e `www.kernastudio.com`). Cloudflare crea da solo i record DNS e l'HTTPS.

Ogni push su `main` ripubblica il sito. Va bene anche un altro hosting statico (GitHub Pages, Netlify).

## Da fare

- **Piè di pagina:** aggiungere ragione sociale, partita IVA e sede legale. In fondo a `index.html` c'è un commento che indica il punto.

## Contatto

Il pulsante "Scrivici" apre la chat Instagram di `@kernastudio`. Per cambiare profilo, sostituire `kernastudio` nei link `https://ig.me/m/…` e `https://www.instagram.com/…` in `index.html`.
