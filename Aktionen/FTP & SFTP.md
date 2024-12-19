# FTP & SFTP
FTPFileUpload
-------------

Die Aktion **FTPFileUpload** lädt die angegebene Datei (Attribut: Source) in ein angegebenes Verzeichnis (Attribut: Destination) des FTP-Servers hoch.

```text-x-trilium-auto
<FTPFileUpload Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPFileDownload
---------------

Die Aktion **FTPFileDownload** lädt die angegebene Datei (Attribut: Source) von einem FTP-Server in ein lokales Zielverzeichnis (Attribut: Destination) herunter.

```text-x-trilium-auto
<FTPFileDownload Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPDirectoryUpload
------------------

Die Aktion **FTPDirectoryUpload** lädt das angegebene Verzeichnis (Attribut: Source) samt der darin enthaltenen Dateien in das angegebene Verzeichnis (Attribut: Destination) des FTP-Servers hoch.

```text-x-trilium-auto
<FTPDirectoryUpload Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Overwrite="false" Mirror="false" Variable="{@Result}" />
```

FTPDirectoryDownload
--------------------

Die Aktion **FTPDirectoryDownload** lädt das angegebene Verzeichnis (Attribut: Source) samt der darin enthaltenen Dateien von einem FTP-Server in ein lokales Zielverzeichnis (Attribut: Destination) herunter.

```text-x-trilium-auto
<FTPDirectoryDownload Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Overwrite="false" Mirror="false" Variable="{@Result}" />
```

FTPFileRename
-------------

Die Aktion **FTPFileRename** ändert den Namen einer Datei auf einem FTP-Server. Über das Attribut Source wird der Pfad inkl. dem alten Dateinamen und Dateiendung angegeben. Über das Attribut Destination wird der Pfad und der neue Dateiname inkl. Dateiendung angegeben.

```text-x-trilium-auto
<FTPFileRename Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPFileDelete
-------------

Die Aktion **FTPFileDelete** löscht die angegebene Datei (Attribut: Source) auf dem FTP-Server.

```text-x-trilium-auto
<FTPFileDelete Source="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPFileExists
-------------

Die Aktion **FTPFileExists** prüft, ob die angegebene Datei (Attribut: Source) auf dem FTP-Server existiert.

```text-x-trilium-auto
<FTPFileExists Source="" File="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPPathCreate
-------------

Die Aktion **FTPPathCreate** erstellt ein Verzeichnis für den in dem Attribut Destination angegebenen Pfad auf dem FTP-Server.

```text-x-trilium-auto
<FTPPathCreate Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPPathRename
-------------

Die Aktion **FTPPathRename** ändert den Namen des angegebenen Verzeichnis (Attribut: Source) in den angegebenen Zielpfad (Attribut: Destination)

```text-x-trilium-auto
<FTPPathRename Source="" Destination="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPPathDelete
-------------

Die Aktion **FTPPathDelete** löscht das angegebene Verzeichnis (Attribut: Source) auf dem FTP-Server.

```text-x-trilium-auto
<FTPPathDelete Source="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPPathExists
-------------

Die Aktion **FTPPathExists** prüft, ob das angegebene Verzeichnis (Attribut: Source) auf dem FTP-Server existiert.

```text-x-trilium-auto
<FTPPathExists Source="" Host="" User="" Password="" SSL="Tls12" Passiv="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

FTPListDirectory
----------------

Die Aktion **FTPListDirectory** listet alle Dateien und Verzeichnisse aus dem angegebenen Pfad auf (Attribut: Source) und gibt das Ergebnis als DataTable Objekt über das Attribut Data zurück. Über das DataTable Objekt kann anschließend mit einer ForEach Schleife iteriert werden (Siehe Dokumentation Allgemein/ForEach). Zusätzlich wird über das Attribut DataCount die Anzahl der gefundenen Dateien und Verzeichnisse zurückgegeben.

```text-x-trilium-auto
<FTPListDirectory Data="{@myData}" Source="" Host="" User="" Password="" SSL="Tls12" Passiv="true" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPFileUpload
--------------

Die Aktion **SFTPFileUpload** lädt die angegebene Datei (Attribut: Source) auf einen angegebenen Pfad (Attribut: Destination) des SFTP-Servers.

```text-x-trilium-auto
<SFTPFileUpload Source="" Destination="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPFileDownload
----------------

Die Aktion **SFTPFileDownload** lädt die angegebene Datei (Attribut: Source) von einem SFTP-Server auf ein lokales Zielverzeichnis (Attribut: Destination).

```text-x-trilium-auto
<SFTPFileDownload Source="" Destination="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPFileRename
--------------

Die Aktion **SFTPFileRename** ändert den Namen einer Datei auf einem SFTP-Server. Über das Attribut Source wird der Pfad inkl. dem alten Dateinamen und Dateiendung angegeben. Über das Attribut Destination wird der Pfad und der neue Dateiname inkl. Dateiendung angegeben.

```text-x-trilium-auto
<SFTPFileRename Source="" Destination="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPFileDelete
--------------

Die Aktion **SFTPFileDelete** löscht die angegebene Datei (Attribut: Source) auf dem SFTP-Server.

```text-x-trilium-auto
<SFTPFileDelete Source="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPFileExists
--------------

Die Aktion **SFTPFileExists** prüft, ob die angegebene Datei (Attribut: Source) auf dem SFTP-Server existiert.

```text-x-trilium-auto
<SFTPFileExists Source="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPPathCreate
--------------

Die Aktion **SFTPPathCreate** erstellt ein Verzeichnis für den in dem Attribut Destination angegebenen Pfad auf dem SFTP-Server.

```text-x-trilium-auto
<SFTPPathCreate Destination="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPPathRename
--------------

Die Aktion **SFTPPathRename** ändert den Namen des angegebenen Verzeichnis (Attribut: Source) in den angegebenen Zielpfad (Attribut: Destination)

```text-x-trilium-auto
<SFTPPathRename Source="" Destination="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPPathDelete
--------------

Die Aktion **SFTPPathDelete** löscht das angegebene Verzeichnis (Attribut: Source) auf dem SFTP-Server.

```text-x-trilium-auto
<SFTPPathDelete Source="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SFTPPathExists
--------------

Die Aktion **SFTPPathExists** prüft, ob das angegebene Verzeichnis (Attribut: Source) auf dem SFTP-Server existiert.

```text-x-trilium-auto
<SFTPPathExists Source="" Servername="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
 
```

SFTPListDirectory
-----------------

Die Aktion **SFTPListDirectory** listet alle Dateien und Verzeichnisse aus dem angegebenen Pfad auf (Attribut: Source) und gibt das Ergebnis als Daten-Tabelle über das Attribut Data zurück. Über das DataTable Objekt kann anschließend mit einer ForEach Schleife iteriert werden (Siehe Dokumentation Allgemein/ForEach). Zusätzlich wird über das Attribut DataCount die Anzahl der gefundenen Dateien und Verzeichnisse zurückgegeben.

```text-x-trilium-auto
<SFTPListDirectory Data="{@myData}" Source="" Servername="" User="" Password="" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```