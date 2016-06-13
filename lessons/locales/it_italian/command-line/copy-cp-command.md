# cp (Copy)

## Lesson Content

Iniziamo a fare delle copie dei nostri file. Un po' come fare copia/incolla di file in altri sistemi operativi, la shell ci fornisce un sistema ancora più semplice di operare.

<pre>$ cp filetosto /home/pete/Documenti/robatosta</pre>

dove filetosto è il file che si vuole copiare e /home/pete/Documents/cooldocs è dove lo stiamo copiando.

Puoi copiare più file e directory contemporaneamente utilizzando dei caratteri jolly (o wildcard). Una wildcard è un carattere che può essere sostituito per effettuare una seleziona basata su di un pattern, fornendo una maggiore flessibilità nelle ricerche. Puoi usare le wildcard praticamente con qualunque comando aumentandone la flessibilità di utilizzo.

<ul>
<li>* è la regina delle wildcard, si utilizza per rappresentare tutti i singoli caratteri o qualunque sequenza di qualunque carattere.</li>
<li>? si utilizza per rappresentare un singolo carattere qualunque.</li>
<li>[] si utilizza per rappresentare ogni singolo carattere contenuto all'interno delle parentesi quadrate.</li>
</ul>

<pre>$ cp *.jpg /home/pete/Immagini</pre>

Questo comando effettua la copia di tutti i file che terminano con l'estensione .jpg presenti nella tua directory corrente nella directory Immagini.

Un'opzione utile consiste nell'impiego del flag -r, che copierà ricorsivamente tutti i file e le directory contenuti in una directory.

Prova a lanciare un comando cp su una directory che contiene un qualche file verso la tua directory Documenti. Non ha funzionato, vero? È successo perché devi copiare i file ma anche le directory aggiungendo il comando -r.

<pre>$ cp -r Tonno/ /home/pete/Documenti</pre>

Occorre precisare un'altra cosa, se copi un file verso una directory che ne contiene uno con lo stesso nome, il file verrà riscritto con il contenuto che stai copiando. Non è positivo se il file che hai appena sovrascritto conteneva delle cose che eri interessato a mantenere. Puoi aggiungere il flag -i (interattivo) per ricevere a video una richiesta di conferma prima di sovrascrivere un file.

<pre>$ cp -i filetosto /home/pete/Immagini</pre>

## Exercise

Copia un paio di file, fai attenzione a non sovrascrivere nulla di importante.

## Quiz Question

Che flag devi specificare per copiare una cartella per intero?

## Quiz Answer

-r
