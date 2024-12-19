# Daten Tabellen
Verwendung von Daten Tabellen
-----------------------------

"Daten Tabellen" im Kontext des Batchpad sind Tabellen, die zur Laufzeit des Skripts aufgebaut werden. Spalten werden über die Aktionen DataAdd... hinzugefügt. Reihen über die Aktion DataRowInsert.

Die "Daten Tabellen" können zur Laufzeit befüllt, kopiert und gelöscht werden. Zudem können die "Daten Tabellen" über die Aktionen DataUpdate und DataInsert in eine Datenbank geschrieben werden.

Die "Daten Tabellen" können zur Laufzeit über den Inspektor eingesehen werden. Der Inspektor zeigt wie die "Daten Tabellen" zur Laufzeit mit Spalten und Reihen erweitert und mit Daten befüllt werden.

DataAddBooleanColumn
--------------------

Die Aktion **DataAddBooleanColumn** fügt eine Spalte des Datentyps Boolean der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddBooleanColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddDateTimeColumn
---------------------

Die Aktion **DataAddDateTimeColumn** fügt eine Spalte des Datentyps DateTime der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddDateTimeColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddDecimalColumn
--------------------

Die Aktion **DataAddDecimalColumn** fügt eine Spalte des Datentyps Decimal der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddDecimalColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddDoubleColumn
-------------------

Die Aktion **DataAddDoubleColumn** fügt eine Spalte des Datentyps Double der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddDoubleColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddIntegerColumn
--------------------

Die Aktion **DataAddIntegerColumn** fügt eine Spalte des Datentyps Integer der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddIntegerColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddLongColumn
-----------------

Die Aktion **DataAddLongColumn** fügt eine Spalte des Datentyps Long der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddLongColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddShortColumn
------------------

Die Aktion **DataAddShortColumn** fügt eine Spalte des Datentyps Short der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddShortColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAddStringColumn
-------------------

Die Aktion **DataAddStringColumn** fügt eine Spalte des Datentyps String der Daten-Tabelle (Attribut: Data) hinzu. Der Spaltenname wir über das Attribut Name gesetzt. Nullwerte können über das Attribut AllowNull erlaubt werden. Sollen die Werte bei einem Update/Insert (Aktionen DataUpdate und DataInsert) in eine Datenbank ignoriert werden kann über das Attribut IngoreOnWrite auf true gesetzt werden.

```text-x-trilium-auto
<DataAddStringColumn Data="{@myData}" Name="" AllowNull="true" IgnoreOnWrite="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRemoveColumn
----------------

Die Aktion **DataRemoveColumn** löscht eine Spalte aus der Daten-Tabelle (Attribut: Data). Die zu löschende Spalte kann über das Attribut Name angegeben werden.

```text-x-trilium-auto
<DataRemoveColumn Data="{@myData}" Name="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataCopy
--------

Die Aktion **DataCopy** kopiert eine Daten-Tabelle (Attribut: Data) in eine neue Daten-Tabelle (Attribut: DataCopy). Wenn die Daten bei dem Kopieren mit in die neue Tabelle übernommen werden sollen kann das Attribut SchemaOnly auf false gesetzt werden. Zudem kann über einen Filter (Attribut: Where) mit SQL-Syntax bestimmt werden welche Reihen aus der Tabelle übernommen werden. Über das Attribut OrderBy kann mit SQL-Syntax die Reihen der Tabelle sortiert werden. Die Anzahl der kopierten Reihen wird über das Attribut DataCount ausgegeben.

```text-x-trilium-auto
<DataCopy Data="{@myData}" DataCopy="{@myDataCopy}" Where="" OrderBy="" SchemaOnly="false" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataInsert
----------

Die Aktion **DataInsert** führt einen INSERT Befehl auf der angegeben Datenbank Tabelle durch (Attribut: Table). Bei dem INSERT werden die Daten aus der Daten-Tabelle (Attribut: Data) in angegebene Datenbank geschrieben (Attribut: Connection). Über das Attribut StopWhenRowFaild wird angegeben ob bei einem INSERT Fehler die noch offenen INSERT Befehle auf die Datenbank ausgeführt (false) oder abgebrochen werden sollen (true).

```text-x-trilium-auto
<DataInsert Data="{@myData}" Table="" Connection="{@myConnection}" StopWhenRowFailed="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataUpdate
----------

