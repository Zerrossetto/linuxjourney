# env (Environment)

## Lesson Content

Lancia il comando che segue:

<pre>$ echo $HOME</pre>

Dovresti vedere il percorso fino alla tua home directory, la mia è /home/pete.

E questo comando?

<pre>$ echo $USER </pre>

Dovrebbe farti vedere il tuo username!

Da dove salta fuori questa informazione? Proviene dalle variabili di ambiente. le puoi vedere tutte digitando

<pre>$ env </pre>

Che restituisce un sacco di informazioni relative alla variabili do ambiente che attualmente sono valorizzate. Le variabili contengono informazioni utili che la shell e altri processi possono usare.

Ecco un breve esempio:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>

Una variabile particolarmente importante è la variabile PATH. Puoi accedere alle variabili aggiungendo il simbolo $ all'inizio del nome della variabile, così:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

Il comando ha ritornato una lista di percorsi separati dal simbolo due punti “:” che il tuo sistema ricerca quando si cerca di lanciare un comando. Mettiamo che hai scaricato manualmente da internet e poi installato un programma, e poi l'hai messo in una cartella non standard ma vuoi eseguire quel comando. Digiti $ bellofigogu e il prompt ti dice che non ha trovato il programma. È strano, dato hai davanti la cartella che contiene il binario e sai che esiste. Succede che la variabile $PATH non contiene il percorso per quella cartella e perciò ritorna un errore.

Diciamo che hai una miriade di file binari che vorresti far girare da quella directory, puoi modificare la variabile PATH per includere anche la tua cartella tra i percorsi già presenti nel valore di PATH.

## Exercise

Cosa ritorna il comando che segue? Perché?
<pre>$ echo $HOME</pre>

## Quiz Question

Come fai a vedere tutte le tue variabili di ambiente?

## Quiz Answer

env
