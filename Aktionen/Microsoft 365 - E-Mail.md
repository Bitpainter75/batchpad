# Microsoft 365 - E-Mail
Microsoft365MailFolderList
--------------------------

Ruft die Liste der E-Mail-Ordner eines Benutzers ab und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365MailFolderList Data="{@myData}" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Ergebnisdaten der E-Mail-Ordner gespeichert werden.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Ordner aufgerufen werden sollen.
*   **Account**: Gibt das zu verwendende Konto für die Abfrage an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailFolderList Data="{@myData}" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition=""  Variable="{@Result}" IgnoreError="false" />
```

Im obigen Beispiel wird die Liste der E-Mail-Ordner für den Benutzer **benutzer@example.com** abgerufen. Die Ergebnisdaten werden in der Variable **{@myData}** gespeichert. Das angegebene Konto **{@Account:MyAccount}** wird für die Authentifizierung verwendet. Da kein Wert für Condition gesetzt wurde, wird die Aktion immer ausgeführt.

Microsoft365MailList
--------------------

Listet die E-Mails in einem bestimmten Ordner eines Benutzers auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365MailList Data="{@myData}" FolderId="inbox" Filter="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die aufgelisteten E-Mails gespeichert werden.
*   **FolderId**: Die ID des Ordners, aus dem die E-Mails abgerufen werden sollen. Standardwert ist inbox.
*   **Filter**: Optionaler Filter zur Einschränkung der abgerufenen E-Mails.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen E-Mails abgerufen werden sollen.
*   **Account**: Gibt das zu verwendende Konto für die Abfrage an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailList Data="{@myEmails}" FolderId="inbox" Filter="isRead eq false" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Dieses Beispiel ruft alle ungelesenen E-Mails (**isRead eq false**) aus dem Posteingang für den Benutzer **benutzer@example.com** ab. Die Ergebnisse werden in der Variable **{@myEmails}** gespeichert.

Die möglichen Filter entsprechen den Filterkriterien der MSGraph API: [https://learn.microsoft.com/de-de/graph/filter-query-parameter](https://learn.microsoft.com/de-de/graph/filter-query-parameter)

Microsoft365MailRead
--------------------

Liest Details einer bestimmten E-Mail und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365MailRead MailId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die eindeutige ID der E-Mail, die gelesen werden soll.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen E-Mail gelesen werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Abfrage an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailRead MailId="AAMkAGIAAA=" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@EmailDetails}" IgnoreError="false" />
```

In diesem Beispiel wird die E-Mail mit der ID **AAMkAGIAAA=** für den Benutzer **benutzer@example.com** ausgelesen. Die E-Mail-Details werden in der Variable **{@EmailDetails}** gespeichert.

Microsoft365MailReadJson
------------------------

Liest die MSGraph Details einer bestimmten E-Mail als JSON und speichert sie in der angegebenen Variable.

```text-x-trilium-auto
<Microsoft365MailReadJson MailId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die eindeutige ID der E-Mail, deren Details im JSON-Format gelesen werden sollen.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen E-Mail gelesen werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Abfrage an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailReadJson MailId="AAMkAGIAAA=" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@EmailDetails}" IgnoreError="false" />
```

In diesem Beispiel wird die E-Mail mit der ID **AAMkAGIAAA=** für den Benutzer **benutzer@example.com** ausgelesen. Die E-Mail-Details werden in der Variable **{@EmailDetails}** gespeichert.

Microsoft365MailSend
--------------------

Sendet eine neue E-Mail-Nachricht mit optionalen Anhängen.

