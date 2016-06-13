# uniq (Unique)

## Lesson Content

Il comando uniq (unique, unico) è un altro comando utile per parsare il testo.

Supponiamo di avere un file con un mucchio di valori duplicati:

<pre>
letture.txt
libro
libro
paper
paper
articolo
articolo
rivista</pre>

E supponiamo di voler rimuovere i duplicati, lo puoi fare usando il comando uniq:

<pre>$ uniq letture.txt
libro
paper
articolo
rivista</pre>

Otteniamo anche il conteggio di quante occorrenze abbiamo della stessa riga:

<pre>$ uniq -c letture.txt
2 libro
2 paper
2 articolo
1 rivista</pre>

Prendiamo soltanto i valori unici:

<pre>$ uniq -u letture.txt
rivista</pre>

Teniamo soltanto i valori duplicati:

<pre>$ uniq -d letture.txt
libro
paper
articolo</pre>

## Exercise

Che risultato pensi di ottenere usando uniq -uc?

## Quiz Question

Che comando useresti per rimuovere i duplicati in un file?

## Quiz Answer

uniq
