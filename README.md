Questo è un progetto frontend che ho realizzato per simulare l’interfaccia e l’architettura del sito “The Guardian”.

Funzionalità principali: 
  1) Dark/Light Mode: Gestita tramite variabili CSS (Custom Properties) nel :root.: La preferenza dell’utente viene salvata nel localStorage del browser per mantenerla attiva anche aggiornando la pagina.
  2) Reading Progress Bar: Una barra fissa in alto che si riempie man mano che si scrolla l’articolo, ottimizzata per non pesare sulle performance.
  3) Lazy Loading avanzato: Oltre all’attributo nativo loading=”lazy”, ho implementato un fallback con IntersectionObserver per gestire il caricamento delle immagini solo quando si avvicinano al viewport.
  4) Menu Mobile e Overlay di ricerca: Layout completamente responsivo. Su mobile il menu principale si trasforma in una comoda sidebar a scorrimento laterale.
  5) Ticker “Breaking News”: Un banner animato (marquee) realizzato in puro CSS, che si mette in pausa quando ci passi sopra con il mouse (per facilitare la lettura).
  6) Tab Interattive: Una sezione “Most Popular” con tab (“Most viewed” e “Deeply read”) completamente navigabile anche da tastiera.
