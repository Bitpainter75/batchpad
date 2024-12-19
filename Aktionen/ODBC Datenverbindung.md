# ODBC Datenverbindung
ODBCConnect
-----------

Die Aktion ODBCConnect stellt mit den angegebenen Parametern eine Verbindung zur Datenbank her. Über das Attribut ConnectionString wird ein kompletter ConnectionString zum Aufbau der Datenverbindung angegeben.

```text-x-trilium-auto
<ODBCConnect Connection="{@myConnection}" ConnectionString="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCExecute
-----------

Die Aktion ODBCExecute sendet eine SQL-Anweisung an die Datenbank und liefert bei erfolgreicher Ausführung True als Wert in die angegebene Variable zurück. Mit dem Attribut Query wird die auszuführende SQL-Anweisung angegeben.

```text-x-trilium-auto
<ODBCExecute Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCExists
----------

Die Aktion ODBCExists prüft, ob in einer Tabelle abhängig von einem Filterkriterium Datensätze vorhanden sind. Mit dem Attribut Table wird der Name der Tabelle übergeben, die überprüft werden soll. Über das Attribut Where wird das Filterkriterium festgelegt.

```text-x-trilium-auto
<ODBCExists Table="" Where="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCExistsField
---------------

Die Aktion ODBCExistsField prüft, ob in einer Tabelle eine bestimmte Spalte vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben, in der nach der Spalte gesucht werden soll. Über das Attribut Field wird die zu suchende Spalte festgelegt.

```text-x-trilium-auto
<ODBCExistsField Table="" Field="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCExistsTable
---------------

Die Aktion ODBCExistsTable prüft, ob eine Tabelle in der angegeben Datenverbindung Connection vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben.

```text-x-trilium-auto
<ODBCExistsTable Table="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCLookup
----------

Die Aktion ODBCLookup liest einen einzelnen Wert aus der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Mit dem Attribut Variable wird die Platzhalter-Variable bestimmt, in der sich nach Ausführung der Aktion der ausgelesene Wert befindet.

```text-x-trilium-auto
<ODBCLookup Table="" Field="" Where="" Connection="{@myConnection}" DefaultValue="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ODBCReadData
------------

Die Aktion ODBCReadData führt eine Datenbankabfrage, die im Attribut Query hinterlegt ist, aus. Das Ergebnis der Abfrage wird in der Platzhalter-Variable gespeichert, welche über das Attribut Data angegeben wird. Die einzelnen Ergebnis-Datensätze aus der Abfrage lassen sich anschließend mit dem ForEach-Konstrukt durchiterieren.

```text-x-trilium-auto
<ODBCReadData Data="{@myData}" Query="" Connection="{@myConnection}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```