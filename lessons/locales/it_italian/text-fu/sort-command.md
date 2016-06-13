# sort

## Lesson Content

Io comando sort è molto utile per ordinare le righe.

<pre>
file1.txt
cane
mucca
gatto
elefante
passero

$ sort file1.txt
cane
elefante
gatto
mucca
passero
</pre>

Puoi anche ordinare al contrario:

<pre>$ sort -r file1.txt
passero
mucca
gatto
elefante
cane
</pre>

Oppure ordinare tramite il valore numerico di ogni carattere:

<pre>$ sort -n file1.txt
cane
elefante
gatto
mucca
passero
</pre>

## Exercise

La vera forza di sort nasce dalla possibilità di poterlo combinare con altri comandi, prova il comando qui sotto, vedi cosa succede?

<pre>$ ls /etc | sort -rn</pre>

## Quiz Question

Che flag devi usare per lanciare un ordinamento inverso?

## Quiz Answer

-r
