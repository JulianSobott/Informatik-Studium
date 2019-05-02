.. role:: def
    :class: underline

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


Beispiel:
^^^^^^^^^^^

1. .. math::
        :nowrap:

        \begin{align*}
        69+53 &= 122 \equiv 3 \; (mod\, 7)\\
        69+53 &\equiv 6+4 = 10 \equiv 3\; (mod\, 7)
        \end{align*}

2. .. math::
        :nowrap:

        \begin{align*}
        69*53 &= 3657 \equiv 3 \; (mod\, 7)\\
        69*53 &\equiv 6*4 = 24 \equiv 3\; (mod\, 7)
        \end{align*}

2. .. math::
        :nowrap:

        \begin{align*}
        69*53+29*23 &= 4324 \equiv 5 \; (mod\, 7)\\
        &\equiv 6*4+1*2 \equiv 3+2 \equiv 5\; (mod\, 7)
        \end{align*}

Folgerung 9:
************

Ist :math:`a\equiv_m b`, dann ist auch :math:`a^n\equiv_m b^n \;\;\forall n \ge 0`

Folgerung 10:
*************

Kongruenzen können bis auf die Division, wie normale Gleichungen umgeformt werden.

Beispiel:
^^^^^^^^^^

.. math::
    :nowrap:

    \begin{align*}
    x-4 &\equiv_7 6\\
    x &\equiv_7 6+4\\
    x &\equiv_7 3
    \end{align*}

.. todo::

    Beispiel: durch 3 teilbar

Divisions Alternative:
************************

Die oben genannten Rechenregeln erlauben keine herkömmliche Division. Es gilt z.B :math:`6=2*3\equiv 10=2*5\;(mod\,4)`.
Beide Seiten enthalten den Faktor 2. Teilt man jedoch beide Seiten durch 2, gilt die Kongruenz nicht mehr.
Allerdings kann in bestimmten Fällen ein Faktor durch eine entsprechende Multiplikation entfernt werden.

Beispiel:
^^^^^^^^^^

.. math::
    :nowrap:

    \begin{align*}
    32 &= 2*2*2*2*2\equiv 22=2*11 \pmod 5\\
    &\Leftrightarrow 2*2*2*2*(2*3)\equiv (2*3)*11\pmod 5\\
    &\Leftrightarrow 2*2*2*2*1\equiv 1*11\pmod 5\\
    \end{align*}

**Hinweis:** :math:`2*3 \mod 5 = 1`


Definition 10: Inverses
*************************

Ein Faktor :math:`x\in \mathbb{Z}_m` (:any:`Def. 3: mögliche Reste <01_01_def_03>`) für den gilt
:math:`a*x\equiv 1\pmod m` nennt man :def:`Inverses zu a modulo m`. Man schreibt für x dann :math:`a^{-1}`.

Definition 11: teilerfremde Menge
**********************************

Die Menge der zu m teilerfremden Zahlen wird als :math:`Z_m^*` bezeichnet. :math:`Z_m^*\subseteq Z_m`

Beispiel:
^^^^^^^^^^

:math:`Z_2^*=\{1\}`, :math:`Z_3^*=\{1,2\}`, :math:`Z_4^*=\{1,3\}`, :math:`Z_5^*=\{1,2,3,4\}`, :math:`Z_6^*=\{1,5\}`

.. _dm_03_theorem_06:

Theorem 6:
***********

:math:`a \perp m \Rightarrow \exists! z\in Z_m^*: z=a^{-1}*b \pmod m`

