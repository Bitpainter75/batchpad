# Microsoft 365 - Kontakte
Microsoft365ContactList
-----------------------

Die Aktion **Microsoft365ContactList** ruft eine Liste von Kontakten aus dem Microsoft 365-Konto ab und speichert sie in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365ContactList Data="{@myData}" Filter="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Ergebnisdaten der Kontakte gespeichert werden.
*   **Filter**: (Optional) Ein Filter zur Einschränkung der Kontakte.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Kontakte abgerufen werden sollen.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365ContactList Data="{@myData}" Filter="startswith(DisplayName, 'M')" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel werden alle Kontakte abgerufen, deren Anzeigename mit **M** beginnt. Die Ergebnisse werden in **{@myData}** gespeichert.

Die möglichen Filter entsprechen den Filterkriterien der MSGraph API: [https://learn.microsoft.com/de-de/graph/filter-query-parameter](https://learn.microsoft.com/de-de/graph/filter-query-parameter)

Microsoft365ContactReadJson
---------------------------

Die Aktion **Microsoft365ContactReadJson** liest die MSGraph Details eines bestimmten Kontakts und speichert sie im JSON-Format in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365ContactReadJson ContactId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ContactId**: Die ID des Kontakts, dessen Details abgerufen werden sollen.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Kontakt gelesen werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert.

Beispiel:

```text-x-trilium-auto
<Microsoft365ContactReadJson ContactId="12345" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Dieses Beispiel liest die Details des Kontakts mit der ID **12345** und speichert sie in der Variablen **{@Result}**.

Microsoft365ContactCreate
-------------------------

Die Aktion **Microsoft365ContactCreate** erstellt einen neuen Kontakt im Microsoft 365-Konto.

```text-x-trilium-auto
<Microsoft365ContactCreate DisplayName="" GivenName="" Initials="" MiddleName="" NickName="" Surname="" Title="" Birthday="" EmailAddresses="" Jobtitle="" CompanyName="" BusinessHomePage="" BusinessPhones="" MobilePhone="" HomePhones="" HomeAddressStreet="" HomeAddressPostalCode="" HomeAddressCity="" HomeAddressState="" HomeAddressCountry="" BusinessAddressStreet="" BusinessAddressPostalCode="" BusinessAddressCity="" BusinessAddressState="" BusinessAddressCountry="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **DisplayName**: Der Anzeigename des Kontakts.
*   **GivenName**: Der Vorname des Kontakts.
*   **Surname**: Der Nachname des Kontakts.
*   **EmailAddresses**: Eine kommagetrennte Liste von E-Mail-Adressen.
*   **MobilePhone**, **BusinessPhones**, **HomePhones**: Kommagetrennte Listen von Telefonnummern des Kontakts.
*   **Birthday**: Das Geburtsdatum des Kontakts.
*   **HomeAddress** und **BusinessAddress**: Attribute für Straßenname, PLZ, Stadt, Bundesland und Land des Kontakts.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, für den der Kontakt erstellt wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert.

Beispiel:

```text-x-trilium-auto
<Microsoft365ContactCreate DisplayName="Max Mustermann" GivenName="Max" Surname="Mustermann" EmailAddresses="max@example.com" MobilePhone="+49123456789" Birthday="1985-10-15" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt einen neuen Kontakt mit dem Namen Max Mustermann, einer E-Mail-Adresse und einer Telefonnummer.

Microsoft365ContactUpdate
-------------------------

Die Aktion **Microsoft365ContactUpdate** aktualisiert die Details eines bestehenden Kontakts.

```text-x-trilium-auto
<Microsoft365ContactUpdate ContactId="" DisplayName="" GivenName="" Initials="" MiddleName="" NickName="" Surname="" Title="" Birthday="" EmailAddresses="" Jobtitle="" CompanyName="" BusinessHomePage="" BusinessPhones="" MobilePhone="" HomePhones="" HomeAddressStreet="" HomeAddressPostalCode="" HomeAddressCity="" HomeAddressState="" HomeAddressCountry="" BusinessAddressStreet="" BusinessAddressPostalCode="" BusinessAddressCity="" BusinessAddressState="" BusinessAddressCountry="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ContactId**: Die ID des zu aktualisierenden Kontakts.
*   **DisplayName**: Der Anzeigename des Kontakts.
*   **GivenName**: Der Vorname des Kontakts.
*   **Surname**: Der Nachname des Kontakts.
*   **EmailAddresses**: Eine kommagetrennte Liste von E-Mail-Adressen.
*   **MobilePhone**, **BusinessPhones**, **HomePhones**: Kommagetrennte Listen von Telefonnummern des Kontakts.
*   **Birthday**: Das Geburtsdatum des Kontakts.
*   **HomeAddress** und **BusinessAddress**: Attribute für Straßenname, PLZ, Stadt, Bundesland und Land des Kontakts.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, für den der Kontakt erstellt wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert.

Beispiel:

```text-x-trilium-auto
<Microsoft365ContactUpdate ContactId="12345" DisplayName="Max Mustermann" EmailAddresses="max.neu@example.com" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Aktualisiert den Kontakt mit der ID **12345** und ändert die E-Mail-Adresse in **max.neu@example.com**.

Microsoft365ContactDelete
-------------------------

Die Aktion **Microsoft365ContactDelete** löscht einen bestehenden Kontakt.

```text-x-trilium-auto
<Microsoft365ContactDelete ContactId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ContactId**: Die ID des zu löschenden Kontakts.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Kontakt gelöscht werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert.

Beispiel:

```text-x-trilium-auto
<Microsoft365ContactDelete ContactId="12345" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Kontakt mit der ID **12345** für den Benutzer **benutzer@example.com**.