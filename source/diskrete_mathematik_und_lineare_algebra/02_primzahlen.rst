Primzahlen
================

Definition: Primzahl
**********************

:math:`p\in\mathbb{N} heißt Primzahl, wenn `p` genau 2 Teiler besitzt. Jede natürliche Zahl `n` hat mindestens die
trivialen Teiler 1 und `n`.

*Hinweis:* Die kleinste Zahl, die die Definition erfüllt, ist die 2.

Bsp.
^^^^^

2, 3, 5, 7, 11, 13, ...

Primzahlentest:
*****************

**Naive Idee:** Teste für alle Zahlen :math:`k=2,3,...,n-1` ob sie Teiler sind.

**Verbesserung:** Der kleinst mögliche Teiler von n ist 2 (der n als Primzahl ausschließt), daher kann der größte
Teiler maximal :math:`\frac{n}{2}` sein. **Beobachtung:** Wenn
