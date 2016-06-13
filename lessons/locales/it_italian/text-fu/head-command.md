# head

## Lesson Content

Mettiamo di avere un file bello lungo, e di fatto ne abbiamo parecchi tra cui scegliere. Fai una prova, lancia il comando cat /var/log/syslog. Vedrai pagine e pagine di testo. Non sarebbe meglio vedere soltanto il primo paio di linee del documento? Si può fare con il comando head, head per default mostrerà le prime 10 righe di un certo file.

<pre>$ head /var/log/syslog</pre>

Puoi modificare il numero di righe in quello che preferisci, poniamo per esempio che voglia visualizzare le prime 15.

<pre>$ head -n 15 /var/log/syslog</pre>

Il flag -n sta per numero di righe.

## Exercise

Cosa fa il comando qui sotto e perché?

<pre>$ head -c 15 /var/log/syslog</pre>

## Quiz Question

Che flag si usa per cambiare il numero di righe che vengono mostrate nel comando head?

## Quiz Answer

-n
