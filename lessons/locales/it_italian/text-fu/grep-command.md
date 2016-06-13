# grep

## Lesson Content

Il comando grep è probabilmente il comando di base di processazione del testo che utilizzerai più di frequente. Grep ti consente di ricercare file per caratteri che compongono un certo pattern. E se volessi sapere se un file esiste in una certa directory, o se volessi controllare se una certa stringa di testo è contenuta in un file? Di sicuro non controlleresti riga per riga, puoi usare grep!

Usiamo il file estratto.txt come esempio:

<pre>$ grep fez estratto.txt</pre>

Dovresti aver visto dal risultato che grep ha trovato fez dentro il file estratto.txt.

Puoi anche ricercare per dei pattern case insensitive (in cui le lettere possono essere indifferentemente maiuscole o minuscole) con il flag -i:

<pre>$ grep -i unpattern unfile</pre>

e per essere ancora più flessibilite con grep lo puoi combinare ai risultati di altri comandi tramite |.

<pre>$ env | grep -i User</pre>

Come vedi grep è parecchio versatile. Puoi usare anche delle espressioni regolari nel tuo pattern:

<pre>$ ls /unacartella | grep '.txt$'</pre>

Che restituirà tutti i file che terminano con .txt nella cartella unacartella.

## Exercise

Magari hai sentito parlare di egrep e fgrep, sono chiamate deprecate di grep che sono state sostituite da un po' di tempo dai flag grep -E e grep -F. Leggi le pagine man del comando grep per saperne di più.

## Quiz Question

Che comando puoi usare per cercare un determinato pattern?

## Quiz Answer

grep
