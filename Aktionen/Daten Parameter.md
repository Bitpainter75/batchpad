# Daten Parameter
DataParameterAddBit
-------------------

Fügt einen Data-Parameter vom Typ Bit der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddBit Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddBoolean
-----------------------

Fügt einen Data-Parameter vom Typ Boolean der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddBoolean Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddDateTime
------------------------

Fügt einen Data-Parameter vom Typ DateTime der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddDateTime Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddDecimal
-----------------------

Fügt einen Data-Parameter vom Typ Decimal der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddDecimal Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddDouble
----------------------

Fügt einen Data-Parameter vom Typ Double der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddDouble Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddInteger
-----------------------

Fügt einen Data-Parameter vom Typ Integer der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddInteger Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddLong
--------------------

Fügt einen Data-Parameter vom Typ Long der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddLong Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddShort
---------------------

Fügt einen Data-Parameter vom Typ Short der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddShort Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterAddString
----------------------

Fügt einen Data-Parameter vom Typ String der Parameterliste hinzu.

```text-x-trilium-auto
<DataParameterAddString Name="" Value="" DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterClear
------------------

Löscht alle Parameter in der angegebenen Parameterliste.

```text-x-trilium-auto
<DataParameterClear DataParameter="{@myDataParameter}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name des Parameters.
*   **Value**: Der Wert des Parameters.
*   **DataParameter**: Die Variable der Parameterliste.

DataParameterInsert
-------------------

Fügt eine neue Zeile in die angegebene Tabelle der angegeben Datenverbindung ein.

```text-x-trilium-auto
<DataParameterInsert DataParameter="{@myDataParameter}" Connection="{@myConnection}" Table="" Identity="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **DataParameter**: Die Ziel-Parameterliste.
*   **Connection:** Die Datenverbindung auf der das Insert ausgeführt wird.
*   **Table**: Der Name der Tabelle, in die eingefügt werden soll.
*   **Identity**: Gibt an, ob der automatisch generierte Primärschlüssel zurückgegeben werden soll (true oder false).

Beispiel:

```text-x-trilium-auto
<DataParameterAddString Name="FirstName" Value="Max" DataParameter="{@myDataParameter}" />
<DataParameterAddString Name="LastName" Value="Mustermann" DataParameter="{@myDataParameter}" />
<DataParameterInsert DataParameter="{@myDataParameter}" Connection="{@myConnection}" Table="Users" Identity="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

*   Zwei Parameter (FirstName, LastName) werden mit Werten definiert.
*   Die Parameter werden verwendet, um einen neuen Benutzer in die Tabelle **Users** einzufügen.
*   Der automatisch generierte Primärschlüssel wird in der Variable **{@Result}** gespeichert.

DataParameterUpdate
-------------------

Aktualisiert eine vorhandene Zeile in der angegebenen Tabelle basierend auf einer WHERE-Bedingung.

```text-x-trilium-auto
<DataParameterUpdate DataParameter="{@myDataParameter}" Connection="{@myConnection}" Table="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **DataParameter**: Die Ziel-Parameterliste.
*   **Connection:** Die Datenverbindung auf der das Update ausgeführt wird.
*   **Table**: Der Name der Tabelle, in die eingefügt werden soll.
*   **Where**: Die WHERE-Bedingung zur Identifizierung der zu aktualisierenden Zeile.
*   **Identity**: Gibt an, ob der automatisch generierte Primärschlüssel zurückgegeben werden soll (true oder false).

Beispiel:

```text-x-trilium-auto
<DataParameterAddString Name="LastName" Value="Müller" DataParameter="{@myDataParameter}" />
<DataParameterUpdate DataParameter="{@myDataParameter}" Connection="{@myConnection}" Table="Users" Where="FirstName='Max'" Condition="" Variable="{@Result}" IgnoreError="false" />
```

*   Der Parameter **LastName** wird mit dem Wert **"Müller"** definiert.
*   Die Zeile mit **FirstName='Max'** in der Tabelle **Users** wird aktualisiert.

DataParameterExecute
--------------------

Führt eine benutzerdefinierte SQL-Abfrage mit den angegebenen Parametern aus.

```text-x-trilium-auto
<DataParameterExecute DataParameter="{@myDataParameter}" Connection="{@myConnection}" Query="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **DataParameter**: Die Parameterliste.
*   **Connection:** Die Datenverbindung auf der die Abfrage ausgeführt wird.
*   **Query**: Die SQL-Abfrage, die ausgeführt werden soll.
    

DataParameterLookup
-------------------

Liest den Wert eines bestimmten Felds aus einer Tabelle basierend auf einer WHERE-Bedingung.

```text-x-trilium-auto
<DataParameterLookup DataParameter="{@myDataParameter}" Connection="{@myConnection}" Table="" Field="" Where="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **DataParameter**: Die Parameterliste.
*   **Connection:** Die Datenverbindung auf der die Abfrage ausgeführt wird.
*   **Table**: Die Tabelle, aus der der Wert gelesen werden soll.
*   **Field**: Das Feld, dessen Wert zurückgegeben werden soll.
*   **Where**: Die WHERE-Bedingung.
    

DataParameterReadData
---------------------

Liest mehrere Datensätze aus einer SQL-Abfrage und speichert sie in einer Daten-Tabelle.

```text-x-trilium-auto
<DataParameterReadData Data="{@myData}" DataParameter="{@myDataParameter}" Connection="{@myConnection}" Query="" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Variable, in der die DataTable gespeichert wird.
*   **DataParameter**: Die Parameterliste.
*   **Query**: Die SQL-Abfrage, die ausgeführt wird.
*   **DataCount**: Speichert die Anzahl der gelesenen Datensätze.