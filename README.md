# Kerna Studio

Sito di una pagina di Kerna Studio, studio di sviluppo software. HTML e CSS puri: nessun framework, nessuno script, nessun cookie.

## Contenuto

- `index.html`, `style.css`: la pagina e il suo stile
- `fonts/`: Outfit e JetBrains Mono, ospitati nel sito (nessuna richiesta a servizi esterni)
- `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`: icone
- `og.png`: immagine per le anteprime sui social (1200×630)
- `robots.txt`

## Come metterlo online

Va bene qualsiasi hosting per siti statici (GitHub Pages, Cloudflare Pages, Netlify o un hosting tradizionale). `index.html` sta nella radice della repo, quindi non serve nessuna impostazione di build.

## Da fare prima di pubblicare

1. **Piè di pagina:** aggiungere ragione sociale, partita IVA e sede legale. In fondo a `index.html` c'è un commento che indica il punto.
2. **Dominio:** quando c'è, in `index.html` togliere i commenti al blocco `canonical / og:image` e sostituire `IL-TUO-DOMINIO` con l'indirizzo vero.

## Contatto

Il pulsante "Scrivici" apre la chat Instagram di `@kernastudio`. Per cambiare profilo, sostituire `kernastudio` nei link `https://ig.me/m/…` e `https://www.instagram.com/…` in `index.html`.
