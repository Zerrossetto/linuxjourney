# cut

## Lesson Content

Impareremo alcuni comandi utili per processare il testo. Prima di iniziare, creiamo il file che useremo poi per lavorare. Copia e incolla il comando che segue, dopo che hai finito di incollare aggiungi una tabulazione con il tasto Tab ⇥ tra copre e davanti (tieni premuto ctrl-v e Tab ⇥).

<pre>$ echo 'Quel fez sghembo; copre davanti' > estratto.txt</pre>

Come primo comando impareremo il comando cut. Cut serve a estrarre porzioni di testo da un file.

Per estrarre i contenuti da una lista di caratteri:

<pre>$ cut -c 6 estratto.txt</pre>

Così restituisce il sesto carattere per ogni riga del file. Nel nostro caso è una “f”, nota inoltre che anche gli spazi contano come carattere.

Per estrarre i contenuti da un campo, dobbiamo introdurre una piccola modifica:

<pre>$ cut -f 2 estratto.txt</pre>

Il -f o flag field (campo) taglia il testo di una linea basandosi sui campi, che per default utilizzano la tabulazione ⇥ come delimitatore, perciò ogni cosa separata dal Tab ⇥ è considerata un campo. Dovresti quindi aver visto a video la parola “davanti”.

Puoi combinare il -f con il flag delimitatore per estrarre il contesto usando un delimitatore diverso:

<pre>$ cut -f 1 -d ";" estratto.txt</pre>

Così hai modificato il delimitatore Tab ⇥ facendolo diventare il carattere “;” e dato che stiamo tagliando sul primo campo, il risultato dovrebbe essere “Quel fez sghembo”.

## Exercise

Cosa fa secondo te il comando che segue? Perché?

<pre>$ cut -c 5-10 estratto.txt
$ cut -c 5- estratto.txt
$ cut -c -5 estratto.txt
</pre>

## Quiz Question

Che comando useresti per ottenere il primo carattere di ogni linea in un file?

## Quiz Answer

cut -c 1
