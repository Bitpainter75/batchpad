# Verzeichnisse
PathCreate
----------

Die Aktion **PathCreate** erstellt den angegebenen Pfad (Attribut Path).

```text-x-trilium-auto
<PathCreate Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

PathRename
----------

Die Aktion **PathRename** benennt das Verzeichnis des angegebenen Pfads (Attribut: Path) in den angegebenen Namen (Attribut: NewName) um. Dabei muss für das Attribut Path der vollständige Pfad angegeben werden und für das Attribut NewName nur der neue Name des Verzeichnisses.

```text-x-trilium-auto
<PathRename Path="" NewName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

PathDelete
----------

Die Aktion **PathDelete** löscht das angegebene Verzeichnis (Attribut: Path).

```text-xml
<PathDelete Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

PathExists
----------

Die Aktion **PathExists** prüft ob das Verzeichnis unter dem angegebenen Pfad existiert (Attribut: Path). Ist das Verzeichnis vorhanden wird über das Attribut Variable true ausgegeben.

```text-x-trilium-auto
<PathExists Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

PathCreateSymbolicLink
----------------------

Die Aktion **PathCreateSymbolicLink** erstellt eine symbolische Verknüpfung auf ein Verzeichnis innerhalb des Dateisystems.

```text-x-trilium-auto
<PathCreateSymbolicLink Source="" Destination="" Variable="{@Result}" />
```

GetDirectoryName
----------------

Die Aktion **GetDirectoryName** schneidet alles nach dem letzten Backslash (inkl. des letzten Backslashs) in dem angegeben Pfad (Attribut: Source) ab. Das Ergebnis wird über das Attribut Variable ausgegeben.

```text-x-trilium-auto
<GetDirectoryName Source="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Parameter
---------

|     |     |
| --- | --- |
| **Parameter** | **Wert (Beispiele)** |
| {@DirectoryApplicationData} | C:\\Users\\\[Benutzerverzeichnis\]\\AppData\\Roaming |
| {@DirectoryCommonApplicationData} | C:\\ProgramData |
| {@DirectoryCommonDesktop} | C:\\Users\\Public\\Desktop |
| {@DirectoryCommonDocuments} | C:\\Users\\Public\\Documents |
| {@DirectoryCommonProgramFiles} | C:\\Program Files (x86)\\Common Files |
| {@DirectoryCommonPrograms} | C:\\ProgramData\\Microsoft\\Windows\\Start Menu\\Programs |
| {@DirectoryCurrent} | C:\\Program Files (x86)\\LogiSoft Batchpad |
| {@DirectoryDesktop} | C:\\Users\\\[Benutzerverzeichnis\]\\Desktop |
| {@DirectoryLocalApplicationData} | C:\\Users\\\[Benutzerverzeichnis\]\\AppData\\Local |
| {@DirectoryMyDocuments} | C:\\Users\\\[Benutzerverzeichnis\]\\Documents |
| {@DirectoryProgramFiles} | C:\\Program Files (x86) |
| {@DirectoryPrograms} | C:\\Users\\\[Benutzerverzeichnis\]\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs |
| {@DirectoryStartMenu} | C:\\Users\\\[Benutzerverzeichnis\]\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu |
| {@DirectoryStartup} | C:\\Users\\\[Benutzerverzeichnis\]\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Startup |
| {@DirectorySystem} | C:\\WINDOWS\\system32 |
| {@DirectoryUserProfile} | C:\\Users\\\[Benutzerverzeichnis\] |
| {@DirectoryWindows} | C:\\WINDOWS |