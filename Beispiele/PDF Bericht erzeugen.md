# PDF Bericht erzeugen
Das Beispiel zeigt wie mit dem Batchpad ein PDF-Bericht erstellt wird. Dazu wird ein eine Vorlage aufgerufen, welche mit dem integrierten Berichtsdesigner entworfen wurde.

Um das Beispiel zur Ausführung zu bringen müssen folgende Schritte beachtet werden

*   Das im Anhang verfügbare SQL-Skript (DateienBeispielBerichtBatchpad.zip) ausführen. Dabei werden die benötigten Tabellen angelegt und Demodatensätze erzeugt.
*   Der vorgefertigte Bericht (Reisekosten.repx) liegt im Anhang (DateienBeispielBerichtBatchpad.zip) und muss in das entsprechende Verzeichnis gelegt werden.
*   Die Pfade in folgendem Batchpad Skript überarbeiten und das Skript anschließend zur Ausführung bringen. Die erzeugten PDF-Berichte befinden sich anschließend in dem angegebenen Ordner.

```text-x-trilium-auto
<Batch>
    <Set Variable="{@ExportFolder}" Value="E:\Ablage" />
    <!-- Datenbankverbindung aufbauen und Datensätze auslesen-->
    <SQLConnect Connection="{@myConnection}" ConnectionString="{@ConnectionString}" Variable="{@ResultConnect}" />
    
    <SQLReadData Data="{@myData}" Query="SELECT * FROM mydsReisekosten_Bericht" Connection="{@myConnection}" 
                 Condition="{@ResultConnect}" />

    <PathExists Path="{@ExportFolder}" Variable="{@ResultExists}" />
    <PathCreate Path="{@ExportFolder}" Condition="NOT {@ResultExists}" />

    <PathExists Path="{@ExportFolder}\Reisekostenabrechnungen" Variable="{@ResultExists}" />
    <PathCreate Path="{@ExportFolder}\Reisekostenabrechnungen" Condition="NOT {@ResultExists}" />

    <ForEach Data="{@myData}">
        <!-- Jeden Eintrag unter mydsReisekosten_Bericht abarbeiten--> 
        <PathExists Path="{@ExportFolder}\Reisekostenabrechnungen\{@Data:UserId}" Variable="{@ResultExists}" />
        <PathCreate Path="{@ExportFolder}\Reisekostenabrechnungen\{@Data:UserId}" Condition="NOT {@ResultExists}" />
        <!-- Report erstellen. Dabei wird der über den Berichtsdesigner entworfene Report verwendet. Über den angegebenen Filter wird der Bericht gefiltert --> 
        <ReportExportPDF Report="E:\Ablage\Reisekostenabrechnungen\Reisekosten.repx" Filter="UserId=='{@Data:UserId}'"
                         Export="{@ExportFolder}\Reisekostenabrechnungen\{@Data:UserId}\{@Data:UserId}.pdf" />
    </ForEach>
</Batch>
```

Hinweise:

*   Die Syntax des Filters entspricht der Critearia Language Syntax. Zu beachten ist das der Parmater UserId ein String ist und in dem Filter mit Hochkommas umschlossen werden muss.
*   Der Bericht wurde über den integrierten Berichtsdesigner entworfen (Mit Hilfe des integrierten Assistenten -> Tabellen Bericht). Der vorgefertigte Bericht kann, über den im BatchPad integrierten Berichtsdesigner, bearbeitet werden.
*   Der Berichtszeitraum kann über die Tabelle mydsReisekosten\_Bericht verändert werden.