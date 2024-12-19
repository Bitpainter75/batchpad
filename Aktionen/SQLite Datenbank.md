# SQLite Datenbank
SQLiteConnect
-------------

Die Aktion **SQLiteConnect** stellt mit den angegebenen Parametern eine Verbindung zur Datenbank her. Mit Attribut Server wird der Servername angeben, mit Database die Datenbank, an die sich angemeldet werden soll. Das Attribut User für den Benutzernamen und Password für das Passwort dienen zur Authentifizierung am Datenbankserver. Alternativ zu diesen Angaben kann über das Attribut ConnectionString auch ein kompletter ConnectionString verwendet werden.

```text-x-trilium-auto
<SQLiteConnect Connection="{@myConnection}" Database="" User="" Password="" Create="false" ConnectionString="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteExecute
-------------

Die Aktion **SQLiteExecute** sendet eine SQL-Anweisung an die Datenbank und liefert bei erfolgreicher Ausführung True als Wert in die angegebene Variable zurück. Mit dem Attribut Query wird die auszuführende SQL-Anweisung angegeben.

```text-x-trilium-auto
<SQLiteExecute Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteExecuteIdentity
---------------------

Die Aktion **SQLiteExecuteIdentity** gibt die ID der ausgeführten INSERT SQL-Anweisung (Attribut: Query) über das Attribut Variable zurück.

```text-x-trilium-auto
<SQLiteExecuteIdentity Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteExists
------------

Die Aktion **SQLiteExists** prüft, ob in einer Tabelle abhängig von einem Filterkriterium Datensätze vorhanden sind. Mit dem Attribut Table wird der Name der Tabelle übergeben, die überprüft werden soll. Über das Attribut Where wird das Filterkriterium festgelegt.

```text-x-trilium-auto
<SQLiteExists Table="" Where="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteExistsField
-----------------

Die Aktion **SQLiteExistsField** prüft, ob in einer Tabelle eine bestimmte Spalte vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben, in der nach der Spalte gesucht werden soll. Über das Attribut Field wird die zu suchende Spalte festgelegt.

```text-x-trilium-auto
<SQLiteExistsField Table="" Field="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteExistsTable
-----------------

Die Aktion **SQLiteExistsTable** prüft ob eine Tabelle in der angegeben Datenverbindung Connection vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben.

```text-x-trilium-auto
<SQLiteExistsTable Table="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteLookup
------------

Die Aktion **SQLiteLookup** liest einen einzelnen Wert aus der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Mit dem Attribut Variable wird die Platzhalter-Variable bestimmt, in der sich nach Ausführung der Aktion der ausgelesene Wert befindet.

```text-x-trilium-auto
<SQLiteLookup Table="" Field="" Where="" Connection="{@myConnection}" DefaultValue="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLiteReadData
--------------

Die Aktion **SQLiteReadData** führt eine Datenbankabfrage, die im Attribut Query hinterlegt ist, aus. Das Ergebnis der Abfrage wird in der Platzhalter-Variable gespeichert, welche über das Attribut Data angegeben wird. Die einzelnen Ergebnis-Datensätze aus der Abfrage lassen sich anschließend mit dem ForEach-Konstrukt durchiterieren.

```text-x-trilium-auto
<SQLiteReadData Data="{@myData}" Query="" Connection="{@myConnection}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```