🗞️ Progetto Frontend: Mockup "Quotidiano Online"
Questo è un progetto frontend che ho realizzato per simulare l'interfaccia e l'architettura del sito "The Guardian.

✨ Funzionalità principali

🌗 Dark/Light Mode: Gestita tramite variabili CSS (Custom Properties) nel :root.: La preferenza dell'utente viene salvata nel localStorage del browser per mantenerla attiva anche aggiornando la pagina.

📏 Reading Progress Bar: Una barra fissa in alto che si riempie man mano che si scrolla l'articolo, ottimizzata per non pesare sulle performance.

🖼️ Lazy Loading avanzato: Oltre all'attributo nativo loading="lazy", ho implementato un fallback con IntersectionObserver per gestire il caricamento delle immagini solo quando si avvicinano al viewport.

📱 Menu Mobile e Overlay di ricerca: Layout completamente responsivo. Su mobile il menu principale si trasforma in una comoda sidebar a scorrimento laterale.

📰 Ticker "Breaking News": Un banner animato (marquee) realizzato in puro CSS, che si mette in pausa quando ci passi sopra con il mouse (per facilitare la lettura).

🗂️ Tab Interattive: Una sezione "Most Popular" con tab ("Most viewed" e "Deeply read") completamente navigabile anche da tastiera.

🧠 Scelte tecniche interessanti (Cose di cui vado fiero)
Se dai un'occhiata al codice sorgente, noterai alcune chicche:

Architettura CSS Mista (Grid + Flexbox): Ho usato Flexbox per i menu e gli allineamenti lineari (1D), ma per le griglie complesse degli articoli ho sfruttato la potenza di CSS Grid (es. .g4, .g3). È incredibile quanto codice risparmi gestendo i breakpoint responsivi direttamente con Grid.

Performance dello Scroll: Agli EventListener legati allo scroll (come la progress bar e l'header sticky) ho passato l'opzione { passive: true }. Questo dice al browser di non bloccare il rendering in attesa di calcoli JS, rendendo lo scroll fluido e senza scatti ("jank-free"), specialmente su smartphone.

Sicurezza dello Scope (IIFE): Tutto il codice JavaScript è racchiuso all'interno di una Immediately Invoked Function Expression (IIFE) e usa 'use strict'. Questo evita di inquinare lo scope globale di window e previene conflitti con eventuali script futuri.

Accessibilità (A11y): Non ho trascurato chi usa gli screen reader. Ho inserito classi .sr-only per nascondere visivamente le etichette necessarie, uno "skip link" nascosto all'inizio della pagina, e abbondante uso di attributi aria-label, aria-hidden e aria-expanded.
