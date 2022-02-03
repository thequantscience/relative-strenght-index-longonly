L'obbiettivo di questo script è quello di mostrare velocemente all' investitore le performance di trading passate utilizzando l' indicatore RSI. 

Gli script prendono in analisi il pair Bitcoin/USDTether con timeframe 4H (KuCoin Exchange).

Inizialmente per comprendere lo script ti consigliamo quindi di impostare questo pair assieme al suo timeframe di riferimento. 

I file sono due: 

1) Time Exit 
2) Stop Loss Take Profit 

Differiscono per la funzione di uscita dal trade. L' uscita 1) si basa su un periodo temporale, il 2) su un uscita in base al valore corrente del capitale investito. 

IMPORTANTE: Il file 2) contenente stop loss e take profit calcola una media sul capitale per decretare i livelli di stop e profit. Questo può portare a modeste variazioni in temrmini percentuali. Queste variazioni dipendono da due fattori:

A) Il primo è che l' output tiene in considerazione anche dei costi di transazione.
B) Il secondo dato il calcolo di SL e TP sulla media, se il capitale iniziale cresce o diminuisce può comportare transitorie variazioni sui parametri di SL e TP futuri.

Per comprendere il funzionamento circa i parametri di SL e TP puoi approfondire la funzione --> strategy.position_avg_price

# Strategia
La strategia presa in considerazione è long only, vengono analizzate esclusivamente le posizioni long. 

Ingresso: L' algoritmo acquista long il capitale iniziale quando l'RSI è inferiore a 30. 

Uscita: Per l' uscita dal trade utilizzeremo due diverse metodologie, la prima è quella classica basata su Stop Loss e Take Profit e la seconda si basa sul Time Exit. 

All' interno dello script diamo la possibilità all'algoritmo di detrarre il costo di transazione per ogni trade, per rendere lo storico piu veritiero. 
Il costo per transazione fissato è pari al 3% per trade. 

Il capitale iniziale su cui analizziamo questa strategia è fissato a 1000€. 

I parametri di costo per transazione e capitale iniziale possono essere modificati a piacere dall' utente cosi come i parametri tecnici dell' indicatore RSI.

In questo algoritmo ogni perdita e guadagno viene reinvestita con ottica dell' interesse composto.

# Setting 

1) Copia il codice dal file GitHub. 
2) Incolla il codice sul tuo editor di Trading View e salva.
3) Scegli un mercato e un time frame. 
4) Clicca su aggiungi al grafico. 
5) Analizza. 

Potrai modificare i parametri dell' algoritmo in base al mercato e time frame di riferimento senza alcun vincolo. 

# ATTENZIONE: Disclaimer 

La performance passata non è garanzia di risultati futuri e il valore degli investimenti può aumentare o diminuire. Nessuna strategia di investimento è al riparo dal rischio e i mercati influiscono sui risultati dell'investimento. I mercati e le loro condizioni possono cambiare bruscamente. Strategie o prodotti possono registrare perdite o guadagni. Gli investitori che hanno ulteriori domande dovrebbero richiedere una consulenza indipendente in base alle loro esigenze, situazione e livello di tolleranza al rischio. Questo è un semplice esempio di backtesting, non un consiglio finanziario! Eventuali danni derivanti da un uso diverso da quello accademico non sono imputabili in alcun modo al titolare dell'account.  L'utilizzo dei dati e delle informazioni come supporto di scelte di operazioni d'investimento personale è a completo rischio dell'Utente. Prima di concludere una qualsiasi operazione bancaria/finanziaria sulla base delle informazioni ottenute - direttamente o indirettamente - , è opportuno che l'Utente si rivolga alla propria banca o ad altro intermediario finanziario autorizzato, al fine di verificare la veridicità e la correttezza di tali informazioni, nonché l'opportunità dell'operazione in relazione alle proprie esigenze personali e alla propria situazione economica, finanziaria e reddituale.
