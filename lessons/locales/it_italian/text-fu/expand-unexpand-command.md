# expand and unexpand

## Lesson Content

Durante la lezione sul comando cut, avevamo un file estratto.txt che conteneva una tabulazione. Normalmente le tabulazioni mostrano una differenza marcata rispetto agli spazi, ma certe volte no. Avere delle tabulazioni in un file potrebbe risultare dunque in una quantità di spazi che in realtà non volevamo avere. Per trasformare tutte le tabulazioni in spazi, usa il comando expand.

<pre>$ expand estratto.txt</pre>

Adesso tutte le tabulazioni del file sono state convertite in spazi.

In modo simile a expand, possiamo anche convertire gli spazi in tabulazioni con il comando unexpand:

<pre>$ unexpand estratto.txt</pre>

## Exercise

Cosa succede quando digiti expand ma senza specificare un file di input?

## Quiz Question

Qual è il comando da usare per convertire le tabulazioni in spazi?

## Quiz Answer

expand
