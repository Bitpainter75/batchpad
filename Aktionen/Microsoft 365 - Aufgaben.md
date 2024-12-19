# Microsoft 365 - Aufgaben
Microsoft365TaskFolderList
--------------------------

Listet die verfügbaren Aufgaben-Ordner eines Microsoft 365-Benutzers auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365TaskFolderList Data="{@myData}" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Aufgaben-Ordner gespeichert wird.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskFolderList Data="{@myFolders}" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Aufgaben-Ordner für den Benutzer **benutzer@example.com** und speichert sie in **{@myFolders}**.

Microsoft365TaskList
--------------------

Listet die Aufgaben aus einem bestimmten Aufgaben-Ordner auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365TaskList Data="{@myData}" ListId="" Filter="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Aufgaben gespeichert wird.
*   **ListId**: Die ID des Aufgaben-Ordners.
*   **Filter**: (Optional) Ein Filter zur Einschränkung der Aufgaben.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskList Data="{@myTasks}" ListId="ListeID123" Filter="status eq 'notStarted'" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Aufgaben aus dem Ordner **ListeID123**, die noch nicht gestartet wurden, und speichert sie in **{@myTasks}**.

Die möglichen Filter entsprechen den Filterkriterien der MSGraph API: [https://learn.microsoft.com/de-de/graph/filter-query-parameter](https://learn.microsoft.com/de-de/graph/filter-query-parameter)

Microsoft365TaskRead
--------------------

Liest die Details einer bestimmten Aufgabe und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365TaskRead ListId="" TaskId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners.
*   **TaskId**: Die ID der zu lesenden Aufgabe.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskRead ListId="ListeID123" TaskId="TaskID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest die Details der Aufgabe **TaskID456** aus dem Aufgaben-Ordner **ListeID123**.

Microsoft365TaskReadJson
------------------------

Liest die MSGraph Details einer bestimmten Aufgabe im JSON-Format und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365TaskReadJson ListId="" TaskId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners.
*   **TaskId**: Die ID der zu lesenden Aufgabe.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskReadJson ListId="ListeID123" TaskId="TaskID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest die Details im JSON-Format der Aufgabe **TaskID456** aus dem Aufgaben-Ordner **ListeID123**.

Microsoft365TaskCreate
----------------------

Erstellt eine neue Aufgabe in einem bestimmten Aufgaben-Ordner.

```text-x-trilium-auto
<Microsoft365TaskCreate ListId="" Title="" Body="" DueDateTime="" Status="notStarted" IsReminderOn="false" ReminderDateTime="" Importance="normal" Recurrence="daily" RecurrenceInterval="1" RecurrenceStartDateTime="" RecurrenceEndDateTime="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners.
*   **Title**: Der Titel der Aufgabe.
*   **Body**: Die Beschreibung der Aufgabe.
*   **DueDateTime**: Fälligkeitsdatum der Aufgabe
*   **Status**: Der Status der Aufgabe. Mögliche Werte:
    *   notStarted
    *   inProgress
    *   completed
    *   waitingOnOthers
    *   deferred
*   **IsReminderOn**: Gibt an, ob eine Erinnerung aktiviert ist (true oder false).
*   **ReminderDateTime**: Das Datum und die Uhrzeit für die Erinnerung
*   **Importance**: Die Wichtigkeit der Aufgabe. Mögliche Werte:
    *   low
    *   normal
    *   high
*   **Recurrence**: Gibt die Wiederholung an. Mögliche Werte:
    *   none
    *   daily
    *   weekly
    *   monthly
*   **RecurrenceInterval**: Das Intervall der Wiederholung (z. B. 1 für täglich, 7 für wöchentlich).
*   **RecurrenceStartDateTime**: Startdatum der Wiederholung.
*   **RecurrenceEndDateTime**: Enddatum der Wiederholung.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskCreate ListId="ListeID123" Title="Projektplan erstellen" Body="Erstellung des Projektplans bis Montag." DueDateTime="2024-01-10T17:00:00" Importance="high" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt eine neue Aufgabe mit dem Titel **Projektplan erstellen** und speichert sie im Ordner **ListeID123**.

Microsoft365TaskUpdate
----------------------

Aktualisiert die Details einer bestehenden Aufgabe in einem bestimmten Aufgaben-Ordner.

```text-x-trilium-auto
<Microsoft365TaskUpdate ListId="" TaskId="" Title="" Body="" DueDateTime="" Status="notStarted" IsReminderOn="false" ReminderDateTime="" Importance="normal" Recurrence="daily" RecurrenceInterval="1" RecurrenceStartDateTime="" RecurrenceEndDateTime="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

**Attribute:**

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der zu aktualisierenden Aufgabe.
*   **Title**: Der neue Titel der Aufgabe.
*   **Body**: Die neue Beschreibung der Aufgabe.
*   **DueDateTime** :Das neue Fälligkeitsdatum der Aufgabe
*   **Status**: Der neue Status der Aufgabe. Mögliche Werte:
    *   notStarted
    *   inProgress
    *   completed
    *   waitingOnOthers
    *   deferred
*   **IsReminderOn**: Gibt an, ob eine Erinnerung aktiviert ist (true oder false).
*   **ReminderDateTime**: Das Datum und die Uhrzeit für die Erinnerung
*   **Importance**: Die neue Wichtigkeit der Aufgabe. Mögliche Werte:
    *   low
    *   normal
    *   high
*   **Recurrence**: Gibt die Wiederholung der Aufgabe an. Mögliche Werte:
    *   none
    *   daily
    *   weekly
    *   monthly
*   **RecurrenceInterval**: Das Intervall der Wiederholung (z. B. 1 für täglich, 7 für wöchentlich).
*   **RecurrenceStartDateTime**: Startdatum der Wiederholung.
*   **RecurrenceEndDateTime**: Enddatum der Wiederholung.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Aufgabe aktualisiert werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

**Beispiel:**

```text-x-trilium-auto
<Microsoft365TaskUpdate ListId="ListeID123" TaskId="TaskID456" Title="Projektfinalisierung" Body="Abschluss der finalen Projektschritte." DueDateTime="2024-01-15T17:00:00" Status="inProgress" IsReminderOn="true" ReminderDateTime="2024-01-15T09:00:00" Importance="high" Recurrence="weekly" RecurrenceInterval="1" RecurrenceStartDateTime="2024-01-15T00:00:00" RecurrenceEndDateTime="2024-03-15T00:00:00" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

  
In diesem Beispiel wird die Aufgabe **TaskID456** im Ordner **ListeID123** aktualisiert:

*   Der Titel wird auf **Projektfinalisierung** geändert.
*   Die Beschreibung lautet **Abschluss der finalen Projektschritte**.
*   Die Fälligkeit wird auf **15\. Januar 2024, 17:00 Uhr** gesetzt.
*   Der Status wird zu **inProgress** geändert.
*   Eine Erinnerung ist aktiviert und wird für **9:00 Uhr am 15. Januar 2024** gesetzt.
*   Die Aufgabe wiederholt sich **wöchentlich** bis zum **15\. März 2024**. 

Microsoft365TaskDelete
----------------------

Löscht eine bestimmte Aufgabe aus einem Aufgaben-Ordner.

```text-x-trilium-auto
<Microsoft365TaskDelete ListId="" TaskId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners.
*   **TaskId**: Die ID der zu löschenden Aufgabe.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskDelete ListId="ListeID123" TaskId="TaskID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Aufgabe **TaskID456** aus dem Aufgaben-Ordner **ListeID123**.

Microsoft365TaskChecklistItemList
---------------------------------

Listet die Checklistenelemente einer bestimmten Aufgabe auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365TaskChecklistItemList Data="{@myData}" ListId="" TaskId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Checklistenelemente gespeichert wird.
*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, deren Checkliste aufgelistet werden soll.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskChecklistItemList Data="{@myChecklist}" ListId="ListeID123" TaskId="TaskID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Checklistenelemente der Aufgabe **TaskID456** im Aufgaben-Ordner **ListeID123** auf und speichert sie in der Variable **{@myChecklist}**.

Microsoft365TaskChecklistItemCreate
-----------------------------------

Erstellt ein neues Checklistenelement zu einer bestimmten Aufgabe.

```text-x-trilium-auto
<Microsoft365TaskChecklistItemCreate ListId="" TaskId="" ChecklistItemName="" IsChecked="false" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, zu der das Checklistenelement hinzugefügt wird.
*   **ChecklistItemName**: Der Name des neuen Checklistenelements.
*   **IsChecked**: Gibt an, ob das Element bereits abgehakt ist (true oder false).
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskChecklistItemCreate ListId="ListeID123" TaskId="TaskID456" ChecklistItemName="Dokumente prüfen" IsChecked="false" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Fügt das Checklistenelement **Dokumente prüfen** zur Aufgabe **TaskID456** im Aufgaben-Ordner **ListeID123** hinzu und markiert es als noch nicht erledigt.

Microsoft365TaskChecklistItemUpdate
-----------------------------------

Aktualisiert ein vorhandenes Checklistenelement einer Aufgabe.

```text-x-trilium-auto
<Microsoft365TaskChecklistItemUpdate ListId="" TaskId="" ChecklistItemId="" ChecklistItemName="" IsChecked="false" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners.
*   **TaskId**: Die ID der Aufgabe, zu der das Checklistenelement gehört.
*   **ChecklistItemId**: Die ID des zu aktualisierenden Checklistenelements.
*   **ChecklistItemName**: Der neue Name des Checklistenelements.
*   **IsChecked**: Gibt an, ob das Element abgehakt ist (true oder false).
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskChecklistItemUpdate ListId="ListeID123" TaskId="TaskID456" ChecklistItemId="ChecklistID789" ChecklistItemName="Dokumente final prüfen" IsChecked="true" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Aktualisiert das Checklistenelement **ChecklistID789**, ändert den Namen zu **Dokumente final prüfen** und markiert es als erledigt.

Microsoft365TaskChecklistItemDelete
-----------------------------------

Löscht ein Checklistenelement aus einer bestimmten Aufgabe.

```text-x-trilium-auto
<Microsoft365TaskChecklistItemDelete ListId="" TaskId="" ChecklistItemId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, aus der das Checklistenelement gelöscht wird.
*   **ChecklistItemId**: Die ID des zu löschenden Checklistenelements.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskChecklistItemDelete ListId="ListeID123" TaskId="TaskID456" ChecklistItemId="ChecklistID789" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht das Checklistenelement **ChecklistID789** aus der Aufgabe **TaskID456** im Aufgaben-Ordner **ListeID123**.

Microsoft365TaskAttachmentList
------------------------------

Listet die Anhänge einer bestimmten Aufgabe auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365TaskAttachmentList Data="{@myData}" ListId="" TaskId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Anhänge gespeichert wird.
*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, deren Anhänge aufgelistet werden sollen.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers,.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskAttachmentList Data="{@myAttachments}" ListId="ListeID123" TaskId="TaskID456" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel werden alle Anhänge der Aufgabe **TaskID456** im Aufgaben-Ordner **ListeID123** aufgelistet und in der Variable **{@myAttachments}** gespeichert.

Microsoft365TaskAttachmentDelete
--------------------------------

Löscht einen bestimmten Anhang von einer Aufgabe.

```text-x-trilium-auto
<Microsoft365TaskAttachmentDelete ListId="" TaskId="" AttachmentId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, von der der Anhang gelöscht wird.
*   **AttachmentId**: Die ID des zu löschenden Anhangs.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskAttachmentDelete ListId="ListeID123" TaskId="TaskID456" AttachmentId="AnhangID789" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Anhang mit der ID **AnhangID789** aus der Aufgabe **TaskID456** im Aufgaben-Ordner **ListeID12"**.

Microsoft365TaskAttachmentUpload
--------------------------------

Lädt eine Datei als Anhang zu einer bestimmten Aufgabe hoch.

```text-x-trilium-auto
<Microsoft365TaskAttachmentUpload ListId="" TaskId="" Source="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, zu der der Anhang hinzugefügt wird.
*   **Source**: Der Dateipfad der Datei, die hochgeladen werden soll.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskAttachmentUpload ListId="ListeID123" TaskId="TaskID456" Source="C:\Dokumente\Bericht.pdf" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** zu der Aufgabe **TaskID456** im Ordner **ListeID123** hoch.

Microsoft365TaskAttachmentDownload
----------------------------------

Lädt einen bestimmten Anhang einer Aufgabe herunter und speichert ihn im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365TaskAttachmentDownload ListId="" TaskId="" AttachmentId="" DestinationFolder="" AttachmentName="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, aus der der Anhang heruntergeladen wird.
*   **AttachmentId**: Die ID des herunterzuladenden Anhangs.
*   **DestinationFolder**: Der Pfad des Zielordners, in dem der Anhang gespeichert wird.
*   **AttachmentName**: Der Name, unter dem der Anhang gespeichert wird.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskAttachmentDownload ListId="ListeID123" TaskId="TaskID456" AttachmentId="AnhangID789" DestinationFolder="C:\Downloads" AttachmentName="Bericht.pdf" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt den Anhang **AnhangID789** aus der Aufgabe **TaskID456** herunter und speichert ihn als **Bericht.pdf** im Ordner **C:\\Downloads**.

Microsoft365TaskAttachmentDownloadAll
-------------------------------------

Lädt alle Anhänge einer Aufgabe herunter und speichert sie im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365TaskAttachmentDownloadAll ListId="" TaskId="" DestinationFolder="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ListId**: Die ID des Aufgaben-Ordners, zu dem die Aufgabe gehört.
*   **TaskId**: Die ID der Aufgabe, deren Anhänge heruntergeladen werden sollen.
*   **DestinationFolder**: Der Pfad des Zielordners, in dem die Anhänge gespeichert werden.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365TaskAttachmentDownloadAll ListId="ListeID123" TaskId="TaskID456" DestinationFolder="C:\Downloads" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt alle Anhänge der Aufgabe **TaskID456** herunter und speichert sie im Ordner **C:\\Downloads**.