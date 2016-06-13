# stderr (Standard Error)

## Lesson Content

Proviamo qualcosa di un po' diverso ora, proviamo a elencare i contenuti di una directory che non esiste sul tuo sistema e redirigere di nuovo il risultato nel file peanuts.txt.

<pre>$ ls /directory/finta > peanuts.txt </pre>

Dovresti vedere a video:

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Ti starai probabilmente chiedendo: il messaggio non dovrebbe essere finito nel file? In realtà dietro le quinte esiste uno stream I/O diverso chiamato standard error (stderr). Di default, anche l'stderr invia i propri risultati direttamente a video, ed è uno stream completamente diverso dallo stdout. Dovrai quindi redirigere il suo output in una maniera diversa.

Malauguratamente il simbolo di redirezione non è leggibile quanto <b>&lt;</b> o <b>&gt;</b> ma ci va vicino. Dobbiamo usare un descrittore di file. Un descrittore di file è un numero non negativo che viene usato per accedere a un file oppure a uno stream. Spiegheremo il concetto più nel dettaglio un'altra volta, per adesso sappi che i descrittori per stdin, stdout e stderr sono rispettivamente i numeri 0, 1 e 2.

Se quindi adesso volessimo redirigere il nostro stderr in un file possiamo fare così:

<pre>$ ls /directory/finta 2> peanuts.txt</pre>

Dovresti aver trovato i messaggi di errore nel file peanuts.txt.

Se adesso volessi mettere sia stderr che stdout nel file peanuts.txt? È possibile farlo usando i descrittori di file.

<pre>$ ls /directory/finta > peanuts.txt 2>&1</pre>

Abbiamo spedito i risultati di ls /directory/finta nel file peanuts.txt e poi rediretto lo stderr nello stdout tramite 2>&1. L'ordine delle operazioni conta, 2>&1 invia lo stderr a qualsiasi bersaglio sia puntato da stdout. In questo caso stdout punta a un file, quindi anche 2>&1 spedirà lo stderr verso un file. Se quindi apri il file peanuts.txt troverai sia stderr che stdout. Nel nostro caso, il comando sopra scrive soltanto tramite lo stderr.

C'è anche un metodo più corto di redirigere sia stdout che stderr sullo stesso file:

<pre>$ ls /directory/finta &> peanuts.txt</pre>

Invece se non volessi leggermi tutta quella sbobba e mi volessi sbarazzare completamente dei messaggi di errore? Posso farlo redirigendo il risultato su un file speciale chiamato /dev/null che scarterà ogni input.

<pre>$ ls /directory/finta 2> /dev/null</pre>

## Exercise

Qual è l'effetto di questo comando?

<pre>$ ls /directory/finta >> /dev/null 2>&1</pre>

## Quiz Question

Qual è l'operatore di redirezione per l'stderr?

## Quiz Answer

2>
