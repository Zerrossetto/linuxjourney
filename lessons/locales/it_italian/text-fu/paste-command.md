# paste

## Lesson Content

Il comando paste somiglia al comando cat, ossia mette in fila le linee di un file. Creiamo un nuovo file con questi contenuti:

<pre>
$ cat estratto2.txt
Quel
fez
sghembo
copre
davanti
</pre>

Combiniamo assieme tutte le linee in una linea sola:

<pre>$ paste -s estratto2.txt</pre>

Il delimitatore predefinito per paste è Tab ⇥, perciò ora abbiamo una linea sola con le parole separate l'una dall'altra da una tabulazione.

Cambiamo il delimitatore (-d) in qualcosa che renda tutto più leggibile:

<pre>$ paste -d ' ' -s estratto2.txt</pre>

Adesso tutto è disposto su una linea e separato da degli spazi.

## Exercise

Prova a lanciare paste su più di un file contemporaneamente, cosa è successo?

## Quiz Question

Che flag devi usare com paste per unire tutto su una sola riga?

## Quiz Answer

-s
