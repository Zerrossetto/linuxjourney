# stdout (Standard Out)

## Lesson Content

Fino ad adesso, abbiamo guadagnato familiarità con tanti comandi e il loro risultati, questo ci conduce direttamente al prossimo argomento, gli stream di input/output. Lanciamo il comando che segue e parliamo di quello che fa.

<pre>$ echo Hello World > peanuts.txt</pre>

Cos'è successo? Controlla nella cartella in cui ti trovi ed ecco che dovresti trovare un file chiamato peanuts.txt, guarda dentro il file e dovresti trovarci la scritta Hello World. Sono successe un sacco di cose in un solo comando, cominciamo dall'inizio.

Per prima cosa osserviamo la parte iniziale:

<pre>$ echo Hello World</pre>

Sappiamo che questo comando scrive a video Hello World, ma come fa? Il programma utilizza gli stream I/O per ricevere un input e ritornare un risultato (output). Di default il comando echo prende l'input (standard input o stdin) dalla tastiera e ritorna l'output (standard output o stdout) a video. Ecco perchè quando digiti echo Hello World nella tua shell, ricevi poi Hello World a video. La redirezione I/O, dalla sua, consente di modificare il comportamento di default donandoci una flessibilità maggiore.

Andiamo sulla prossima parte del comando:

<pre> > </pre>

Il simbolo > è un operatore di redirezione che ci consente di modificare la destinazione dello standard output. Ci consente di spedire il risultato di echo Hello World in un file invece che a video. Se il file non esiste già verrà creato. Però se il file esiste già verrà sovrascritto (puoi sempre aggiungere un flag alla tua shell per prevenire il comportamento, ma può dipendere dalla shell che stai usando).

In pratica è così che la redirezione dello stdout funziona!

Poniamo che io non voglia sovrascrivere il mio file peanuts.txt, per fortuna c'è un operatore di redirezione anche per questo, >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Questo comando appenderà Hello World alla fine del file peanuts.txt, se il file non esiste verrà creato esattamente come avveniva con l'operatore di redirezione >!


## Exercise

Prova questa serie di comandi:

<pre>
$ ls -l /var/log > output.txt
$ echo Hello World > rm
$ > unfile.txt
</pre>

## Quiz Question

Che redirettore usi se vuoi appendere il tuo risultato a un file?

## Quiz Answer

>>
