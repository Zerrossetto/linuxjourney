# regex (Regular Expressions)

## Lesson Content

Le espressioni regolari sono un potente strumento per effettuare selezioni basate su pattern. Per farlo utilizzano una notazione speciale simile a quella che abbiamo incontrato, come la wildcard *.

Approfondiremo alcune delle espressioni regolari più comuni, che sono in pratica trasversali a tutti i linguaggi di programmazione.

Useremo questa frase come stringa di test:
<pre>
sopra il pozzo c'è un cane pazzo
date al pazzo cane un pezzo di pane
</pre>

<b>1. Facendo iniziare l'espressione con ^</b>

<pre>
<b>^</b>date
la linea "date al pazzo cane un pezzo di pane" viene selezionata
</pre>

<b>2. Facendo finire l'espressione con $</b>

<pre>
pane<b>$</b>
la linea "date al pazzo cane un pezzo di pane" viene selezionata
</pre>

<b>3. Selezionare un carattere qualunque con .</b>

<pre>
d<b>.</b>
"di" viene selezionato
</pre>

<b>4. Notazione con parentesi [] e ()</b>

Questo è un po' più difficile, le parentesi ti consentono di selezionare per i caratteri inclusi tra le parentesi.

<pre>
p<b>[aeo]</b>zzo
seleziona: pozzo, pazzo, pezzo
</pre>

Il segno di accento circonflesso ^ visto poco fa, quando usato tra le parentesi, indica che si cerca qualunque cosa eccetto i caratteri inclusi all'interno.

<pre>
p<b>[^e]</b>zzo
seleziona: pazzo e pozzo ma non pezzo
</pre>

Le parentesi accettano anche intervalli per aumentare il numero di caratteri che potresti voler usare.

<pre>
p<b>[a-c]</b>zzo
potrebbe selezionare le parole pazzo, pbzzo e pczzo
</pre>

Attento però, le parentesi sono case sensitive:

<pre>
p<b>[A-C]</b>zzo
selezionerà pAzzo, pBzzo e pCzzo ma non pazzo, pbzzo e pczzo
</pre>

E con questo abbiamo affrontato alcune delle espressioni regolari base.

## Exercise

Prova a combinare delle espressioni regolari con il comando grep e cerca dentro a dei file.

<pre>
grep [insersci qui l'espressione regolare] [file]

## Quiz Question

Quale espressione regolare useresti per selezionare un singolo carattere qualunque?

## Quiz Answer

.
