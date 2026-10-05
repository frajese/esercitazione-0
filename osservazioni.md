# Osservazioni — Esercitazione 0

Gruppo: 47

Componenti (Veronica Dina Frajese, username:Frajese; Gaia Fioravanti, username:Gaia-06);

URL del repository condiviso: https://github.com/frajese/esercitazione-0 

Chi ha usato la tastiera nello step 1 e nello step 2: :D

Compilate insieme le osservazioni e discutete le risposte: entrambi dovete
saper spiegare le prove svolte.

## Step 1 — Hello World: compilazione ed esecuzione

Comando di compilazione: Make

Comando di esecuzione e risultato osservato: ./hello, il programma ha stampato "Hello, computational physics!"

Che cosa ho capito su sorgente ed eseguibile:
Il sorgente è il file di testo che scrivo con Emacs e che contiene le istruzioni in linguaggio C. L’eseguibile viene creato dal compilatore a partire dal sorgente e, quando viene eseguito, permette di verificare il comportamento del programma attraverso i risultati prodotti.

Output richiesto e comportamento del programma prima della modifica:
prima della modifica il codice è commentato, quindi il programma compila ma non stampa nulla.

Esito dopo la modifica e spiegazione della correzione:
Dopo aver completato il TODO in hello.c, e inserito la stampa del messaggio "Hello, computational physics!" seguito da una nuova riga, usando printf, ho ricompilato il programma ed eseguito ./hello, verificando che l'output fosse esattamente quello richiesto, ossia  "Hello, computational physics!".


Risposta alle domande stimolo:  


Dopo aver completato la stampa, Il fatto che il programma compili basta a garantire che faccia ciò che è richiesto?  
No, il fatto che il programma compili non basta a garantire che faccia ciò che è richiesto. Compilare significa che il codice C è sintatticamente corretto e il compilatore riesce a trasformarlo in un eseguibile.
Eseguire e controllare l'output significa verificare che il programma faccia effettivamente ciò che la traccia richiede.

Che differenza c'è tra hello.c e hello? Se modifichi il messaggio nel sorgente e avvii subito l'eseguibile, quale versione stai usando?   
hello.c è il codice sorgente, mentre hello è il programma eseguibile. Se modifico hello.c e avvio subito hello senza ricompilare, uso ancora la vecchia versione.

Che cosa cambia quando ricompili?   
Il compilatore legge il sorgente modificato e crea un nuovo eseguibile, che contiene le ultime modifiche.

Come puoi distinguere ciò che stampa il programma da ciò che mostra il terminale?Che cosa osservi se esegui aggiungendo > output.txt?  
Si può distinguere l'output del programma da ciò che mostra il terminale osservando ciò che viene stampato dal programma rispetto al prompt e agli altri messaggi della shell, con > output.txt, l'output standard del programma viene reindirizzato nel file output.txt e non viene mostrato sul terminale.

## Step 1 — Git

Che differenza c'è fra salvare un file, creare un commit e fare push?   
Salvare modifica il file sul computer; git commit registra le modifiche come una nuova versione nella cronologia locale; git push invia quella versione al repository su GitHub.

