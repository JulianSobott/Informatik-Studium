.. role:: def
    :class: underline



Primzahlen
================

.. contents::
    :local:

Definition: Primzahl
**********************

:math:`p\in\mathbb{N}` heißt Primzahl, wenn `p` genau 2 Teiler besitzt. Jede natürliche Zahl `n` hat mindestens die
trivialen Teiler 1 und `n`.

**Hinweis:** Die kleinste Zahl, die die Definition erfüllt, ist die 2.

Beispiel: Primzahlen
^^^^^^^^^^^^^^^^^^^^^

2, 3, 5, 7, 11, 13, ...

Primzahlentest:
*****************

**Naive Idee:** Teste für alle Zahlen :math:`k=2,3,...,n-1` ob sie Teiler sind.

**Verbesserung:** Der kleinst mögliche Teiler von n ist 2 (der n als Primzahl ausschließt), daher kann der größte
Teiler maximal :math:`\frac{n}{2}` sein.

**Beobachtung:** Wenn :math:`\frac{n}{2}\mid n`, dann gilt auch :math:`2\mid n`, denn :math:`n=2*\frac{n}{2}`.

**Allgemein gilt:** Für :math:`k\in \mathbb{N}` gilt, wenn :math:`\frac{n}{k}\mid n`, dann gilt auch :math:`k\mid n`.

Sei :math:`k\ne 1` der kleinste Teiler von `n`, dann findet der oben beschriebene Algorithmus `k` vor
:math:`\frac{n}{k}`, da gilt :math:`k\le \frac{n}{k}`. Abschätzung für den kleinsten Teiler `k` : :math:`k \le
\frac{n}{k} \Leftrightarrow k^2\le n \Leftrightarrow k \le \sqrt{n}`. D.h. existiert ein Teiler :math:`k \notin \{1,
n\}`, dann ist mindestens ein Teiler von `n` kleiner als :math:`\sqrt{n}`. Um zu zeigen, dass `n` eine Primzahl ist,
genügt es also zu zeigen, dass gilt: :math:`\forall k \le \sqrt{n}: k \nmid n`

**Beobachtung:**
    - Wenn :math:`2 \nmid`, dann gilt :math:`\forall a < \sqrt{n}` ebenfalls :math:`(2a)\nmid n`
    - Wenn :math:`3 \nmid`, dann gilt :math:`\forall a < \sqrt{n}` ebenfalls :math:`(3a)\nmid n`
    - Allgemein: Für :math:`k<\sqrt{n}` gilt, wenn :math:`k \nmid n` dann gilt:
        :math:`\forall a < \sqrt{n}` ebenfalls :math:`(k*a)\nmid n`

Sieb des Eratosthenes
***********************

Algorithmus um herauszufinden, ob eine Zahl `n` eine Primzahl ist. Ist die Zahl keine Primzahl wird ein Teiler
zurückgegeben ansonsten 0. Der Algorithmus kann auch genommen werden um Primzahlen zu finden, wenn man anstatt eine
Zahl zurückgibt, den prim Array nimmt und schaut wo nch Ende des Durchlaufs noch true drin steht.

.. code-block:: none

    Sieb_des_eratosthenes(n)
        If n = 2 then return 0
        If 2 | n then return 2
        prim[2] <- true
        // prim ist ein Array in dem steht, welche Zahlen Primzahlen sind
        for k <- 3 to floor(sqrt(n)) do prim[k] <- k ist ungerade?
        for k <- 3 to floor(sqrt(n)) step 2 do
            if prim[k] then
                if k | n then return k
                j <- k^2
                // Alle kleineren k werden zuvor schon gestrichen
                while j <= floor(sqrt(n))
                    prim[j] <- false
                    j <- j + 2k
                    // ungerade + ungerade wäre gerade
                    // und diese wurden schon alle gestrichen
        return 0


Lemma 2: Primfaktorzerlegung
******************************

Jede natürliche Zahl :math:`n \ge 1` kann als Produkt von Primzahlen geschrieben werden. Ein solches Produkt wird
auch als :def:`Primfaktorzerlegung` bezeichnet. Dabei ist die Primfaktorzerlegung von 1, das leere Produkt, welches
auf den Wert 1 definiert ist.

Beweis:
^^^^^^^^

.. todo::

    Beweis

Beispiele:
^^^^^^^^^^^^

.. math::
    :nowrap:

    \begin{align*}
    10&=2*5\\
    24&=2*2*2*3=2^3*3\\
    29&= 29
    \end{align*}


Theorem 3:
***********

Für :math:`n\ge 1` gilt: Die Darstellung von :math:`n=p_0*p_1*...*p_n` mit Primzahlen :math:`p_i` und :math:`p_0\le p_1
\le ... \le p_n` ist eindeutig.

Beweis:
^^^^^^^^^^^^^^

.. todo::

    Beweis

