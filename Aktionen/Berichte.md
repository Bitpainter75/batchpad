# Berichte
Die Aktionen aus der Kategorie Berichte

Allgemeine Attribute
--------------------

### Report

Das Attribut Report gibt den Pfad zu der .repx Datei an. Die .repx Datei ist eine Datei die über den in das Batchpad integrierten Berichtsdesigner erstellt werden kann (Siehe Hauptmenü).

### Parameter

Die Parameter für das Filtern der SQL Abfragen des Reports müssen über das Attribut Parameter an die Reporting Engine übergeben werden. Wie die Parameter als SQL Filter in dem Report eingesetzt werden, wird hier gezeigt: [https://docs.logisoft.de/share/m9JXdpWNfeo6](https://docs.logisoft.de/share/m9JXdpWNfeo6)

Beispiel

```text-x-trilium-auto
Parameter="FilterArtikelnummer:='00100041';FilterMandant=123"
```

### Filter

Filter grenzt die Datensätze des Berichts über einen Filterausdruck **Client-Seitig** ein, aber nicht für die Abfrage gegen den SQL Server. Für eine Filterung der SQL Abfrage müssen im Bericht Parameter angelegt und in das Filterstatement der Abfrage eingebaut werden. Die Parameter fürs Filtern können dann über das Attribut Parameter an die Reporting Engine übergeben werden. 

Das Attribut **Filter** sollte nur im Ausnahmefall verwendet werden. Das Filtern der SQL Abfragen muss über das Attribut **Parameter** erfolgen, siehe hierzu: [https://docs.logisoft.de/share/m9JXdpWNfeo6](https://docs.logisoft.de/share/m9JXdpWNfeo6)

Die Syntax für den Wert des Attributs Filter entspricht der Critearia Language Syntax. Beispielsweise würde folgender Filter nach der UserId mit dem Wert 1 filtern:

```text-x-trilium-auto
UserId==1
```

Falls die UserId eine Zeichenfolge enthält muss der Wert mit Hochkommas umschlossen werden:

```text-x-trilium-auto
UserId=='1'
```

### Export

Das Attribut Export gibt den Pfad, den Dateinamen und die Dateiendung des zu speichernden Berichts an. Hinweis: Bei der Angabe der Dateiendung das Ausgabeformat der Aktion beachten.

ReportExportPDF
---------------

Die Aktion ReportExportPDF erzeugt einen Bericht im PDF Format.

```text-x-trilium-auto
<ReportExportPDF Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportJPG
---------------

Die Aktion ReportExportJPG erzeugt einen Bericht im JPG Format.

```text-x-trilium-auto
<ReportExportJPG Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportHTML
----------------

Die Aktion ReportExportHTML erzeugt einen Bericht im HMTL Format.

```text-x-trilium-auto
<ReportExportHTML Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportRTF
---------------

Die Aktion ReportExportRTF erzeugt einen Bericht im RTF Format.

```text-x-trilium-auto
<ReportExportRTF Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportDOCX
----------------

Die Aktion ReportExportDOCX erzeugt einen Bericht im DOCX Format.

```text-x-trilium-auto
<ReportExportDOCX Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportXLSX
----------------

Die Aktion ReportExportXLSX erzeugt einen Bericht im XLSX Format.

```text-x-trilium-auto
<ReportExportXLSX Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportExportCSV
---------------

Die Aktion ReportExportCSV erzeugt einen Bericht im CSV Format.

```text-x-trilium-auto
<ReportExportCSV Report="" Export="" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ReportPrint
-----------

Die Aktion ReportPrint erzeugt einen Bericht und druckt diesen Bericht über den im Attribut Printer angegebenen Drucker. Über das Attribut Copies kann die Anzahl der Kopien festgelegt werden.

```text-x-trilium-auto
<ReportPrint Report="" Printer="" Copies="1" Filter="" Parameter="" Condition="" Variable="{@Result}" IgnoreError="false" />
```