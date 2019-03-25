Wahrscheinlichkeitsräume
=============================

.. contents::
    :local:


Definition 1: Wahrscheinlichkeitsraum
**************************************

.. role:: def
    :class: underline


Ein (diskreter [#f1]_) :def:`Wahrscheinlichkeitsraum` ist eine :def:`Ergebnissmenge`
:math:`\Omega = \{\omega_1, \omega_2\, \omega_3, ...\}` [#f2]_ von :def:`Elementarerignissen`
:math:`\omega_1, \omega_2\, \omega_3, ...` . Jedem :math:`\omega_i` ist eine :def:`Wahrscheinlichkeit`
:math:`Pr[\omega_i]` zugeordnet, so dass gilt:

    - :math:`0\le Pr[\omega_i] \le 1`
    - :math:`\sum_{\omega_i\in \Omega} Pr[\omega_i] = 1`


Definition 2: Ereignis
************************

Die Wahrscheinlichkeit von :def:`Ereignis` :math:`E\subseteq\Omega` ist:

.. math:: Pr[E] = \sum_{\omega\in E} Pr[\omega]

Ein Ereignis E :def:`tritt ein`, wenn eines der Elementarereignissen aus E eintritt.

Speziell:
^^^^^^^^^^

    - :math:`\emptyset` - das :def:`unmögliche Ereignis`
    - :math:`\Omega` - das :def:`sichere Ereignis`

Definition 3: Komplementär Ereignis
************************************

Das :def:`komplementäre Ereignis` zu E ist :math:`\bar E=\Omega-E`.

Definition 4: Relative Häufigkeit bzw. Wahrscheinlichkeit
*************************************************************

Statistik über die Häufigkeit von Ereignis E.

:def:`Relative Häufigkeit (E)` :math:`=\frac{absolute Häufigkeit (E)}{Anzahl Messungen}`

Relative Häufigkeiten gelten als Erwartungen für die Zukunft und können als :def:`Wahrscheinlichkeiten` (en:
*propability*) betrachtet werden.

Für die Wahrscheinlichkeit eines Ereignisses E, werden die Wahrscheinlichkeiten der Elementarereignissen in E
aufsummiert.

Definition 5: Laplace Experiment:
***********************************

Alle Elementarereignisse :math:`\omega_i` einer endlichen Ergebnismenge :math:`\Omega` sind gleich wahrscheinlich.

.. math:: Pr[\omega]=\frac{1}{\vert\Omega\vert}, \;\; \forall\omega\in\Omega

Allgemein für ein Ereignis E:

.. math:: Pr[E]=\frac{\vert E\vert}{\vert\Omega\vert}

Lemma:
^^^^^^^^^^^^

:math:`0\le\frac{1}{\vert\Omega\vert}\le 1` und

:math:`\sum_{\omega\in\Omega}Pr[\omega]=\sum_{\omega\in\Omega}\frac{1}{\vert\Omega\vert}=
\frac{1}{\vert\Omega\vert}\sum_{\omega\in\Omega}1=\frac{1}{\vert\Omega\vert} * \vert\Omega\vert = 1`

Beispiele:
^^^^^^^^^^^^^^

1. Würfel (Laplace Experiment)

    :math:`\Omega=\{1,2,3,4,5,6\}`

    :math:`Pr[k]=\frac{1}{6}` mit :math:`1\le k\le 6`

    Ereignis :math:`P=\{k\in\Omega\mid k\; ist\; prim\} = \{2,3,5\}`

    :math:`Pr[P]=3*\frac{1}{6}=\frac{1}{2}`

2. Münze: 3-mal werfen (Laplace Experiment)

    :math:`\Omega=\{k,z\}^3`  , :math:`\vert\Omega\vert = 8`

    :math:`Pr[\omega]=\frac{1}{8}`

    E = genau einmal k

    :math:`Pr[E]=3*\frac{1}{8}=\frac{3}{8}`

3. Urne:

    5 Bälle, 2 rot (r) und 3 schwarz (s)

    Ziehe 2 mal ohne Zurücklegen.

    :math:`\Omega=\{r,s\}^2`  , :math:`\vert\Omega\vert = 4`

    .. todo::

        Baumdiagramm Bild einfügen

    E = 2. Kugel ist rot :math:`=\{sr, rr\}`

    :math:`Pr[E]=\frac{3}{10}+\frac{1}{10}=\frac{4}{10}=\frac{2}{5}`

Eigenschaften
**************

Seien :math:`A,B\in\Omega` Ereignisse.

1. :math:`Pr[\emptyset]=0`, (da :math:`0\le Pr[\emptyset]\le 1-Pr[\Omega]=0`) und :math:`Pr[\Omega]=1` (nach Definition)
2. :math:`Pr[\bar A]=1-Pr[A]`

        :math:`A \cup \bar A= \Omega \Rightarrow Pr[\bar A] + Pr[A] = Pr[\Omega] = 1`

3. :math:`A\subseteq B \Rightarrow Pr[A] \le Pr[B]`

        :math:`Pr[B]=\sum_{\omega\in B}Pr[\omega]=\sum_{\omega\in A}Pr[\omega] + \sum_{\omega\in B-A}Pr[\omega] \ge
        \sum_{\omega\in A}Pr[\omega]=Pr[A]`

4. :math:`A \cap B = \emptyset \Rightarrow Pr[A \cup B]=Pr[A] + Pr[B]`

        :def:`Additionssatz`: :math:`\sum_{\omega\in A \cup B}Pr[\omega] =
        \sum_{\omega\in A}Pr[\omega] + \sum_{\omega\in B}Pr[\omega]`

        Allgemeiner für :math:`A_1, A_2, ...` paarweise disjunkt gilt:

        .. math:: Pr[\bigcup_{i\ge 1}A_i]=\sum_{\omega\in A}Pr[A_i]

5. :math:`Pr[A \cup B]=Pr[A]+Pr[B]-Pr[A \cap B]`

        :def:`Siebformel`:

        .. math::
            :nowrap:

            \begin{align*}
            \vert A\cup B\vert &= \vert A\vert + \vert B\vert -\vert A\cap B\vert\\

            \vert A\cup B \cup B\vert &= \vert A\vert + \vert B\vert +\vert C\vert  -(\vert A\cap B\vert +
            \vert A\cap C\vert + \vert B\cap C\vert) + \vert A\cap B \cap C\vert
            \end{align*}



.. rubric:: Fußnoten

.. [#f1] Aufzählbar und isolierte Objekte
.. [#f2] Unendlich viele Objekte möglich
