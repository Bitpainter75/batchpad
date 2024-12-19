# MS-SQL Datenbank
SQLConnect
----------

Die Aktion **SQLConnect** stellt mit den angegebenen Parametern eine Verbindung zur Datenbank her. Mit dem Attribut Server wird der Servername angeben, mit Database die Datenbank, an die sich angemeldet werden soll. Das Attribut User für den Benutzernamen und Password für das Passwort dienen zur Authentifizierung am Datenbankserver. Alternativ zu diesen Angaben kann über das Attribut ConnectionString auch ein kompletter ConnectionString verwendet werden.

```text-x-trilium-auto
<SQLConnect Connection="{@myConnection}" Server="" Database="" User="" Password="" Port="" ConnectionString="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLExecute
----------

Die Aktion **SQLExecute** sendet eine SQL-Anweisung an die Datenbank und liefert bei erfolgreicher Ausführung True als Wert in die angegebene Variable zurück. Mit dem Attribut Query wird die auszuführende SQL-Anweisung angegeben.

```text-x-trilium-auto
<SQLExecute Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLExecuteIdentity
------------------

Die Aktion **SQLExecuteIdentity** gibt die ID der ausgeführten INSERT SQL-Anweisung (Attribut: Query) über das Attribut Variable zurück.

```text-x-trilium-auto
<SQLExecuteIdentity Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLExists
---------

Die Aktion **SQLExists** prüft ob in einer Tabelle abhängig von einem Filterkriterium Datensätze vorhanden sind. Mit dem Attribut Table wird der Name der Tabelle übergeben, die überprüft werden soll. Über das Attribut Where wird das Filterkriterium festgelegt.

```text-x-trilium-auto
<SQLExists Table="" Where="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLExistsField
--------------

Die Aktion **SQLExistsField** prüft ob in einer Tabelle eine bestimmte Spalte vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben, in der nach der Spalte gesucht werden soll. Über das Attribut Field wird die zu suchende Spalte festgelegt.

```text-x-trilium-auto
<SQLExistsField Table="" Field="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLExistsTable
--------------

Die Aktion **SQLExistsTable** prüft ob eine Tabelle in der angegeben Datenverbindung Connection vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben.

```text-x-trilium-auto
<SQLExistsTable Table="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLLookup
---------

Die Aktion **SQLLookup** liest einen einzelnen Wert aus der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Mit dem Attribut Variable wird die Platzhalter-Variable bestimmt, in der sich nach Ausführung der Aktion der ausgelesene Wert befindet.

```text-x-trilium-auto
<SQLLookup Table="" Field="" Where="" Connection="{@myConnection}" DefaultValue="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLReadData
-----------

Die Aktion **SQLReadData** führt eine Datenbankabfrage die im Attribut Query hinterlegt ist aus. Das Ergebnis der Abfrage wird in der Platzhalter-Variable gespeichert, welche über das Attribut Data angegeben wird. Die einzelnen Ergebnis-Datensätze aus der Abfrage lassen sich anschließend mit dem ForEach-Konstrukt durchiterieren.

```text-x-trilium-auto
<SQLReadData Data="{@myData}" Query="" Connection="{@myConnection}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLFileDownload
---------------

Die Aktion **SQLFileDownload** speichert eine Datei aus der Datenbank unter dem im Attribut FileName angegebenen Pfad. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt.

```text-x-trilium-auto
<SQLFileDownload FileName="" Table="" Where="" DataField="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SQLFileUpload
-------------

Die Aktion **SQLFileUpload** speichert eine Datei aus einem unter dem Attribut FileName angegebenen Pfad in der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Zudem besteht die optionale Möglichkeit den Namen der Datei (Attribut: FileNameField) und die Dateiendung (Attribut: ExtensionField) in der Datenbank zu speichern.

```text-x-trilium-auto
<SQLFileUpload FileName="" Table="" Where="" DataField="" FileNameField="" ExtensionField="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```