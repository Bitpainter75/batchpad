# Rekursive Datensicherung
Zeigt wie eine Funktion rekursiv aufgerufen werden kann, um z.B. eine Datensicherung durchzuführen.

```text-x-trilium-auto
<!-- Vor der Ausführung Parameter im Batchpad hinterlegen: QuelleBackupOrdner ZielBackupOrdner ZielBackupOrdnerSicherheitskopie NameOrdnerSicherheitskopie-->
<Batch>
    <!-- ###### 1. Vorbereitung ####### -->
    <!-- Zielpfad erstellen falls nicht vorhanden -->
    <PathExists Path="{@ZielBackupOrdner}" Variable="{@Existiert}" />
    <ConditionTrue Condition="NOT {@Existiert}">
        <PathCreate Path="{@ZielBackupOrdner}" Variable="{@Result}" />
    </ConditionTrue>

    <ConditionTrue Condition="{@Existiert}">
        <!-- Sicherheitskopie des Backups löschen -->
        <PathExists Path="{@ZielBackupOrdnerSicherheitskopie}" Variable="{@Existiert}" />
        <ConditionTrue Condition="{@Existiert}">
            <PathDelete Path="{@ZielBackupOrdnerSicherheitskopie}" Variable="{@Result}" />
        </ConditionTrue>
        <!-- Sicherheitskopie des letzten Backups erstellen -->
        <PathRename Path="{@ZielBackupOrdner}" NewName="{@NameOrdnerSicherheitskopie}" Variable="{@Result}" />
    </ConditionTrue>

    <!-- Variablen fuer den Backup Vorgang initialisieren -->
    <Set Variable="{@AktuellesVerzeichnisVollerPfad}" Value="{@QuelleBackupOrdner}" />
    <Set Variable="{@AktuellesVerzeichnis}" Value="\" />

    <!-- ###### 2. Backup ausführen ######## -->
    <CallFunction Name="{@backup}" Variable="{@Result}" />
    
    <Function Name="{@backup}">
        <!-- Alle Dateien und Verzeichnisse auslesen -->
        <FileListDirectory Source="{@AktuellesVerzeichnisVollerPfad}" Data="{@myData}" OnlyFiles="false" OnlyDirectories="false" WithInformations="true" DataCount="{@ResultCount}" />
        <ForEach Data="{@myData}">
            <ConditionTrue Condition="{@Data:IsDirectory}">
                <!-- Verzeichnispfade neu setzen -->
                <StringReplace Value="{@Data:FullName}" Search="{@QuelleBackupOrdner}" Replace="" Variable="{@Result}" />
                <Set Variable="{@AktuellesVerzeichnisVollerPfad}" Value="{@Data:FullName}" />
                <Set Variable="{@AktuellesVerzeichnis}" Value="{@Result}" />
                <!-- Rekursiver Aufruf -->
                <CallFunction Name="{@backup}" Variable="{@Result}" />
            </ConditionTrue>

            <ConditionTrue Condition="{@Data:IsFile}">
                <!-- Verzeichnis anlegen wenn nicht vorhanden -->
                <PathExists Path="{@ZielBackupOrdner}{@AktuellesVerzeichnis}" Variable="{@Result}" />
                <ConditionTrue Condition="NOT {@Result}">
                    <PathCreate Path="{@ZielBackupOrdner}{@AktuellesVerzeichnis}" Variable="{@Result}" />
                </ConditionTrue>
                <!-- Datei kopieren -->
                <FileCopy Source="{@Data:FullName}" Destination="{@ZielBackupOrdner}{@AktuellesVerzeichnis}\{@Data:Value}" Overwrite="true" Variable="{@Result}" />
            </ConditionTrue>
        </ForEach>
    </Function>
</Batch>
```

Das Skript soll den Umgang mit Funktionen demonstrieren und zeigen wie rekursiv die Ordner und Dateien aus einem Dateisystem ausgelesen werden können.

Zur Datensicherung gibt es effizienterer Methoden wie die BatchPad Aktion FileMirror. Mehr Informationen zu FileMirror gibt es unter der Rubrik "Aktionen und Parameter".