```text-x-trilium-auto
<Microsoft365MailSend Subject="" Body="" To="" Cc="" Bcc="" Attachment="" Importance="normal" RequestReadReceipt="false" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Subject**: Der Betreff der E-Mail.
*   **Body**: Der Inhalt der Nachricht. HTML ist möglich.
*   **To**: Eine kommagetrennte Liste der Empfängeradressen.
*   **Cc**: Eine kommagetrennte Liste der CC-Empfängeradressen.
*   **Bcc**: Eine kommagetrennte Liste der BCC-Empfängeradressen.
*   **Attachment**: Eine kommagetrennte Liste der Dateipfade für Anhänge.
*   **Importance**: Gibt die Wichtigkeit der Nachricht an. Mögliche Werte:
    *   low
    *   normal (Standard)
    *   high
*   **RequestReadReceipt**: Gibt an, ob eine Lesebestätigung angefordert wird.
*   **UserPrincipalName**: Die E-Mail-Adresse des Absenders.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailSend Subject="Projektupdate - Woche 3" Body="<h1>Statusbericht</h1>" To="empfaenger@example.com" Cc="cc1@example.com" Bcc="bcc1@example.com" Attachment="C:\Reports\status.pdf" Importance="high" RequestReadReceipt="true" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird eine E-Mail mit dem Betreff **Projektupdate - Woche 3** und einem HTML-Body gesendet. Die Nachricht enthält einen Anhang **C:\\Reports\\status.pdf** und wird als **high** markiert.

Microsoft365MailDelete
----------------------

Löscht eine bestimmte E-Mail anhand ihrer ID.

```text-x-trilium-auto
<Microsoft365MailDelete MailId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die eindeutige ID der E-Mail, die gelöscht werden soll.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen E-Mail gelöscht werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailDelete MailId="AAMkAGIAAA=" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Im Beispiel wird die E-Mail mit der ID **AAMkAGIAAA=** für den Benutzer **benutzer@example.com** gelöscht.

Microsoft365MailMove
--------------------

Verschiebt eine E-Mail in einen anderen Ordner.

```text-x-trilium-auto
<Microsoft365MailMove MailId="" DestinationFolderId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die ID der E-Mail, die verschoben werden soll.
*   **DestinationFolderId**: Die ID des Zielordners, in den die E-Mail verschoben werden soll.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen E-Mail verschoben wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailMove MailId="AAMkAGIAAA=" DestinationFolderId="Archiv" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Die E-Mail mit der ID **AAMkAGIAAA=** wird in den Ordner **Archiv** für den Benutzer **benutzer@example.com** verschoben.

Microsoft365MailAttachmentList
------------------------------

Listet alle Anhänge einer E-Mail auf und speichert die Ergebnisse in der angegebenen Daten-Tabelle.

```text-x-trilium-auto
<Microsoft365MailAttachmentList Data="{@myData}" MailId="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die ID der E-Mail, deren Anhänge aufgelistet werden sollen.
*   **Data**: Variable, in der die Anhänge gespeichert werden.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Anhänge abgerufen werden.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365AttachmentList MailId="AAMkAGIAAA=" Data="{@myAttachments}" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Hier werden die Anhänge der E-Mail mit der ID **AAMkAGIAAA=** für den Benutzer **benutzer@example.com** aufgelistet. Die Ergebnisse werden in **{@myAttachments}** gespeichert.

Microsoft365MailAttachmentDownload
----------------------------------

Lädt einen bestimmten Anhang einer E-Mail herunter und speichert ihn im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365MailAttachmentDownload MailId="" AttachmentId="" DestinationFolder="" AttachmentName="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die ID der E-Mail, zu der der Anhang gehört.
*   **AttachmentId**: Die ID des Anhangs, der heruntergeladen werden soll.
*   **DestinationFolder**: Der Zielordner, in dem der Anhang gespeichert wird.
*   **AttachmentName**: Der Name, unter dem der Anhang gespeichert wird.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Anhang heruntergeladen werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailAttachmentDownload MailId="AAMkAGIAAA=" AttachmentId="12345" DestinationFolder="C:\Downloads" AttachmentName="Report.pdf" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird der Anhang mit der ID **12345** aus der E-Mail **AAMkAGIAAA=** heruntergeladen und als **Report.pdf** im Ordner **C:\\Downloads** gespeichert.

Microsoft365MailAttachmentDownloadAll
-------------------------------------

Lädt alle Anhänge einer bestimmten E-Mail herunter und speichert sie im angegebenen Zielordner.

```text-x-trilium-auto
<Microsoft365MailAttachmentDownloadAll MailId="" DestinationFolder="" UserPrincipalName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **MailId**: Die ID der E-Mail, aus der alle Anhänge heruntergeladen werden sollen.
*   **DestinationFolder**: Der Zielordner, in dem die Anhänge gespeichert werden.
*   **UserPrincipalName**: Die E-Mail-Adresse des Benutzers, dessen Anhänge heruntergeladen werden sollen.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<Microsoft365MailAttachmentDownloadAll MailId="AAMkAGIAAA=" DestinationFolder="C:\Downloads" UserPrincipalName="benutzer@example.com" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel werden alle Anhänge aus der E-Mail **AAMkAGIAAA=** heruntergeladen und im Ordner **C:\\Downloads** gespeichert.