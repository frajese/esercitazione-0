# Osservazioni — Esercitazione 0

Gruppo:47

Componenti (Veronica Dina Frajese, username:Frajese; Gaia Fioravanti, username:Gaia-06);

URL del repository condiviso: https://github.com/frajese/esercitazione-0 

Chi ha usato la tastiera nello step 1 e nello step 2: :D

Compilate insieme le osservazioni e discutete le risposte: entrambi dovete
saper spiegare le prove svolte.

## Step 1 — Hello World: compilazione ed esecuzione

Comando di compilazione: Make

Comando di esecuzione e risultato osservato: ./hello, il programma ha stampato "Hello, computational physics!"

Che cosa ho capito su sorgente ed eseguibile:
sorgente è il file di testo che io scrivo su emacs, l'eseguibile viene creato con il compilatore e se eseguito permette di controllare il funzionamento del codice.

Output richiesto e comportamento del programma prima della modifica:
prima della modifica gran parte del codice rimane commentato, quindi il codice compila ma non stampa nulla.

Esito dopo la modifica e spiegazione della correzione:
Dopo aver completato il TODO in hello.c, ho inserito la stampa del messaggio Hello, computational physics! seguito da una nuova riga, usando printf. Ho poi ricompilato il programma ed eseguito ./hello, verificando che l'output fosse esattamente quello richiesto, ossia  "Hello, computational physics!".


Risposta alle domande stimolo:
Dopo aver completato la stampa, Il fatto che il programma compili basta a garantire che faccia ciò che è richiesto?
No, il fatto che il programma compili non basta a garantire che faccia ciò che è richiesto. Compilare significa che il codice C è sintatticamente corretto e il compilatore riesce a trasformarlo in un eseguibile.
Eseguire e controllare l'output significa verificare che il programma faccia effettivamente ciò che la traccia richiede.

La differenza tra hello.c e hello: hello.c è il codice sorgente, mentre hello è il programma eseguibile. Se modifico hello.c e avvio subito hello senza ricompilare, uso ancora la vecchia versione.

Che cosa cambia quando ricompili? Il compilatore legge il sorgente modificato e crea un nuovo eseguibile, che contiene le ultime modifiche.

Come puoi distinguere ciò che stampa il programma da ciò che mostra il terminale? Ciò che stampa il programma è il suo output; il terminale può mostrare anche comandi ed eventuali messaggi di errore. Con > output.txt, l'output normale del programma viene salvato nel file output.txt invece di essere visualizzato sul terminale

Differenza fra salvare, commit e push: salvare modifica il file sul computer; git commit registra le modifiche come una nuova versione nella cronologia locale; git push invia quella versione al repository su GitHub.

Cosa mostra git diff e quali file servono: git diff mostra le modifiche fatte ai file ma non ancora preparate per il commit. Per ricompilare il programma servono i file sorgente, quindi hello.c (e il Makefile fornito dall'esercitazione, se si usa make).

Come verificare la versione su GitHub: dopo git push, confronto l'ultimo commit mostrato da git log --oneline -5 con quello presente nella cronologia su GitHub e controllo che i file contengano le modifiche che ho provato.

## Step 1 — Git

Quali file ho incluso nel commit e perché: Ho incluso il file sorgente hello.c, perché contiene il codice necessario per ricompilare il programma e osservazioni.md

Come ho verificato che la versione provata sia presente su GitHub: Dopo git push ho controllato su GitHub che il file modificato e il relativo commit fossero presenti.

Che cosa ho osservato prima e dopo `git pull`, e perché non serve un nuovo clone:
dopo "git pull" osservazioni.md viene aggiornato sul locale con la modifica eseguita online su Github;
non serve un nuovo clone perché utilizzo il comando pull per aggiornare il locale, non ho bisogno di clonare di nuovo tutti i file che avevo già scaricato.

## Step 2 — Eco: prima prova

Argomenti passati, comando e risultato:

Che cosa posso concludere:

## Step 2 — Eco: seconda prova

Argomenti passati, comando e risultato:

Che cosa ho capito su testo, conversioni e stampa:

## Step 2 — Risultato ed errori

Previsioni per l'esecuzione con argomenti validi e per quella con `dodici`:

Contenuto di `eco.txt`, messaggi nel terminale e codici di uscita osservati:

Come un controllo automatico può riconoscere un errore:

## Step 2 — Parametri e calcolo fisico

Quando serve ricompilare e quando basta cambiare gli argomenti:

## Step 2 — Git

Come riconosco nella cronologia i commit dei due step:

Come ho verificato che la versione finale sia presente su GitHub:
