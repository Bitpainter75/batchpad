# S3 Object Storage
S3FileUpload
------------

Die Aktion **S3FileUpload** lädt eine Datei von einem lokalen Pfad in einen S3-Bucket hoch.

```text-x-trilium-auto
<S3FileUpload Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der lokale Pfad der Datei, die hochgeladen werden soll (inkl. Dateiname und Dateiendung).
*   **Destination**: Der Zielpfad im S3-Bucket, in den die Datei hochgeladen wird.
*   **Account**: Gibt das zu verwendende S3-Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<S3FileUpload Source="C:\Daten\Bericht.pdf" Destination="my-bucket/Dokumente/Bericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** von **C:\\Daten** in den S3-Pfad **my-bucket/Dokumente/** hoch.

S3FileDownload
--------------

Die Aktion **S3FileDownload** lädt eine Datei aus einem S3-Bucket herunter und speichert sie lokal.

```text-x-trilium-auto
<S3FileDownload Source="" Destination="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei im S3-Bucket, die heruntergeladen werden soll.
*   **Destination**: Der lokale Pfad, in dem die Datei gespeichert wird (inkl. Dateiname und Dateiendung).
*   **Account**: Gibt das zu verwendende S3-Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<S3FileDownload Source="Dokumente/Bericht.pdf" Destination="C:\Downloads\Bericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** aus dem S3-Pfad **Dokumente/** herunter und speichert sie lokal in **C:\\Downloads**.

S3FileDelete
------------

Die Aktion **S3FileDelete** löscht eine Datei aus einem S3-Bucket.

```text-x-trilium-auto
<S3FileDelete Source="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei im S3-Bucket, die gelöscht werden soll.
*   **Account**: Gibt das zu verwendende S3-Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<S3FileDelete Source="Dokumente/Bericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Datei **Bericht.pdf** aus dem S3-Pfad **Dokumente/**.

S3PathOrFileExists
------------------

Die Aktion **S3PathOrFileExists** prüft, ob ein Pfad oder eine Datei in einem S3-Bucket existiert.

```text-x-trilium-auto
<S3PathOrFileExists Source="" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner im S3-Bucket, der geprüft werden soll.
*   **Account**: Gibt das zu verwendende S3-Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in der gespeichert wird, ob die Datei oder der Ordner gefunden wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<S3PathOrFileExists Source="Dokumente/Bericht.pdf" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Datei **Bericht.pdf** im S3-Pfad **Dokumente/** existiert.

S3ListDirectory
---------------

Die Aktion **S3ListDirectory** listet alle Dateien und Ordner aus einem angegebenen S3-Pfad auf und speichert die Ergebnisse als Daten-Tabelle.

```text-x-trilium-auto
<S3ListDirectory Data="{@myData}" DataCount="{@ResultCount}" Source="" Version="1" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Dateien und Ordner gespeichert wird.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Dateien und Ordner gespeichert wird.
*   **Source**: Der Pfad des zu durchsuchenden Ordners im S3-Bucket.
*   **Version:** (Optional) Gibt an, welche API-Version verwendet wird. Standardwert ist 1.
*   **Account**: Gibt das zu verwendende S3-Konto für die Aktion an.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<S3ListDirectory Data="{@myFiles}" DataCount="{@ResultCount}" Source="Dokumente" Version="1" Account="{@Account:MyAccount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Dateien und Ordner im S3-Pfad **Dokumente** auf, speichert die Inhalte in **{@myFiles}** und die Anzahl der Einträge in **{@ResultCount}**.