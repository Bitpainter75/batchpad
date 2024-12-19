# Microsoft 365 - Kalender
Microsoft365CalendarList
------------------------

Die Aktion ruft die Kalender eines Microsoft 365-Benutzers ab und speichert sie in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365CalendarList Data="{@myData}" Filter="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Kalender gespeichert werden.
*   **Filter**: (Optional) Ein Filter zur Einschränkung der abgerufenen Kalender.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Kalender abgerufen werden sollen.
*   **Account**: Gibt das zu verwendende Konto für die Abfrage an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarList Data="{@myCalendars}" Filter="" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel werden alle Kalender des Benutzers **benutzer@example.com** abgerufen und in der Variable **{@myCalendars}** gespeichert.

Microsoft365CalendarEventList
-----------------------------

Die Aktion ruft die Ereignisse eines bestimmten Kalenders im angegebenen Zeitraum ab und speichert sie in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365CalendarEventList Data="{@myData}" CalendarId="" StartDateTime="" EndDateTime="" Filter="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Ereignisse gespeichert werden.
*   **CalendarId**: Die ID des Kalenders, aus dem die Ereignisse abgerufen werden sollen.
*   **StartDateTime**: Startzeitpunkt des Zeitraums
*   **EndDateTime**: Endzeitpunkt des Zeitraums
*   **Filter**: (Optional) Ein Filter zur Einschränkung der Ereignisse.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventList Data="{@myEvents}" CalendarId="KalenderID123" StartDateTime="2024-01-01T00:00:00" EndDateTime="2024-01-31T23:59:59" Filter="startswith(Subject, 'Meeting')" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Hier werden alle Ereignisse aus dem Kalender mit der ID **KalenderID123** im Zeitraum Januar 2024 abgerufen. Es werden nur Ereignisse gefiltert, deren Betreff mit **Meeting** beginnt.

