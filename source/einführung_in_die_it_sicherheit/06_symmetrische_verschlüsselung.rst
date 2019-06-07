Kryptographie - Symmetrische Verschlüsselung
=================================================

Warum ist Kryptographie für IT-Sicherheit so wichtig? Erklärung anhand der 5 Säulen der ITS
----------------------------------------------------------------------------------------------------------------------

- **Vertraulichkeit:** nur befugte verstehen die Daten. (Verschlüsselung)
- **Authenzität:** Daten stammen von angegebenen Urheber. (Digitale Signatur)
- **Verbindlichkeit:** Nachverfolgbar, dass Daten gesendet wurden, und wie oft. (Zeitstempel)
- **Integrität:** Daten wurden nicht im Nachhinein manipuliert. (Message Digests)

Was erzeugt ein pRNG im Gegensatz zu einem RNG?
----------------------------------------------------------------------------------------------------------------------
Ein pRNG (pseudo random number generator) erzeugt keine wirklichen Zufallszahlen. Es sieht nur zufällig aus. Ein RNG
generiert richtige Zufallszahlen.

Was haben One-Time-Pads mit absoluter Sicherheit zu tun?
----------------------------------------------------------------------------------------------------------------------

Jede Information, wird mit einem anderem Schlüssel verschlüsselt.

Absolute/informationstheoretische Sicherheit: Chiffretext gibt keine Hinweise auf Plaintext. Anzahl
möglicher Schlüssel > Anzahl möglicher Plaintexte.

Wieso ist security by obscurity schlecht? Welches Prinzip (mit Erklärung) sollte stattdessen verwendet werden?
----------------------------------------------------------------------------------------------------------------------

Sobald der Quellcode in die öffentlichkeit gelangt, ist der Algorithmus nicht mehr sicher. **Das einzige Geheimnis
sollte der Schlüssel sein, während die Algorithmen öffentlich bekannt sind. Es gibt genügend Kryptosysteme, die diese
Anforderung erfüllen.


Was unterscheidet eine Blockchiffre von einer Stromchiffre?
----------------------------------------------------------------------------------------------------------------------

- Eine Stromchiffre kann unendlich lang sein.
- Eine Blockchifre hingegen hat immer eine feste Größe. Längere Daten werden in mehrere Blöcke zerlegt

Nenne Sie jeweils einen Vor- und einen Nachteil von Selbstsynchronisierenden Stromchiffren.
----------------------------------------------------------------------------------------------------------------------

Vorteile:
- Selbst bei identischen Schlüsseln, unterscheiden sich die Geheimtexte, wenn sich die plaintexte unterscheiden.
- Wenn Bits verloren gehen, synchronisiert sich das System selbst

Nachteile:
- Replay attacks sind möglich
- Keine Berechnung der Schlüsselbits im Voraus

Wie funktioniert DES? (Zeichnung)
----------------------------------------------------------------------------------------------------------------------

.. todo:: Zeichnung einfügen