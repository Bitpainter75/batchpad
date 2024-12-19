# OneDrive & Sharepoint
OneDriveFileUpload
------------------

Lädt eine Datei von einem lokalen Pfad zu einem Zielordner auf OneDrive oder SharePoint hoch.

```text-x-trilium-auto
<OneDriveFileUpload Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der lokale Pfad der Datei, die hochgeladen werden soll.
*   **Destination**: Der Zielpfad auf OneDrive oder SharePoint, in den die Datei hochgeladen wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveFileUpload Source="C:\Berichte\Jahresbericht.pdf" Destination="/Dokumente/Berichte/Jahresbericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Jahresbericht.pdf** von **C:\\Berichte** in den OneDrive-Ordner **/Dokumente/Berichte/** hoch.

OneDriveFileDownload
--------------------

Lädt eine Datei von OneDrive oder SharePoint herunter und speichert sie im angegebenen lokalen Zielordner.

```text-x-trilium-auto
<OneDriveFileDownload Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei auf OneDrive oder SharePoint.
*   **Destination**: Der lokale Pfad, in dem die Datei gespeichert wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveFileDownload Source="/Dokumente/Berichte/Jahresbericht.pdf" Destination="C:\Downloads\Jahresbericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Jahresbericht.pdf** von OneDrive aus dem Pfad **/Dokumente/Berichte/** herunter und speichert sie lokal in **C:\\Downloads**.

OneDrivePathCreate
------------------

Erstellt einen neuen Ordner auf OneDrive oder SharePoint.

```text-x-trilium-auto
<OneDrivePathCreate Path="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Path**: Der Pfad des neuen Ordners, der erstellt werden soll.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDrivePathCreate Path="/Dokumente/Projekte/2024" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt einen neuen Ordner **2024** im Pfad **/Dokumente/Projekte/**.

OneDriveItemCopy
----------------

Kopiert eine Datei oder einen Ordner zu einem neuen Pfad auf OneDrive oder SharePoint.

```text-x-trilium-auto
<OneDriveItemCopy Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der kopiert werden soll.
*   **Destination**: Der Zielpfad, in den die Kopie erstellt wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemCopy Source="/Dokumente/Projektplan.xlsx" Destination="/Backups/Projektplan_Kopie.xlsx" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Kopiert die Datei **Projektplan.xlsx** in den Ordner **/Backups/** und benennt sie als **Projektplan\_Kopie.xlsx**.

OneDriveItemMove
----------------

Verschiebt eine Datei oder einen Ordner zu einem neuen Pfad auf OneDrive oder SharePoint.

```text-x-trilium-auto
<OneDriveItemMove Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der verschoben werden soll.
*   **Destination**: Der Zielpfad, in den verschoben wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemMove Source="/Dokumente/Entwurf.docx" Destination="/Projekte/Final/Entwurf.docx" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Verschiebt die Datei **Entwurf.docx** von **/Dokumente/** nach **/Projekte/Final/**.

OneDriveItemRename
------------------

Benennt eine Datei oder einen Ordner auf OneDrive oder SharePoint um.

```text-x-trilium-auto
<OneDriveItemRename Source="" NewName="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der umbenannt werden soll.
*   **NewName**: Der neue Name für die Datei oder den Ordner.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemRename Source="/Dokumente/Entwurf.docx" NewName="Finaler_Entwurf.docx" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Benennt die Datei **Entwurf.docx** in **Finaler\_Entwurf.docx** um.

OneDriveItemDelete
------------------

Löscht eine Datei oder einen Ordner auf OneDrive oder SharePoint.

```text-x-trilium-auto
<OneDriveItemDelete Source="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der zu löschen ist.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemDelete Source="/Dokumente/AlteBerichte" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Ordner **AlteBerichte** inklusive aller Inhalte.

OneDriveItemExists
------------------

Prüft, ob eine Datei oder ein Ordner auf OneDrive oder SharePoint existiert.

```text-x-trilium-auto
<OneDriveItemExists Source="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der zu löschen ist.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemExists Source="/Dokumente/Projektplan.xlsx" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Datei **Projektplan.xlsx** existiert. Und liefert in der Variablen **{@Result}** den Wert **true** wenn die Datei vorhanden ist.

OneDriveItemShareCreate
-----------------------

Erstellt eine Freigabe für eine Datei oder einen Ordner auf OneDrive oder SharePoint und stellt die Freigabe für die angegebenen E-Mail-Adressen bereit.

```text-x-trilium-auto
<OneDriveItemShareCreate Source="" Account="{@Account:MyAccount}" Recipients="" ReadWrite="false" ExpireDate="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner auf OneDrive oder SharePoint, für die die Freigabe erstellt werden soll.
*   **Recipients:** Eine kommagetrennte Liste von E-Mail-Adressen, an die die Freigabe gesendet wird.
*   **ReadWrite:** Gibt an, ob die Freigabe schreibgeschützt oder mit Bearbeitungsrechten erfolgt:
    *   false (Standard): Schreibgeschützt.
    *   true: Mit Bearbeitungsrechten.
*   **ExpireDate**: (Optional) Ablaufdatum der Freigabe. Nach Ablauf ist der Zugriff nicht mehr möglich.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveItemShareCreate Source="/Dokumente/Projektplan.xlsx" Recipients="max.mustermann@example.com,anna.schmidt@example.com" ReadWrite="true" ExpireDate="2024-01-31" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Datei **Projektplan.xlsx** freigegeben:

*   Die Freigabe wird an die Empfänger **max.mustermann@example.com** und **anna.schmidt@example.com** gesendet.
*   Die Freigabe erlaubt Bearbeitungsrechte (**ReadWrite="true"**).
*   Die Freigabe läuft am **31\. Januar 2024** ab.

OneDriveListDirectory
---------------------

Listet die Inhalte eines Ordners auf OneDrive oder SharePoint auf und speichert die Ergebnisse in einer Daten-Tabelle.

```text-x-trilium-auto
<OneDriveListDirectory Data="{@myData}" Path="" Account="{@Account:MyAccount}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Inhalte gespeichert wird.
*   **Path**: Der Pfad des zu durchsuchenden Ordners.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Elemente gespeichert wird.
*   **Account**: Gibt das zu verwendende Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<OneDriveListDirectory Data="{@myFiles}" Path="/Dokumente" Account="{@Account:MyAccount}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Dateien und Ordner im Pfad **/Dokumente** auf, speichert die Inhalte in {@myFiles} und die Anzahl in {@ResultCount}.