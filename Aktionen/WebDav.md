# WebDav
WebDAVFileUpload
----------------

Die Aktion **WebDAVFileUpload** lädt eine angegebene Datei auf einen Pfad des WebDAV-Servers hoch.

```text-x-trilium-auto
<WebDAVFileUpload Source="" Destination="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der lokale Pfad zur Datei, die hochgeladen werden soll (inkl. Dateiname und Dateiendung).
*   **Destination**: Der Zielpfad auf dem WebDAV-Server, in den die Datei hochgeladen wird.
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVFileUpload Source="C:\Daten\Report.pdf" Destination="/Dokumente/Report.pdf" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Report.pdf** von **C:\\Daten** in den Pfad **/Dokumente/** des WebDAV-Servers hoch.

WebDAVFileDownload
------------------

Die Aktion **WebDAVFileDownload** lädt eine Datei von einem WebDAV-Server in ein lokales Zielverzeichnis herunter.

```text-x-trilium-auto
<WebDAVFileDownload Source="" Destination="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei auf dem WebDAV-Server.
*   **Destination**: Der lokale Pfad, in dem die Datei gespeichert wird (inkl. Dateiname und Dateiendung).
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVFileDownload Source="/Dokumente/Report.pdf" Destination="C:\Downloads\Report.pdf" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Report.pdf** aus dem Pfad **/Dokumente/** herunter und speichert sie in **C:\\Downloads**.

WebDAVFileDelete
----------------

Die Aktion **WebDAVFileDelete** löscht eine angegebene Datei von einem WebDAV-Server.

```text-x-trilium-auto
<WebDAVFileDelete Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei auf dem WebDAV-Server, die gelöscht werden soll.
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVFileDelete Source="/Dokumente/Report.pdf" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Datei **Report.pdf** aus dem Pfad **/Dokumente/** auf dem WebDAV-Server.

WebDAVPathCreate
----------------

Die Aktion **WebDAVPathCreate** erstellt einen Ordner auf einem WebDAV-Server für den angegebenen Pfad.

```text-x-trilium-auto
<WebDAVPathCreate Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad des neuen Ordners, der erstellt werden soll.
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVPathCreate Source="/Dokumente/NeuerOrdner" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt den Ordner **NeuerOrdner** im Pfad **/Dokumente/** auf dem WebDAV-Server.

WebDAVPathOrFileExists
----------------------

Die Aktion **WebDAVPathOrFileExists** prüft, ob ein Pfad oder eine Datei auf einem WebDAV-Server existiert.

```text-x-trilium-auto
<WebDAVPathOrFileExists Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad oder die Datei auf dem WebDAV-Server, die geprüft werden soll.
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in der das Ergebnis der Prüfung gespeichert wird (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVPathOrFileExists Source="/Dokumente/Report.pdf" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Datei **Report.pdf** im Pfad **/Dokumente/** auf dem WebDAV-Server existiert.

WebDAVListDirectory
-------------------

Die Aktion **WebDAVListDirectory** listet alle Dateien und Verzeichnisse in einem angegebenen Pfad auf und speichert das Ergebnis als Daten-Tabelle.

```text-x-trilium-auto
<WebDAVListDirectory Data="" DataCount="" Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Dateien und Verzeichnisse gespeichert wird.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Einträge gespeichert wird.
*   **Source**: Der Pfad des zu durchsuchenden Ordners auf dem WebDAV-Server.
*   **Username**: Der Benutzername für den Zugriff auf den WebDAV-Server.
*   **Password**: Das Passwort für den Zugriff auf den WebDAV-Server.
*   **Hostname**: Die URL oder der Hostname des WebDAV-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WebDAVListDirectory Data="{@myList}" DataCount="{@ResultCount}" Source="/Dokumente" Username="admin" Password="Passwort123" Hostname="https://webdav.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Dateien und Verzeichnisse im Pfad **/Dokumente** auf, speichert die Inhalte in **{@myList}** und die Anzahl der Einträge in **{@ResultCount}**.