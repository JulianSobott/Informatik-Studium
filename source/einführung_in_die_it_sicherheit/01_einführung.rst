Einführung
==============

Datenschutz vs. Datensicherheit
*********************************



**Datenschutz:**

Die Gewährleistung der Rechte von Betroffenen bei der Verarbeitung ihrer personenbezogener Daten. Also der Schutz
der Personen. Bei Datenschutzverletzungen werden die Persönlichkeitsrechte und Grundrechte von Menschen verletzt.


**Datensicherheit/Security:**

*Schutz von Informationssystemen. Die Arte der daten spielt keine Rolle.* Die technische Sicherung, Erhaltung und
Verfügbarkeit der
Datenverarbeitungssysteme und der mit ihnen verarbeiteten Daten. Die Datensicherheit betrifft alle Daten im
Unternehmen, unabhängig davon ob es sich um personenbezogene Daten handelt, oder um daten ohne Personenbezug.
Probleme bei der Datensicherheit führen zum Verlust oder zur Verfälschung von Daten und zur unberechtigten
Einsichtnahme durch Dritte in die Daten. Im schlimmsten Fall kann mangelnde Datensicherheit ein Unternehmen
ruinieren, auch wenn keine personenbezogenen Daten betroffen sind.
Die Sicherstellung der Datensicherheit personenbezogener Daten ist also ebenfalls eine wichtige Aufgabe im
Datenschutz.

**Safety:**

Die physische Sicherheit, also die Verfügbarkeit von Daten und IT.


IT-Sicherheit in Unternehmen
**********************************************

Risiken:
- Social engineering
- veraltete Software
- Cloudanbieter

Folgen von zu geringer IT-Sicherheit:
- Finanzieller Schaden
- Wirtschaftsspionage
- Datenverlust
- Image schaden
- Produktionsausfall


OWASP Top 10:
***************

Definiert die top 10 größten Sicherheitsrisiken in Software.

1. **Injection**: e.g. SQL-injection
2. **Broken Authentication**: Fehlerhafte implementierte Funktionen für Authentisierung oder Session Management
3. **Sensitive Data Exposure**: WEB API schützt sensible Daten nicht richtig. z.B. keine Verschlüsselung
4. **XML External Entities (XXE)**: XML-Verarbeitungsanwendungen werten auch Referenzen auf externe XML Dokumente aus
5. **Broken Access Control**: Einschränkungen für authentisierte Benutzer werden nicht hinreichend umgesetzt
6. **Security Misconfiguration**: Unsichere Konfiguration von Diensten, die extern erreichbar sind. (z.B. Standardeinstellung)
7. **Cross-Site Scripting (XSS)**: Einbetten nicht vertrauenswürdiger Daten in eine Website ohne Überprüfung
8. **Insecure Deserialization**: Unzureichende Überprüfung von vom Nutzer eingegebener Daten, vor dem Deserialisieren
9. **Using Components with Known Vulnerabilities**: Einsatz von Software mit bekannten Sicherheitslücken
10. **Insufficient Logging & Monitoring**

5 Säulen der IT-Sicherheit
******************************

Die 5 Säulen geben vor auf was im Bezug auf IT-Sicherheit geachtet werden, wenn es um Daten geht. Also um das
speichern aber insbesondere auch beim Übertragen von Daten.

1. **Confidentiality (Vertraulichkeit)**: Nur autorisierte Personen können die Daten verstehen. z.B. Verschlüsselung
2. **Authenticity (Authentizität)**: Daten wurden wirklich vom angegebenen Urheber erstellt und nicht von jemand anderem
3. **Non-/Repudiation (Verbindlichkeit)**:
    - Non-Repudiation: Es kann sicher festgestellt werden, wer die Daten abgesendet hat
    - Repudiation: Ein Absender soll abstreiten können etwas gesandt zu haben. z.B. Anonymisierung
4. **Integrity (Integrität)**: Daten können nicht unbemerkt verfälscht werden
5. **Availability (verfügbarkeit)**: Daten sind immer dann verfügbar wenn sie benötigt werden

3 wichtigsten Ziele der IT-Sicherheit: CIA Triad
*************************************************

Von diesen 5 Säulen, werden 3 als die wichtigsten angesehen. Es können jedoch nie alle 3 erreicht werden, da sie
teilweise widersprüchlich sind.

- Availability
- Confidentiality
- Integrity

**Availability vs. Confidentiality:** Information öffentlich im Internet verfügbar, dann kann sie nicht geheim gehalten
werden. Durch (sicheres) Löschen einerInformation kann garantiert werden, dass niemand Zugriff darauf bekommt.
Dann ist die Information aber auch nicht mehr verfügbar.

**Availability vs. Integrity:** Je mehr (unabḧangige) Systeme eine Information enthalten, desto vefügbarer ist sie.
Je mehr und unabhängiger die Systeme sind, desto schwerer ist es die Integrität der Information zu gewährleisten. Die
Integrität einer Information ist garantiert wenn niemand diese ändern kann.

**Confidentiality vs. Integrity:** Je geheimer einer Information ist,desto weniger ”Kopien” sollte es geben. Um
Integrität zu garantieren müsste aber irgendwo eine ”Kopie” der Information vorhanden sein. Je mehr die Integrität
einerInformation geschützt ist, desto mehr muss zusätzlich über die Information gespeichert werden (bis hin zur
vollständigen Kopie)






