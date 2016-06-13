# stdin (Standard In)

## Lesson Content

Nella lezione precedente abbiamo imparato che abbiamo diversi stream stdout a nostra disposizione, come i file o il video. Ci sono anche molti altri standard input (stdin) che possiamo usare. Sapiamo che riceviamo uno stdin da dispositivi come la tastiera, ma possiamo usare file, output di altri comandi e lo stesso terminale, vediamone un esempio.

Usiamo il file peanuts.txt della lezione precedente per questo esempio, ricorda che conteneva il testo Hello World.

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

Allo stesso modo in cui avevamo <b>&gt;</b> per la redirezione dello stdout, possiamo usare <b>&lt;</b> per redirigere lo stdin.

Normalmente nel comando cat, è possibile spedire un file perché diventi lo stdin, in questo caso abbiamo deciso di redirigere peanuts.txt nel nostro stdin. In seguito l'output di cat peanuts.txt, che sarebbe Hello world, viene rediretto in un altro file chiamato banana.txt.

## Exercise

Prova questa serie di comandi:
<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Quiz Question

Che operatore di redirezione usi per redirigere lo stdin?

## Quiz Answer

<
