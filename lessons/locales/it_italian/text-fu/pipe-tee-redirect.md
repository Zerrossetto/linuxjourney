# pipe and tee

## Lesson Content

Ora ci addentreremo nell'idraulica, non proprio ma quasi. Proviamo un comando:

<pre>$ ls -la /etc</pre>

Dovresti vedere un lungo di entità, abbastanza difficile da leggere ammetto. Invece di redirigere questo output in un file, non sarebbe carino se potessimo consultare il risultato in un altro comando come less? Come no, possiamo!

<pre>$ ls -la /etc | less </pre>

L'operatore pipe |, rappresentato dalla barra verticale, ci consente di raccogliere lo stout di un comando per farlo diventare lo stdin di un altro. In questo caso, abbiamo preso lo stdout di ls -la /etc per <i>intubarlo</i> nel comando less. L'operatore pipe è estremamente utile e lo continueremo a utilizzare per l'eternità.

E se volessi scrivere l'output del mio comando su due stream diversi in contemporanea? Possiamo farlo con il comando tee:

<pre>$ ls | tee peanuts.txt</pre>

Dovresti vedere a video il risultato di ls, e se apri il file peanuts.txt dovresti trovare le stesse informazioni!

## Exercise

Prova la sequenza di comandi che segue:
<pre>$ ls | tee peanuts.txt banana.txt</pre>

## Quiz Question

Che simbolo rappresenta l'operatore pipe?

## Quiz Answer

|