Die möglichen Filter entsprechen den Filterkriterien der MSGraph API: [https://learn.microsoft.com/de-de/graph/filter-query-parameter](https://learn.microsoft.com/de-de/graph/filter-query-parameter)

Microsoft365CalendarEventRead
-----------------------------

Liest die Details eines bestimmten Kalendereintrags und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365CalendarEventRead CalendarId="" EventId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, aus dem der Kalendereintrag gelesen werden soll.
*   **EventId**: Die ID des zu lesenden Kalendereintrags.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventRead CalendarId="KalenderID123" EventId="EreignisID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest die Details des Ereignisses mit der ID **EreignisID456** aus dem Kalender **KalenderID123** des Benutzers **benutzer@example.com**.

Microsoft365CalendarEventReadJson
---------------------------------

Liest die MSGraph Details eines bestimmten Kalendereintrags im JSON-Format und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365CalendarEventReadJson CalendarId="" EventId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, aus dem der Kalendereintrag gelesen werden soll.
*   **EventId**: Die ID des zu lesenden Kalendereintrags.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventReadJson CalendarId="KalenderID123" EventId="EreignisID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest die Details des Ereignisses mit der ID **EreignisID456** aus dem Kalender **KalenderID123** des Benutzers **benutzer@example.com**.

Microsoft365CalendarEventCreate
-------------------------------

Erstellt einen neuen Kalendereintrag in einem bestimmten Kalender.

```text-x-trilium-auto
<Microsoft365CalendarEventCreate CalendarId="" Subject="" StartDateTime="" EndDateTime="" IsAllDay="false" Location="" Body="" IsReminderOn="true" ReminderMinutesBeforeStart="15" Importance="normal" Sensitivity="normal" ShowAs="busy" Recurrence="daily" RecurrenceInterval="1" RecurrenceStartDateTime="" RecurrenceEndDateTime="" IsCancelled="false" IsOrganizer="true" OrganizerEmailAddress="" ResponseRequested="true" Attendees="" IsOnlineMeeting="true" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, in dem der Eintrag erstellt werden soll.
*   **Subject**: Der Betreff des Kalendereintrags.
*   **StartDateTime**: Startzeitpunkt des Ereignisses.
*   **EndDateTime**: Endzeitpunkt des Ereignisses.
*   **IsAllDay**: Gibt an, ob das Ereignis ganztägig ist (true oder false).
*   **Location**: Der Veranstaltungsort des Ereignisses.
*   **Body**: Die Beschreibung des Kalendereintrags.
*   **IsReminderOn**: Gibt an, ob eine Erinnerung aktiviert ist (true oder false).
*   **ReminderMinutesBeforeStart**: Zeit in Minuten vor dem Start für die Erinnerung.
*   **Importance**: Die Wichtigkeit des Ereignisses. Mögliche Werte:
    *   low
    *   normal
    *   high
*   **Recurrence**: Gibt die Wiederholung an. Mögliche Werte:
    *   none
    *   daily
    *   weekly
    *   monthly
*   **Attendees**: Eine kommagetrennte Liste von E-Mail-Adressen der Teilnehmer.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventCreate CalendarId="KalenderID123" Subject="Projektbesprechung" StartDateTime="2024-01-10T10:00:00" EndDateTime="2024-01-10T11:00:00" Location="Besprechungsraum A" Body="Projektstatusbesprechung" Attendees="teilnehmer1@example.com,teilnehmer2@example.com" Importance="high" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt ein neues Ereignis mit dem Betreff **Projektbesprechung**, den angegebenen Zeiten und Teilnehmern.

Microsoft365CalendarEventUpdate
-------------------------------

Aktualisiert die Details eines bestehenden Kalendereintrags in einem bestimmten Kalender.

```text-x-trilium-auto
<Microsoft365CalendarEventUpdate CalendarId="" EventId="" Subject="" StartDateTime="" EndDateTime="" IsAllDay="false" Location="" Body="" IsReminderOn="true" ReminderMinutesBeforeStart="15" Importance="normal" Sensitivity="normal" ShowAs="busy" Recurrence="daily" RecurrenceInterval="1" RecurrenceStartDateTime="" RecurrenceEndDateTime="" IsCancelled="false" IsOrganizer="true" OrganizerEmailAddress="" ResponseRequested="true" Attendees="" IsOnlineMeeting="true" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, in dem der Eintrag aktualisiert werden soll.
*   **EventId**: Die ID des zu aktualisierenden Kalendereintrags.
*   **Subject**: Der neue Betreff des Kalendereintrags.
*   **StartDateTime**: Startzeitpunkt des Ereignisses.
*   **EndDateTime**: Endzeitpunkt des Ereignisses.
*   **IsAllDay**: Gibt an, ob das Ereignis ganztägig ist (true oder false).
*   **Location**: Der neue Veranstaltungsort des Ereignisses.
*   **Body**: Die neue Beschreibung des Kalendereintrags.
*   **IsReminderOn**: Aktiviert oder deaktiviert Erinnerungen (true oder false).
*   **ReminderMinutesBeforeStart**: Zeit in Minuten vor dem Start des Ereignisses für die Erinnerung.
*   **Importance**: Die Wichtigkeit des Ereignisses. Mögliche Werte:
    *   low
    *   normal
    *   high
*   **Recurrence**: Die Wiederholung des Ereignisses. Mögliche Werte:
    *   none
    *   daily
    *   weekly
    *   monthly
*   **Attendees**: Eine kommagetrennte Liste der neuen Teilnehmer-E-Mail-Adressen.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Ignoriert auftretende Fehler, wenn auf true gesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventUpdate CalendarId="KalenderID123" EventId="EreignisID456" Subject="Projektupdate" StartDateTime="2024-01-10T13:00:00" EndDateTime="2024-01-10T14:00:00" Location="Besprechungsraum B" Body="Update zur Projektplanung" Attendees="teilnehmer3@example.com,teilnehmer4@example.com" Importance="normal" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Aktualisiert das Ereignis **EreignisID456** im Kalender **KalenderID123** mit neuem Betreff, Zeitrahmen, Teilnehmern und Veranstaltungsort.

Microsoft365CalendarEventDelete
-------------------------------

Löscht einen bestimmten Kalendereintrag aus einem Kalender.

```text-x-trilium-auto
<Microsoft365CalendarEventDelete CalendarId="" EventId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, aus dem das Ereignis gelöscht werden soll.
*   **EventId**: Die ID des zu löschenden Kalendereintrags.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Ignoriert auftretende Fehler, wenn auf true gesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventDelete CalendarId="KalenderID123" EventId="EreignisID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Kalendereintrag **EreignisID456** aus dem Kalender **KalenderID123**.

Microsoft365CalendarEventAttachmentList
---------------------------------------

Listet die Anhänge eines bestimmten Kalendereintrags auf und speichert sie in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentList Data="{@myData}" CalendarId="" EventId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Anhänge gespeichert wird.
*   **CalendarId**: Die ID des Kalenders, zu dem der Eintrag gehört.
*   **EventId**: Die ID des Kalendereintrags.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Ignoriert auftretende Fehler, wenn auf true gesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentList Data="{@myAttachments}" CalendarId="KalenderID123" EventId="EreignisID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Anhänge für das Ereignis **EreignisID456** im Kalender **KalenderID123** auf und speichert sie in **{@myAttachments}**.

Microsoft365CalendarEventAttachmentDelete
-----------------------------------------

Löscht einen bestimmten Anhang eines Kalendereintrags.

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDelete CalendarId="" EventId="" AttachmentId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, zu dem der Kalendereintrag gehört.
*   **EventId**: Die ID des Kalendereintrags, dessen Anhang gelöscht werden soll.
*   **AttachmentId**: Die ID des zu löschenden Anhangs.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDelete CalendarId="KalenderID123" EventId="EreignisID456" AttachmentId="AnhangID789" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Anhang mit der ID **AnhangID789** aus dem Kalendereintrag **EreignisID456** im Kalender **KalenderID123**.

Microsoft365CalendarEventAttachmentUpload
-----------------------------------------

Lädt eine Datei als Anhang zu einem Kalendereintrag hoch.

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentUpload CalendarId="" EventId="" Source="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, zu dem der Kalendereintrag gehört.
*   **EventId**: Die ID des Kalendereintrags, zu dem der Anhang hinzugefügt werden soll.
*   **Source**: Der Dateipfad zur hochzuladenden Datei.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentUpload CalendarId="KalenderID123" EventId="EreignisID456" Source="C:\Dokumente\Bericht.pdf" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** zu dem Kalendereintrag **EreignisID456** im Kalender **KalenderID123** hoch.

Microsoft365CalendarEventAttachmentDownload
-------------------------------------------

Lädt einen bestimmten Anhang eines Kalendereintrags herunter und speichert ihn im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDownload CalendarId="" EventId="" AttachmentId="" DestinationFolder="" AttachmentName="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, zu dem der Kalendereintrag gehört.
*   **EventId**: Die ID des Kalendereintrags, dessen Anhang heruntergeladen werden soll.
*   **AttachmentId**: Die ID des Anhangs, der heruntergeladen werden soll.
*   **DestinationFolder**: Der Zielordner, in dem der Anhang gespeichert wird.
*   **AttachmentName**: Der Name, unter dem der Anhang gespeichert wird.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDownload CalendarId="KalenderID123" EventId="EreignisID456" AttachmentId="AnhangID789" DestinationFolder="C:\Downloads" AttachmentName="Bericht.pdf" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt den Anhang **AnhangID789** herunter und speichert ihn als **Bericht.pdf** im Ordner **C:\\Downloads**.

Microsoft365CalendarEventAttachmentDownloadAll
----------------------------------------------

Lädt alle Anhänge eines Kalendereintrags herunter und speichert sie im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDownloadAll CalendarId="" EventId="" DestinationFolder="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **CalendarId**: Die ID des Kalenders, zu dem der Kalendereintrag gehört.
*   **EventId**: Die ID des Kalendereintrags, dessen Anhänge heruntergeladen werden sollen.
*   **DestinationFolder**: Der Zielordner, in dem die Anhänge gespeichert werden.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365CalendarEventAttachmentDownloadAll CalendarId="KalenderID123" EventId="EreignisID456" DestinationFolder="C:\Downloads" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt alle Anhänge des Kalendereintrags **EreignisID456** aus dem Kalender **KalenderID123** herunter und speichert sie im Ordner **C:\\Downloads**.