Bedingte Wahrscheinlichkeiten
================================

.. role:: def
    :class: underline


.. contents::
    :local:

.. figure:: assets/mengendiagramm_01.png
    :alt: Mengendiagramm mit den Mengen `A` und `B`

    Mengendiagramm mit den Mengen `A` und `B`

**Frage:** Wk. von `A`, wenn man bereits weiß, dass `B` eingetreten ist.

Definition 1: Bedingte Wahrscheinlichkeit
*******************************************

:math:`\Omega` Wk.raum, :math:`B \subseteq \Omega`, :math:`A \subseteq \Omega` und :math:`Pr[B]>0`. Die
:def:`bedingte Wahrscheinlichkeit A gegeben B` ist definiert durch:

.. math::

    Pr[A\mid B]=\frac{Pr[A\cap B]}{Pr[B]}

Falls :math:`Pr[B]=0`, definiere: :math:`Pr[A\mid B]=0`

Eigenschaften: Bedingte Wahrscheinlichkeit
*********************************************

1. :math:`A=B: \;\; Pr[B\mid B] =\frac{Pr[B\cap B]}{Pr[B]}=1`
2. :math:`A \cap B=\emptyset : \;\; Pr[A\mid B] =\frac{Pr[\emptyset]}{Pr[B]}=0`
3. :math:`B=\Omega : \;\; Pr[A\mid \Omega] =\frac{Pr[A \mid \Omega]}{Pr[\Omega]}=Pr[A]`

Beispiele:
^^^^^^^^^^^^

1. Würfel (Laplace Experiment)

    :math:`p=Primzahl=\{2,3,5\}`, :math:`u=ungerade=\{1,3,5\}`, :math:`p\cap u=\{3,5\}`

    :math:`Pr[p]=Pr[u]=\frac{1}{2}`

    :math:`Pr[p \mid u]=\frac{Pr[p\cap u]}{Pr[u]}=\frac{\frac{1}{3}}{\frac{1}{2}}=\frac{2}{3}`

2. 2 Kinder

    :math:`\Omega=\{j,m\}^2=\{jj, jm, mj, mm\}`

    :math:`B=\{jm, mj, mm\}`, :math:`A=\{mm\}`, :math:`A\cap B=\{mm\}`

    :math:`Pr[A \mid B]=\frac{Pr[A \cap B]}{Pr[B]}=\frac{\frac{1}{4}}{\frac{3}{4}}=\frac{1}{3}`

    C = 1. Kind ist :math:`m=\{mj, mm\}`

    :math:`Pr[A \mid C]=\frac{Pr[A \cap C]}{Pr[C]}=\frac{\frac{1}{4}}{\frac{1}{2}}=\frac{1}{2}`

.. _02_multiplikationssatz:

Multiplikationssatz
*********************

Seien :math:`A_1,A_2,...,A_n \subseteq \Omega` Ereignisse mit :math:`Pr[A_1\cap A_2\cap ... \cap A_n]>0`. Dann gilt:

.. math::

    Pr[A_1\cap A_2\cap ... \cap A_n]=Pr[A_1]*Pr[A_2\mid A_1] * Pr[A_3\mid A_1\cap A_2] * Pr[A_n\mid A_1\cap A_2\cap
    ... \cap A_{n-1}]

Beweis:
^^^^^^^^

Definition einsetzen: :math:`Pr[A_1\cap A_2\cap ... \cap A_n]=Pr[A_1] * \frac{Pr[A_1\cap A_2]}{Pr[A_1]} *
\frac{Pr[A_1\cap A_2 \cap A_3]}{Pr[A_1 \cap A_2]} * \frac{Pr[A_1\cap A_2 \cap ... \cap A_n]}{Pr[A_1\cap A_2 \cap ...
\cap A_{n-1}]}`

Alle Nenner sich durch den vorherigen Zähler raus. Nur der Zähler vom letzten Term bleibt stehen. Somit stimmt die
Gleichung.

**Beachte:** :math:`A_1 \supseteq A_1 \cap A_2 \supseteq ... \supseteq A_1 \cap ... \cap A_n`

:math:`\Rightarrow Pr[A_1]\ge Pr[A_1\cap A_2] \ge ... \ge Pr[A_1 \cap ... \cap A_n] \ge 0`


Beispiel: Geburtstagsproblem
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

:math:`\Omega=\{1,2,...,n=365\}`, :math:`m` Personen zufällig.

A = alle `m` Personen haben an unterschiedlichen Tagen Geburtstag.

Personen :math:`1, 2, ..., m`

:math:`A_i=` Person `i` hat an einem anderen Tag Geburtstag als die Personen :math:`1,2,.., i-1`.
D.h. :math:`A=A_1\cap A_2 \cap ... \cap A_m`

:math:`Pr[A_1] = 1`

:math:`Pr[A_2\mid A_1] = \frac{n-1}{n}`

:math:`Pr[A_3\mid A_1 \cap A_2] = \frac{n-2}{n}`

:math:`Pr[A_j\mid A_1 \cap A_2 \cap ... \cap A_{j-1}] = \frac{n-(j-1)}{n}`

Nach :ref:`02_multiplikationssatz`:

.. math::
    :nowrap:

    \begin{align*}
    Pr[A]&=1*\frac{n-1}{n}*\frac{n-2}{n}*...*\frac{n-(m-1)}{n}\\
    &=\prod_{j=1}^m\frac{n-(j-1)}{n} = \prod_{j=1}^m (1-\frac{j-1}{n} \le \prod_{j=1}^m e^{-\frac{j-1}{n}} \le\\
    &\le e^{-\frac{1}{n}* \sum_{j=1}^m (j-1)} = e^{-\frac{1}{n}* \sum_{j=0}^{m-1} (j)} = e^{-\frac{(m-1)m}{2n}}\\

    \end{align*}

.. todo::

    Check formula end

**Hinweis:** :math:`1-x\le e^{-x}`