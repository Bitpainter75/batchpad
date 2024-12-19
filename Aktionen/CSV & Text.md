# CSV & Text
CSVReadData
-----------

Die Aktion CSVReadData gibt ein DataTable Objekt zurück (Attribut: Data), welches aus einer CSV Datei ausgelesen wird (Attribut: File). Das Attribut Delimiter bestimmt mit welchem Zeichen die einzulesenden Einträge getrennt sind. Über das Attribut FirstLineIsHeader wird angegeben, dass die erste Reihe für die Bezeichnung der Spalten herangezogen wird. Über diese Bezeichnung werden die Spalten beschriftet und können über diese Bezeichnung über das DataTable Objekt angesprochen werden (Siehe Allgemein/ForEach). Werden keine Spaltenbezeichnungen angegeben, werden die Spalten aufsteigend mit ganzen Zahlen beginnend bei 0 beschriftet. Die Codierung der Datei wird über das Attribut Codepage angegeben. Sind die Felder oder einzelne Felder mit Anführungszeichen versehen, und die Felder sollen ohne zusätzliche Anführungszeichen in das DataTable Objekt übernommen werden, muss das Attribut HasFieldsEnclosedInQuotes auf true gesetzt werden. Über das Attribut DataCount wird die Anzahl der Datensätze zurückgegeben.

```text-x-trilium-auto
<CSVReadData Data="{@myData}" File="" Codepage="1252" Delimiter=";" HasFieldsEnclosedInQuotes="true" FirstLineIsHeader="true" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

CSVWriteData
------------

Die Aktion CSVWriteData schreibt ein DataTable Objekt (Attribut: Data) in eine CSV Datei (Attribut: File). Das Attribut Delimiter bestimmt mit welchem Zeichen die zu schreibenden Zeichen getrennt werden. Über das Attribut FirstLineIsHeader wird angegeben, dass die erste Reihe für die Bezeichnung der Spalten herangezogen wird. Werden keine Spaltenbezeichnungen angegeben, wird die CSV Datei ohne einen Kopfbereich erstellt. Die Codierung der Datei wird über das Attribut Codepage angegeben. Sind die Felder oder einzelne Felder mit Anführungszeichen versehen, und die Felder sollen mit dem Anführungszeichen in die CSV Datei übernommen werden, muss das Attribut HasFieldsEnclosedInQuotes auf true gesetzt werden.

```text-x-trilium-auto
<CSVWriteData Data="{@myData}" File="" Codepage="1252" Delimiter=";" HasFieldsEnclosedInQuotes="true" FirstLineIsHeader="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

TextFileRead
------------

Die Aktion TextFileRead gibt einen Text zurück (Attribut Variable). Über das Attribut File wird die auszulesende Datei angegeben. Die Codierung der Datei wird über das Attribut Codepage angegeben.

```text-x-trilium-auto
<TextFileRead File="" Codepage="1252" Condition="" Variable="{@Result}" IgnoreError="false" />
```

TextFileWrite
-------------

Die Aktion TextFileWrite schreibt einen bestimmten Text (Attribut Content) eine Datei (Attribut: File). Die Codierung der Datei wird über das Attribut Codepage angegeben. Soll der Text an einen Text in einer bestehenden Textdatei angehangen werden, muss das Attribut Append auf true gesetzt werden. Der Text wird dabei ohne einen Zeilenumbruch an den bestehenden Text angehangen.

```text-x-trilium-auto
<TextFileWrite File="" Content="" Append="false" Codepage="1252" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ExcelReadData
-------------

Liest Daten aus einer Excel-Datei und speichert sie in einem Daten-Objekt.

```text-x-trilium-auto
<ExcelReadData Data="{@myData}" File="" WorksheetName="" StartAtLine="0" StartLineIsHeader="false" Variable="{@Result}" />
```

Attribute:

*   **Data**: Variable, in der die ausgelesenen Daten gespeichert werden.
*   **File**: Pfad zur Excel-Datei, aus der die Daten gelesen werden sollen.
*   **WorksheetName**: Name des Arbeitsblatts, das gelesen wird.
*   **StartAtLine**: Zeile, ab der das Lesen beginnt.
*   **StartLineIsHeader**: Gibt an, ob die Startzeile als Kopfzeile behandelt wird (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

TextConvertToUTF8
-----------------

Konvertiert einen Text in das UTF-8-Format.

```text-x-trilium-auto
<TextConvertToUTF8 Text="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Text**: Text, der konvertiert werden soll.
*   **Variable**: Variable, in der der konvertierte Text gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

TextConvertCodepage
-------------------

Konvertiert Text von einer Codepage in eine andere.

```text-x-trilium-auto
<TextConvertCodepage Text="" FromCodepage="1252" ToCodepage="65001" Variable="{@Result}" />
```

Attribute:

*   **Text**: Text, der konvertiert werden soll.
*   **FromCodepage**: Ursprüngliche Codepage des Textes.
*   **ToCodepage**: Ziel-Codepage, in die der Text konvertiert wird.
*   **Variable**: Variable, in der der konvertierte Text gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

TextClipboardRead
-----------------

Liest den aktuellen Inhalt der Zwischenablage und speichert ihn in einer Variablen.

```text-x-trilium-auto
<TextClipboardRead Variable="{@Result}" />
```

Attribute:

*   **Variable**: Variable, in der der Inhalt aus der Zwischenablage gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

TextClipboardWrite
------------------

Schreibt einen Inhalt in die Zwischenablage.

```text-x-trilium-auto
<TextClipboardWrite Content="" Variable="{@Result}" />
```

Attribute:

*   **Content**: Inhalt, der in die Zwischenablage geschrieben wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

DelimitedStringFromDataColumn
-----------------------------

Erstellt eine Zeichenkette aus den Werten einer bestimmten Spalte in einer Datentabelle.

```text-x-trilium-auto
<DelimitedStringFromDataColumn Data="{@myData}" Column="" Delimiter="," HasFieldsEnclosedInQuotes="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Datentabelle, die verarbeitet wird.
*   **Column**: Name der Spalte, aus der die Werte gelesen werden.
*   **Delimiter**: Trennzeichen welches zwischen den Werten verwendet werden soll.
*   **HasFieldsEnclosedInQuotes** Ob Felder in Anführungszeichen eingeschlossen werden sollen.
*   **Variable**: Variable, in der die erzeugte Zeichenkette gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.
    

DelimitedStringFromDataRow
--------------------------

Erstellt eine Zeichenkette aus den Werten einer einzelnen Zeile in einer Datentabelle.

```text-x-trilium-auto
<DelimitedStringFromDataRow Data="{@myData}" Delimiter="," HasFieldsEnclosedInQuotes="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Datentabelle, aus der die Zeile gelesen wird.
*   **Delimiter** Trennzeichen welches zwischen den Werten verwendet werden soll.
*   **HasFieldsEnclosedInQuotes** Ob Felder in Anführungszeichen eingeschlossen werden sollen.
*   **Variable**: Variable, in der die erzeugte Zeichenkette gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.