**Hinweis:** :math:`\exists! z\in Z_m^* \widehat{=}` "Es gibt genau ein z in :math:`Z_m^*`". D.h. z ist eindeutig.`

Beweis:
^^^^^^^^^^

1. Zeigen, dass eine Lösung existiert

    .. math::
        :nowrap:

        \begin{align*}
        &\exists a^{-1}: a*a^{-1}\equiv 1\pmod m \Rightarrow d\in \mathbb{Z}:a*a^{-1} = todo (d*m+1)\pmod m\\
        &\Rightarrow 1\equiv todo a*a^{-1}-d*m.\\
        \\
        &a\perp m \overset{Folgerung 6}{\Rightarrow} ggT(a,m)=1 \\
        &\overset{Theorem 2}{\Rightarrow} \exists \text{ eine Linearkombination der Form: }\,1=c*a+d*m\\
        \\
        &\text{Ersetze: } c=a^{-1}\text{ und } d=-d \Rightarrow 1=a*a^{-1}-d*m \\
        &\Rightarrow \text{Da c und d mittels des euklidschen Algorithmus berechnet werden können, }\\
        &\text{muss mindestens eine Lösung existieren, die Kongruent zu c in } Z_m \text{ ist.}
        \end{align*}

2. Zeigen, dass die Lösung eindeutig ist

    .. math::
        :nowrap:

        \begin{align*}
        &\text{Angenommen es gibt die Lösungen } e,f\in Z_m. \text{Dann muss gelten: }\\
        &a*e\equiv b\equiv a*f \pmod m \\
        &\Leftrightarrow a^{-1}*a*e\equiv a^{-1}*b\equiv a^{-1}*a*f\pmod m\\
        &\Leftrightarrow e\equiv a^{-1}*b\equiv f\pmod m\\
        &\Leftrightarrow e\equiv f\pmod m\\
        \end{align*}

**Hinweise:**

- Wenn gilt :math:`a\not\perp m`, also insbesondere wenn :math:`ggT(a,m)>1`, gilt das obige Theorem nicht.
- Außerhalb von :math:`Z_m` existieren unendlich viele Lösungen

Damit lassen sich nun Kongruenzen der Form :math:`a*x\equiv b \pmod m` für :math:`a\in Z_m^*` nach x auflösen:
:math:`x\equiv a^{-1}*b \pmod m`

.. todo::

    Beispiel

Folgerung 11:
**************

:math:`p \text{ prim } \cap a*x\equiv b \pmod p \Rightarrow \forall a: \exists a^{-1}\in Z_m`

Folgerung 12:
*************

:math:`(a)_{\mod m}^{-1} \in Z_m^*`

:math:`(a)_{\mod m}^{-1}\widehat{=}` das Inverse von a modulo m.

Für die Kongruenz :math:`a*x\equiv b \pmod m` mit :math:`a \perp m` und :math:`a\in Z_m^*` lässt sich das Inverse zu a
mittels des erweiterten euklidschen Algorithmus errechnen. Vertauscht man die Rollen von :math:`a` und
:math:`a^{-1}` und :math:`d` mit :math:`m` erhält man durch den erweiterten euklidschen Algorithmus die selbe
Linearkombination: :math:`1=a*a^{-1}+d*m`. Daher gilt, dass auch das Inverse zu a modulo m in :math:`Z_m^*` enthalten
sein muss.

Simultane Kongruenz:
*********************

Eine :def:`simultane Kongruenz ganzer Zahlen` ist ein System von linearen Kongruenzen.

Betrachten wir nun den Fall, dass zwei lineare Kongruenzen gegeben sind:

.. math::
    :nowrap:

    \begin{align*}
    a_1*x&\equiv b_1 \pmod m\\
    a_2*x&\equiv b_2 \pmod h\\
    \end{align*}

Angenommen es gilt: :math:`a_1\perp m` und :math:`a_2\perp h`. Mithilfe von :any:`Theorem 6 <dm_03_theorem_06>`:

.. math::
    :nowrap:

    \begin{align*}
    x&\equiv a_1^{-1}*b_1 \pmod m\\
    x&\equiv a_2^{-1}*b_2 \pmod h\\
    \end{align*}

Gesucht werden also Werte für x, die modulo m und modulo h gleich sind.

Theorem 7: Chinesischer Restsatz
**********************************

Sei :math:`m\perp h`. Für :math:`a\in Z_m` und :math:`b\in Z_h` haben die beiden Kongruenzen

.. math::
    :nowrap:

    \begin{align*}
    x&\equiv a \pmod m\\
    x&\equiv b \pmod h\\
    \end{align*}

, die eindeutige gemeinsame Lösung:

.. math::
    x=(a*h'*h+b*m'*m) \mod m*h

Dabei gilt:

:math:`x\in Z_{mh}`,

:math:`h'=(h)_{\mod m}^{-1}=` Inverse zu h modulo m,

:math:`m'=(m)_{\mod h}^{-1}=` Inverse zu m modulo h

.. todo::

    Beweis

.. todo::

    Beispiel

Theorem 8: Verallgemeinerter Chinesischer Restsatz
****************************************************

Gegeben sind die Kongruenzen:

.. math::
    :nowrap:

    \begin{align*}
    x&\equiv a_1 \pmod {n_1}\\
    x&\equiv a_2 \pmod {n_2}\\
    &...
    x&\equiv a_k \pmod {n_k}\\
    \end{align*}

Dabei sind die :math:`n_i`'s paarweise teilerfremd. Dann kann man mit :math:`n=\prod_{i=1}^k n_i`, eine Lösung x wie
folgt berechnet werden:

.. math::
    x=(\sum_{i=1}^k a_i*(\frac{n}{n_i})_{\mod n_i}^{-1}*\frac{n}{n_i}) \mod n

.. _03_th_09:

Theorem 9: Eulersche :math:`\varphi`-Funktion
**************************************************

Die Eulersche :math:`\varphi`-Funktion ist:

.. math:: \varphi(m) = \vert Z_m^*\vert

Für `p` prim gilt:

.. math:: \varphi(m)=m* \prod_{p\mid m}(1-\frac{1}{p})

.. todo::

    BSP.

Theorem 10: Satz von Euler
******************************

Für alle :math:`n\ge 2` und alle :math:`a\in Z_m^*` ist:

.. math:: a^{\varphi(n)} \equiv 1 \pmod{n}


.. todo::

    Beweis

Folgerung 13:
****************************

Für alle Primzahlen `p` und :math:`a\in\{1,...,p\}` gilt:

.. math:: a^{p-1}\equiv 1 \pmod{p},

da nach :ref:`Theorem 9 <03_th_09>`: :math:`\varphi(p)=p-1`

Theorem 11: Kleiner Satz von Fermat
****************************************

Für eine Primzahl `p` und eine beliebige ganze Zahl `a` gilt:

.. math:: a^p\equiv a\pmod{p}

.. todo::

    RSA