Die Aktion **DataUpdate** führt einen UPDATE Befehl auf der angegeben Datenbank Tabelle durch (Attribut: Table). Bei dem UPDATE wird über die Daten aus der Daten-Tabelle (Attribut: Data) ein UPDATE auf die Datenbank ausgeführt (Attribut: Connection). Über das Attribut StopWhenRowFaild wird angegeben ob bei einem UPDATE Fehler die noch offenen UPDATE Befehle auf die Datenbank ausgeführt (false) oder abgebrochen werden sollen (true). Zudem kann ein Filter (Attribut: Where) mit SQL-Syntax bestimmt werden. 

```text-x-trilium-auto
<DataUpdate Data="{@myData}" Table="" Where="" Connection="{@myConnection}" StopWhenRowFailed="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRowClear
------------

Die Aktion **DataRowClear** löscht alle Reihen aus der Daten-Tabelle (Attribut: Data)

```text-x-trilium-auto
<DataRowClear Data="{@myData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRowCount
------------

Die Aktion **DataRowCount** ermittelt die Anzahl der Datensätze in der Daten-Tabelle

```text-x-trilium-auto
<DataRowCount Data="{@myData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRowInsert
-------------

Die Aktion **DataRowInsert** fügt einer Daten-Tabelle (Attribut: Data) eine neue Reihe hinzu. Die neu hinzugefügte Reihe enthält keine Werte. 

```text-x-trilium-auto
<DataRowInsert Data="{@myData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRowGetValue
---------------

Die Aktion **DataRowGetValue** liest aus der Daten-Tabelle (Attribut: Data) der aktiven Reihe und der Spalte (Attribut: Name) den Wert aus und gibt den Wert über das Attribut Variable aus.

```text-x-trilium-auto
<DataRowGetValue Name="" Data="{@myData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataRowSetValue
---------------

Die Aktion **DataRowSetValue** setzt in der Daten-Tabelle (Attribut: Data) der aktiven Reihe in der Spalte (Attribut: Name) einen Wert (Attribut: Value).

```text-x-trilium-auto
<DataRowSetValue Name="" Value="" Data="{@myData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAggregateAvg
----------------

Die Aktion **DataAggregateAvg** gibt den durchnittlichen Wert der Spalte (Attribut: Field) aus der Daten-Tabelle (Attribut: Data) über das Attribut Variable zurück. Ein Filter in SQL-Syntax kann über das Attribut Where gesetzt werden.

```text-x-trilium-auto
<DataAggregateAvg Data="{@myData}" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAggregateCount
------------------

Die Aktion **DataAggregateCount** gibt die Anzahl der Werte der Spalte (Attribut: Field) aus der Daten-Tabelle (Attribut: Data) über das Attribut Variable zurück. Ein Filter in SQL-Syntax kann über das Attribut Where gesetzt werden.

```text-x-trilium-auto
<DataAggregateCount Data="{@myData}" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAggregateMax
----------------

Die Aktion **DataAggregateMax** gibt den maximalen Wert der Spalte (Attribut: Field) aus der Daten-Tabelle (Attribut: Data) über das Attribut Variable zurück. Ein Filter in SQL-Syntax kann über das Attribut Where gesetzt werden.

```text-x-trilium-auto
<DataAggregateMax Data="{@myData}" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAggregateMin
----------------

Die Aktion **DataAggregateMin** gibt den minimalen Wert der Spalte (Attribut: Field) aus der Daten-Tabelle (Attribut: Data) über das Attribut Variable zurück. Ein Filter in SQL-Syntax kann über das Attribut Where gesetzt werden.

```text-x-trilium-auto
<DataAggregateMin Data="{@myData}" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DataAggregateSum
----------------

Die Aktion **DataAggregateSum** gibt die Summe der Werte in der Spalte (Attribut: Field) aus der Daten-Tabelle (Attribut: Data) über das Attribut Variable zurück. Ein Filter in SQL-Syntax kann über das Attribut Where gesetzt werden.

```text-x-trilium-auto
<DataAggregateSum Data="{@myData}" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```