# join and split

## Lesson Content

Il comando join ti permette di unire più file assieme sfruttando un campo comune:

Se per esempio ho due file che voglio unire:
<pre>$ cat file1.txt
1 Mario
2 Francesca
3 Maria

$ cat file2.txt
1 Rossi
2 Rossi
3 Esposito

$ join file1.txt file2.txt
1 Mario Rossi
2 Francesca Rossi
3 Maria Esposito
</pre>

Hai visto come i miei file si sono uniti? L'unione viene fatta di default sfruttando il primo campo e il campo di unione dev'essere identico per entrambi i file, se non sono ordinati puoi ordinarli tu, nel mio caso quindi i file sono stati uniti per 1, 2 e 3.

Come uniresti i due file qui sotto?

<pre>$ cat file1.txt
Mario 1
Francesca 2
Maria 3

$ cat file2.txt
1 Rossi
2 Rossi
3 Esposito
</pre>

Per unire questi file devi specificare su quali campi vuoi eseguire la join. Nel caso in questione dobbiamo unire il secondo campo su file1.txt con il primo campo su file2.txt, quindi il risultato sarà una cosa del genere:

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 Mario Rossi
2 Francesca Rossi
3 Maria Esposito
</pre>

-1 fa riferimento a file1.txt mentre -2 a file2.txt. Semplice. Puoi anche dividere un file in più file diversi file con il comando split:

<pre>$ split unfile</pre>

Così puoi dividere il file in più file diversi, per default verranno divisi fino a raggiungere un limite di 1000 righe. I file vengono chiamati x** per default.

## Exercise

Unisci due file con numeri di riga diversi in ogni file, che risultato ti aspetti di trovare?

## Quiz Question

Che comando devi lanciare per unire dei file chiamati gatto cane mucca?

## Quiz Answer

join gatto cane mucca
