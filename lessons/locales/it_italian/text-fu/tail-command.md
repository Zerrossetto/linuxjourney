# tail

## Lesson Content

Simile al comando head, il comando tail ti permette di vedere come default le ultime 10 linee di un file.

<pre>$ tail /var/log/syslog</pre>

Come per head puoi modificare il numero di linee che intendi vedere.

<pre>$ tail -n 10 /var/log/syslog</pre>

Un'altra fanvolosa opzione che puoi usare è il flag -f (follow, segui), con cui puoi seguire le modifiche al file mentre accadono. Prova a vedere cosa succede.

<pre>$ tail -f /var/log/syslog</pre>

Il file di syslog cambierà in continuazione mentre interagisci col tuo sistema e usando tail -f puoi vedere tutto ciò che viene aggiunto al file.

## Exercise

Leggi le pagine man del comando tail e leggi qualcuno degli altri comandi di cui non abbiamo parlato.

<pre>$ man tail</pre>

## Quiz Question

Qual è il flag usato per seguire le modifiche in coda a un file?

## Quiz Answer

-f
