Plugin grafici
==============
In questa sezione vengono mostrati i plugin grafici sviluppati per la generazione delle figure.
La versione attuale comprende i seguenti plugin:

- Polyline



Polyline
--------
Il plugin Polyline disegna una polilinea in modo dinamico, congiungendo con dei segmenti i punti definiti dall'utente.

Nella slice corrente, il set di punti � un oggetto Map, la cui chiave � rappresentata dalla slice stessa.
Inoltre, � possibile definire sulla stessa slice pi� set di polilinee, memorizzate in un array.
Il set corrente � sempre l'ultimo nella lista.

I metodi 'getCurSet' e 'setCurSet' consentono rispettivamente di conoscere il set corrente di punti, cio� l'ultima polilinea modificata,
e di impostare come corrente il set n della slice attuale.

Il metodo 'addPoint' aggiunge un punto al set attuale; prima dell'inserimento viene verificata la compatibilit� geometrica 
del nuovo set con questo plugin, mediante l'invocazione della funzione 'isValidSet'.

Il disegno vero e proprio della polilinea � effettuato dal metodo 'draw', congiungendo i punti mediante segmenti.