Quali modifiche mostra git diff? Quali file occorrono a un compagno per ricompilare il programma sul proprio computer?  
Git diff mostra le modifiche fatte ai file ma non ancora preparate per il commit. Per ricompilare il programma servono i file sorgente, quindi hello.c (e il Makefile fornito dall'esercitazione, se si usa make).

Come puoi verificare che su GitHub ci sia proprio la versione provata?  
Dopo git push, confronto l'ultimo commit mostrato da git log --oneline -5 con quello presente nella cronologia su GitHub e controllo che i file contengano le modifiche che ho apportato.

Perché non è necessario eseguire di nuovo git clone?  
Non è necessario eseguire di nuovo `git clone` perché la copia locale del repository esiste già. `git pull` aggiorna quella copia locale scaricando dal repository remoto i nuovi commit e integrandoli nella cronologia.

Quali file ho incluso nel commit e perché?  
Ho incluso il file sorgente hello.c, perché contiene il codice necessario per ricompilare il programma e osservazioni.md

Come ho verificato che la versione provata sia presente su GitHub?  
Dopo git push ho controllato su GitHub che il file modificato e il relativo commit fossero presenti.

Che cosa ho osservato prima e dopo `git pull`, e perché non serve un nuovo clone:  
Dopo "git pull" il file viene aggiornato sul locale con la modifica eseguita online su Github.

## Step 2 — Eco: prima prova

Argomenti passati: `ciao 12 3.5`
Comando: `./eco ciao 12 3.5`
Risultato: `ciao 12 3.500000`

Che cosa posso concludere: gli argomenti vengono passati al programma come testo e quelli numerici vengono convertiti nel tipo di dato richiesto prima di essere stampati.


Domande stimolo:

Gli elementi di argv sono già numeri? Che differenza ti aspetti passando 0012 come primo oppure come secondo argomento?   
No, gli elementi di `argv` sono stringhe e hanno bisogno di essere convertiti in interi e decimali. Se passiamo `0012` come primo argomento stampa il numero così come è perché viene salvato tutto in una stringa, passandolo come secondo argomento invece viene stampato solo il numero `12` perché viene convertito in un intero.

Come puoi passare un testo che contiene spazi mantenendolo come un solo argomento?
Scrivendo tutta la parte di testo tra virgolette.

Se scrivi 1.25e1 come terzo argomento, quale valore ti aspetti in uscita? La rappresentazione scritta sulla riga di comando deve rimanere uguale?  
Viene convertito nel valore `12.5`, quindi la scrittura cambia perché il valore viene convertito in un `double` e poi stampato con sei cifre dopo il punto decimale.

Se un argomento manca o non rappresenta il tipo richiesto (ad esempio una stringa invece di un numero), che cosa ti aspetti dal programma?  
Se manca un argomento, il programma stampa il messaggio di errore previsto dal codice. Se si utilizza un numero al posto del testo, viene stampato così come è. Se si inserisce del testo al posto di un numero, il programma segnala un errore. Se si mette un decimale al posto di un intero, la parte decimale viene troncata, se si mette un intero al posto del decimale, viene letto come valore reale e stampato con sei zeri dopo il punto.

Come distingui il risultato da un messaggio di errore?
Si può distinguere osservando dove viene stampato: il risultato viene inviato a `stdout`, mentre il messaggio di errore viene inviato a `stderr`. Con `>` viene reindirizzato solo `stdout`, quindi il risultato finisce nel file mentre il messaggio di errore rimane nel terminale.


Nello step 2, oltre alle prove proposte, individua argc e argv in eco.c: perché il programma richiede argc == 4 pur ricevendo tre argomenti? Che cosa contiene argv[0]?    
Il programma richiede `argc == 4` perché `argc` conta anche il nome del programma, oltre ai tre argomenti passati. `argv[0]` contiene quindi il nome o il percorso con cui è stato eseguito il programma, mentre `argv[1]`, `argv[2]` e `argv[3]` contengono i tre argomenti forniti dall'utente.


## Step 2 — Eco: seconda prova
Argomenti: `ciao 12 3.4` — comando: `./eco ciao 12 3.4` — risultato: `ciao 12 3.400000`.
Argomenti: `ciao dodici 3.4` — comando: `./eco ciao dodici 3.4` — risultato: `ciao 0 3.400000`.
Che cosa ho capito su testo, conversioni e stampa:
Gli argomenti di `argv` sono stringhe. I valori numerici devono essere convertiti nel tipo corretto prima di essere utilizzati e stampati. La stampa può quindi avere una rappresentazione diversa da quella inserita inizialmente.

1. Che cosa contiene eco.txt nei due casi?  
Nel primo caso, eseguendo ./eco ciao 12 3.5 > eco.txt, il file contiene ciao 12 3.500000, perché gli argomenti numerici vengono convertiti correttamente.
Nel secondo caso, eseguendo ./eco ciao dodici 3.5 > eco.txt, il file contiene ciao 0 3.500000, perché la funzione atoi() cerca di convertire la stringa "dodici" in un numero intero, ma non trovando cifre iniziali restituisce 0. Il programma continua quindi l'esecuzione e stampa comunque il risultato. Inoltre, il simbolo > sostituisce il contenuto precedente del file con il nuovo output.

2. Quali codici di uscita osservi? Come potresti usarli in un controllo automatico?   
Nel primo caso il codice di uscita è 0, che indica il completamento regolare. Nel secondo caso è 0 anche se l'argomento è errato, perché il programma usa atoi(), che converte il testo non numerico in 0 senza segnalare un errore. Per riconoscere automaticamente gli errori, bisognerebbe usare una funzione di conversione che controlli la validità dell'argomento e restituisca un codice diverso da 0 in caso di errore.

## Step 2 — Risultato ed errori

Eseguire il programma cambiando il terzo argomento:
Non è necessario ricompilare se si cambia solo il valore del parametro passato al programma, perché il codice non viene modificato. Per cambiare la formula usata dal programma, invece, bisogna modificare il codice sorgente e quindi ricompilare.

Previsioni per l'esecuzione con argomenti validi e per quella con `dodici`:  
Con ./eco ciao 12 3.5 il programma converte 12 in un int e 3.5 in un double, quindi stampa ciao 12 3.500000.
Con ./eco ciao dodici 3.5, dodici non rappresenta un intero valido. La funzione leggi_intero riconosce l'errore e termina il programma.


Contenuto di `eco.txt`, messaggi nel terminale e codici di uscita osservati:
Nel primo caso eco.txt contiene: ciao 12 3.500000
Nel terminale non compare il risultato del programma perché è stato rediretto nel file. Il codice di uscita è 0. Nel secondo caso eco.txt rimane vuoto, perché il programma termina prima di eseguire la printf. Nel terminale compare: "Il secondo argomento deve essere un intero in base 10."
Il codice di uscita è 2.

Come un controllo automatico può riconoscere un errore:
Un controllo automatico può controllare il codice di uscita del programma. 0 indica che l'esecuzione è terminata regolarmente, mentre un valore diverso da 0, come 2, indica che si è verificato un errore. Il valore può essere controllato, ad esempio, con echo $? oppure utilizzato in uno script.

MANCANTI
## Step 2 — Parametri e calcolo fisico

Quando serve ricompilare e quando basta cambiare gli argomenti:

## Step 2 — Git

Come riconosco nella cronologia i commit dei due step:
Per controllare la cronologia su git si utilizza il comando git log --online -5, per controllare la cronologia su Github bisogna verificare l'elenco degli ultimi commit. 

Come ho verificato che la versione finale sia presente su GitHub: Verificando che l'ultimo commit su git e github sia lo stesso. 
