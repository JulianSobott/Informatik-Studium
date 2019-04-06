Kongruenzen
==============

.. contents::
    :local:

Die Kongruenz-Relation :math:`\equiv_m` setzt ganze Zahlen, die den gleichen rest bei der Division durch eine
natürliche Zahl :math:`n\ge 1` haben, in Relation.

Definition 9: Kongruenz
**************************

Sei :math:`m,a,b \in \mathbb{Z}, m\ge 1`.

:math:`a\equiv_m b \Leftrightarrow a\equiv b (mod\;m)\Leftrightarrow a\; mod\; m= b\; mod\; m`

Beispiel:
^^^^^^^^^^

:math:`1\equiv 4\equiv 7\equiv -2 \equiv -5 \;(mod\; 3)` //:math:`(-5+2*3=1)`


Äquivalenzklassen und -relationen
**********************************

Da die Kongruenz mittels Gleichheit definiert ist, handelst es sich um eine Äquivalenzrelation (R, S, T). Daher gibt
es sogenannte Äquivalenzklassen. Eine Äquivalenzklasse ist eine Menge, die alle Zahlen enthält, die modulo eines
bestimmten Modulos einen bestimmten Rest ergeben.

Beispiel:
^^^^^^^^^^

:math:`[2]_5 = \{...,-8,-3,2,7,12,...\}=\{5*t+2\mid t\in \mathbb{Z}\}`

:math:`[r]_m = \{k*m+r\mid k\in \mathbb{Z}\}`

Rechenregeln für Kongruenzen
********************************

- :math:`a \equiv_m 0 \Leftrightarrow m\mid a`

Theorem 5:
**********

Sei :math:`a,b \in \mathbb{Z}`, dann gilt für :math:`m\ge 1`: :math:`a\equiv_m b \Leftrightarrow m\mid(a-b)`

.. todo::

    Beweis

Beispiel:
^^^^^^^^^^

:math:`a=22`, :math:`b=7`

:math:`7\equiv_m 22`

:math:`a-b=22-7=15 \Rightarrow 5\mid 15`


Folgerung 8:
*************

:math:`a\equiv_m b \Leftrightarrow a-b \equiv_m 0`


Lemma 3:
***********

Sei :math:`a\equiv_m b` und :math:`c\equiv_m d`, dann gilt:

1. :math:`a+c \equiv_m b+d`
2. :math:`a-c \equiv_m b-d`
3. :math:`a*c \equiv_m b*d`

**Hinweis:** Dies gilt insbesondere auch wenn :math:`c=d`. D.h. ähnlich wie bei Gleichungen können beide Seiten der
Kongruenz gleichmäßig erhöht, verringert oder multipliziert werden. Vorsicht: für die Division gilt dies nicht!

Weiterhin gelten obige Regeln auch für z.B. :math:`c=m` und :math:`d=0`. D.h. der Modul kann zu einer Seite der
Kongruenz addiert, subtrahiert oder multipliziert werden, ohne die andere Seite zu verändern.

.. todo::

    Beweis