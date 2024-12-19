# Azure Storage
AzureFileUpload
---------------

Die Aktion **AzureFileUpload** führt einen Datei-Upload in den Microsoft Azure Blob-Speicher durch.

```text-x-trilium-auto
<AzureFileUpload Source="" Destination="" Account="" Key="" Container="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der lokale Pfad zur Datei, die hochgeladen werden soll (inkl. Dateiname und Dateiendung).
*   **Destination**: Der Zielpfad im Azure-Blob-Speicher, in den die Datei hochgeladen wird (inkl. Dateiname und Dateiendung).
*   **Account**: Der Name des Azure Storage-Accounts.
*   **Key**: Der Zugriffsschlüssel für den Azure Storage-Account.
*   **Container**: Der Name des Containers, in den die Datei hochgeladen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<AzureFileUpload Source="C:\Daten\Report.pdf" Destination="Berichte/Report.pdf" Account="myazureaccount" Key="abcdef1234567890" Container="dokumente" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Report.pdf** von **C:\\Daten** in den Container **dokumente** unter dem Pfad **Berichte/** hoch.

AzureFileDownload
-----------------

Die Aktion **AzureFileDownload** lädt eine Datei aus dem Azure Blob-Speicher in ein lokales Zielverzeichnis herunter.

```text-x-trilium-auto
<AzureFileDownload Source="" Destination="" Account="" Key="" Container="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei im Azure Blob-Speicher.
*   **Destination**: Der lokale Pfad, in dem die Datei gespeichert wird (inkl. Dateiname und Dateiendung).
*   **Account**: Der Name des Azure Storage-Accounts.
*   **Key**: Der Zugriffsschlüssel für den Azure Storage-Account.
*   **Container**: Der Name des Containers, in den die Datei hochgeladen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<AzureFileDownload Source="Berichte/Report.pdf" Destination="C:\Downloads\Report.pdf" Account="myazureaccount" Key="abcdef1234567890" Container="dokumente" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Report.pdf** aus dem Pfad **Berichte/** im Container **dokumente** herunter und speichert sie in **C:\\Downloads**.

AzureFileDelete
---------------

Die Aktion **AzureFileDelete** löscht eine Datei aus dem Azure Blob-Speicher.

```text-x-trilium-auto
<AzureFileDelete Source="" Account="" Key="" Container="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei im Azure Blob-Speicher, die gelöscht werden soll.
*   **Account**: Der Name des Azure Storage-Accounts.
*   **Key**: Der Zugriffsschlüssel für den Azure Storage-Account.
*   **Container**: Der Name des Containers, in den die Datei hochgeladen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<AzureFileDelete Source="Berichte/Report.pdf" Account="myazureaccount" Key="abcdef1234567890" Container="dokumente" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Datei **Report.pdf** aus dem Pfad **Berichte/** im Container **dokumente**.

AzurePathOrFileExists
---------------------

Die Aktion **AzurePathOrFileExists** prüft, ob ein Pfad oder eine Datei im Azure Blob-Speicher existiert.

```text-x-trilium-auto
<AzurePathOrFileExists Source="" Account="" Key="" Container="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Verzeichnis im Azure Blob-Speicher.
*   **Account**: Der Name des Azure Storage-Accounts.
*   **Key**: Der Zugriffsschlüssel für den Azure Storage-Account.
*   **Container**: Der Name des Containers, in den die Datei hochgeladen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in der das Ergebnis der Prüfung gespeichert wird (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<AzurePathOrFileExists Source="Berichte/Report.pdf" Account="myazureaccount" Key="abcdef1234567890" Container="dokumente" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Datei **Report.pdf** im Pfad **Berichte/** im Container **dokumente** existiert.

AzureListDirectory
------------------

Die Aktion **AzureListDirectory** listet alle Dateien und Verzeichnisse in einem Azure Blob-Speicher-Container auf und speichert das Ergebnis als Daten-Tabelle.

```text-x-trilium-auto
<AzureListDirectory Data="{@myData}" DataCount="{@ResultCount}" Account="" Key="" Container="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Dateien und Verzeichnisse gespeichert wird.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Dateien und Verzeichnisse gespeichert wird.
*   **Account**: Der Name des Azure Storage-Accounts.
*   **Key**: Der Zugriffsschlüssel für den Azure Storage-Account.
*   **Container**: Der Name des Containers, in den die Datei hochgeladen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<AzureListDirectory Data="{@myList}" DataCount="{@ResultCount}" Account="myazureaccount" Key="abcdef1234567890" Container="dokumente" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Dateien und Verzeichnisse im Container **dokumente** auf, speichert die Ergebnisse in **{@myList}** und die Anzahl der Einträge in **{@ResultCount}**.