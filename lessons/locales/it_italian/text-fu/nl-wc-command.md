# wc and nl

## Lesson Content

Il comando wc (work count, conta parole) mostra il conteggio totale di parole in un file.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Mostra rispettivamente il numero di linee, il numero di parole e il numero di byte.

Per vedere soltanto un certo campo, puoi usare i flag corrispondenti -l, -w o -c.

<pre>$ wc -l /etc/passwd
96</pre>

Un altro comando che puoi usare per contare il numero di iline in un file è il comando nl (numero di linee).

<pre>
file1.txt
pasta
col
tonno
</pre>

<pre>$ nl file1.txt
1. pasta
2. col
3. tonno
</pre>

## Exercise

Come puoi estrarre il conteggio totale delle linee usando nl ma senza cercare lungo tutto l'output del comando?
Suggerimento: Usa qualcun altro dei comandi che hai imparato durante questo corso.

## Quiz Question

Che comando useresti se volessi sapere il numero delle parole in un file e nient'altro?

## Quiz Answer

wc -w
