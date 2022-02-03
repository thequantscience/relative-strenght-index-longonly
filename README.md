# relative-strenght-index-longonly
Esempi di codice semplice Pine in cui si applica il backtesting dell' indicatore RSI. 

L'obbiettivo di questo script è quello di mostrare velocemente all' investitore le performance di trading passate utilizzando l' indicatore RSI. 

# Strategia
La strategia presa in considerazione è long only, vengono analizzate esclusivamente le posizioni long. 

Ingresso: L' algoritmo acquista long il capitale iniziale quando l'RSI è inferiore a 30. 

Uscita: Per l' uscita dal trade utilizzeremo due diverse metodologie, la prima è quella classica basata su Stop Loss e Take Profit e la seconda si basa sul Time Exit. 

All' interno dello script diamo la possibilità all'algoritmo di detrarre il costo di transazione per ogni trade, per rendere lo storico piu veritiero. 
Il costo per transazione fissato è pari al 3% per trade. 

Il capitale iniziale su cui analizziamo questa strategia è fissato a 1000€. 

I parametri di costo per transazione e capitale iniziale possono essere modificati a piacere dall' utente cosi come i parametri tecnici dell' indicatore RSI.

In questo algoritmo ogni perdita e guadagno viene reinvestita con ottica dell' interesse composto.



# relative-strenght-index-longonly
