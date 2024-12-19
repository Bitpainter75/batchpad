# Dateien
FileCopy
--------

Die Aktion **FileCopy** kopiert eine angegebene Datei (Attribut: Source) zu dem angegebenen Ziel (Attribut: Destination). Mit dem Attribut Overwrite kann bestimmt werden, ob eine bereits existierende Datei überschrieben werden soll.

```text-x-trilium-auto
<FileCopy Source="" Destination="" Overwrite="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileMove
--------

Die Aktion **FileMove** verschiebt eine angegebene Datei (Attribut: Source) in das angegebene Ziel (Attribut: Destination).

```text-x-trilium-auto
<FileMove Source="" Destination="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileRename
----------

Die Aktion **FileRename** verändert den Pfad, Dateinamen und Dateiendung einer angegebenen Datei (Attribut: Source) und weist der Datei einen neuen Pfad, Dateinamen und Dateiendung zu (Attribut: Destination).

```text-x-trilium-auto
<FileRename Source="" Destination="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileDelete
----------

Die Aktion **FileDelete** löscht eine angegebene Datei (Attribut: File).

```text-x-trilium-auto
<FileDelete File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileExists
----------

Die Aktion **FileExists** prüft, ob eine angegebene Datei (Attribut: File) existiert. Falls Ja wird in das Attribut Variable true zurückgegeben 

```text-x-trilium-auto
<FileExists File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileCreateSymbolicLink
----------------------

Die Aktion **FileCreateSymbolicLink** erstellt eine symbolische Verknüpfung zu einer Datei innerhalb des Dateisystems.

```text-x-trilium-auto
<FileCreateSymbolicLink Source="" Destination="" Variable="{@Result}" />
```

FileGetCreationTime
-------------------

Die Aktion **FileGetCreationTime** ermittelt zu einer angegebenen Datei (Attribut: File) das Erstellungsdatum liefert das Ergebnis in das Attribut Variable zurück.

```text-x-trilium-auto
<FileGetCreationTime File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileSetCreationTime
-------------------

Mit der Aktion **FileSetCreationTime** versieht das Erstellungsdatum einer angegebenen Datei (Attribut: File) mit einem neuen Zeitstempel (Attribut: Value).

```text-x-trilium-auto
<FileSetCreationTime File="" Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileIsReadOnly
--------------

Die Aktion **FileIsReadOnly** prüft, ob die angegebene Datei (Attribut: File) schreibgeschützt ist.

```text-x-trilium-auto
<FileIsReadOnly File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileSetReadOnly
---------------

Die Aktion **FileSetReadOnly** versieht die angegebene Datei (Attribut: File) mit einem Schreibschutz.

```text-x-trilium-auto
<FileSetReadOnly File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileSetWriteable
----------------

Die Aktion **FileSetWriteable** entfernt den Schreibschutz der angegebenen Datei (Attribut: File).

```text-x-trilium-auto
<FileSetWriteable File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileVersion
-----------

Die Aktion **FileVersion** ermittelt zu einer angegebenen Datei (Attribut: File) die Dateiversion. Ist das Attribut ProductVersion auf True gesetzt, wird die Produktversion der Datei in das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<FileVersion File="" ProductVersion="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

GetFileName
-----------

Die Aktion **GetFileName** gibt den Dateinamen inkl. der Dateiendung der angegebenen Datei (Attribut: Source) in das Attribut Variable zurück.

```text-x-trilium-auto
<GetFileName Source="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

GetFileNameWithoutExtension
---------------------------

Die Aktion **GetFileNameWithoutExtension** gibt den Dateinamen ohne die Dateiendung der angegebenen Datei (Attribut: Source) in das Attribut Variable zurück.

```text-x-trilium-auto
<GetFileNameWithoutExtension Source="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

GetExtension
------------

Die Aktion **GetExtension** gibt die Dateiendung der angegebenen Datei (Attribut: Source) in das Attribut Variable zurück. Hinweis: Die Dateiendung wird mit dem Trennzeichen "." übernommen z.B. ".pdf".

```text-x-trilium-auto
<GetExtension Source="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileListDirectory
-----------------

Die Aktion **FileListDirectory** erstellt eine Daten-Tabelle, das Dateien und Ordner enthält, die unter dem angegebenen Pfad (Attribut: Source) verfügbar sind. Dabei kann angegeben werden werden ob nur Dateien (Attribut: OnlyFiles) oder nur Ordner (Attribut: OnlyDirectories) in das DataTable Objekt übernommen werden. Zusätzliche Informationen können über das Attribut WithInformations angefordert werden. Die Informationen, die eine Daten-Tabelle zur Laufzeit hält, können über den Inspektor eingesehen werden (Hauptartikel: Inspektor & Debugging). Dieses Objekt kann dazu verwendet werden, um in einer ForEach Schleife über die Einträge der Daten-Tabelle zu iterieren. Siehe Beispiel: Datensicherung.

```text-x-trilium-auto
<FileListDirectory Source="" Data="{@myData}" OnlyFiles="false" OnlyDirectories="false" WithInformations="false" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

CreateShortcut
--------------

Die Aktion **CreateShortcut** erstellt eine Dateiverknüpfung zu der angegebenen Datei (Attribut: Source) unter einem angegebenen Zielpfad (Attribut: Destination). Der Name und das Icon der Dateiverknüpfung werden über die gleichnamigen Attribute gesetzt. Argumente, die dem Aufruf des Shortcuts angehangen werden sollen, werden über das Attribut Arguments angegeben. Über das Attribut Workpath kann angegeben werden in welchem Verzeichnis die Dateiverknüpfung ausgeführt wird.

```text-x-trilium-auto
<CreateShortcut Source="" Destination="" Name="" Icon="" Workpath="" Arguments="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Zip
---

Die Aktion **Zip** packt eine angegebene Datei/Verzeichnis (Attribut: Source) in ein Zip-Archiv (Attribut: Destination). 

```text-x-trilium-auto
<Zip Source="" Destination="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Unzip
-----

Die Aktion **UnZip** entpackt ein angegebenes Zip-Archiv (Attribut: Source) in ein Zielverzeichnis (Attribut: Destination).

```text-x-trilium-auto
<UnZip Source="" Destination="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileMirror
----------

Die Aktion **FileMirror** kopiert Dateien von einer Quelle (Attribut: Source) in ein Zielverzeichnis (Attribut: Destination). Über das Attribut Message wird ein Bericht des Kopiervorgangs zurückgegeben. Verzeichnisse und Dateien, die ausgeschlossen werden sollen, können über die Attribute ExludeFiles und ExcludeDirectories angegeben werden. Mehrere Verzeichnisse bzw. Dateien werden dabei mit einem Semikolon getrennt. Zudem kann eine Wildcard (\*) verwendet werden (siehe Beispiel).

```text-x-trilium-auto
<FileMirror Source="" Destination="" ExcludeFiles="" ExcludeDirectories="" Message="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

  
Beispiel:

```text-x-trilium-auto
<Batch>
    <FileMirror Source="\\...\Software" Destination="D:\Software" ExcludeFiles=".windows*;AlbumArt*;Thumbs.db" ExcludeDirectories=".*" Message="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
    <Print Text="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
</Batch>
```