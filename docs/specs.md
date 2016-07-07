## Home
contiene le seguenti aree a centro-pagina:
- un’area di welcome dove inserire un piccolo sunto su chi siamo, cosa facciamo e a cosa serve il sito;
- un’area con le ultime news (sarà visualizzato in pratica l’ultimo blog-post in ordine cronologico avente come etichetta “news”- vedi “**Blog minimale**” per saperne di più);
- se ti viene in mente qualcos’altro di utile, fai pure; dai anche un’occhiata a questa [community](http://www.pierotofy.it/), ci bazzicavo in passato e devo dire che è molto carina e ben fatta.

## Blog minimale
Implementate solo la visualizzazione dei vari post, mi va bene anche uno sotto l’altro mettendo in alto il più recente (eventualmente potete fare che scorrendo la pagina verso il basso si caricano i post più vecchi in modo dinamico). L’elenco dei post deve offrire, per ogni post, solo una sua sintesi droppata; per leggere il post completo occorre cliccare sul titolo: si aprirà una pagina nuova con l’articolo completo. Il contenuto lo scriverò io manualmente inserendo una riga nella tabella apposita che creerete per MySQL. La tabella dovrà contenere: **data**, **immagine**, **titolo** (max 100 chars), **contenuto** (max 5000 chars), **elencoTag** (max 100 chars). Se riuscite a trovare un parser di markdown alla BB (tipo [b][/b], [i][/i], [url=], [img][/img], [color=][/color], ecc...) scriverò il contenuto io stesso usando questa sintassi, altrimenti posso usare HTML puro (tanto voi dovete solo visualizzare, quindi non c’è rischio di XSS o query injection dall’esterno).  
*Non ci interessano al momento funzioni di ricerca articolo per parole chiave né funzioni di filtraggio sui tag, i quali avranno una semplice funzione di contestualizzazione degli articoli.*

## Chi siamo
Conterrà l’elenco dei membri e il manifesto della crew.

## Guestbook
Gli ospiti potranno lasciare i loro saluti (potrebbe anche essere un wall di Facebook, ma preferirei rimanere svincolato da quel social; ricordate che abbiamo un MySQL a disposizione su OVH, quindi volendo potete implementarne uno semplicissimo voi; i dati da raccogliere saranno: data [automatica], e-mail [opzionale], nome utente [obbligatorio], messaggio [obbligatorio]).

## Progetti
L’elenco dei progetti mantenuti dalla crew. La immagino come una tabella con **nome progetto**, **descrizione** e **link per il download** (che in alcuni casi potrebbe rimandare a GitHub, in altri un link diretto alla risorsa e in altri ancora, come ad esempio nel caso dell’e-zine, rimanderebbe ad un’ulteriore pagina con tutti i numeri da scaricare [un’ulteriore tabella con **numero**, **periodo** {esempio: luglio-agosto 2016} e **link per il download diretto**] Attenzione! Non create però dei veri download diretti alle risorse, fate passare sempre le richieste utente per una chiamata ad uno script PHP che incrementi un contatore per la data risorsa richiesta, in modo da sapere sempre il numero totale di download effettuati su ciascuna risorsa; su OVH abbiamo MySQL, quindi suggerisco di implementare la relativa tabella con MySQL).

## Widget di Twitter
Credo fortemente che Twitter possa essere il ponte di comunicazione broadcast tra l’underground e l’overground, laddove il sito sia invece uno space pubblicamente esposto dove chiunque può venirci a trovare (ok, è sempre overground, ma in questo caso sono gli altri a venire da noi, mentre con Twitter siamo noi che parliamo agli altri).

## IRC Webclient
Ce ne sono tanti in giro, bisogna solo sceglierne uno decente. I parametri di connessione li trovate nel vostro client desktop :-) A differenza del sito in sé, che è uno space dell’overground, IRC è il nostro space dell’underground. Sono entrambi pubblici, ma il web è molto più esposto di IRC, e a mio avviso fornire un webclient per IRC non rende il canale IRC meno underground di quanto non sia senza.
