# MySQL Datenbank
MySQLConnect
------------

Die Aktion **MySQLConnect** stellt mit den angegebenen Parametern eine Verbindung zur Datenbank her. Mit dem Attribut Server wird der Servername angeben, mit Database die Datenbank an die sich angemeldet werden soll. Das Attribut User für den Benutzernamen und Password für das Passwort dienen zur Authentifizierung am Datenbankserver. Alternativ zu diesen Angaben kann über das Attribut ConnectionString auch ein kompletter ConnectionString verwendet werden.

```text-x-trilium-auto
<MySQLConnect Connection="{@myConnection}" Server="" Database="" User="" Password="" Port="" ConnectionString="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLExecute
------------

Die Aktion **MySQLExecute** sendet eine SQL-Anweisung an die Datenbank und liefert bei erfolgreicher Ausführung True als Wert in die angegebene Variable zurück. Mit dem Attribut Query wird die auszuführende SQL-Anweisung angegeben.

```text-x-trilium-auto
<MySQLExecute Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLExecuteIdentity
--------------------

Die Aktion **MySQLExecuteIdentity** gibt die ID der ausgeführten INSERT SQL-Anweisung (Attribut: Query) über das Attribut Variable zurück.

```text-x-trilium-auto
<MySQLExecuteIdentity Query="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLExists
-----------

Die Aktion **MySQLExists** prüft ob in einer Tabelle abhängig von einem Filterkriterium Datensätze vorhanden sind. Mit dem Attribut Table wird der Name der Tabelle übergeben, die überprüft werden soll. Über das Attribut Where wird das Filterkriterium festgelegt.

```text-x-trilium-auto
<MySQLExists Table="" Where="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLExistsField
----------------

Die Aktion **MySQLExistsField** prüft ob in einer Tabelle eine bestimmte Spalte vorhanden ist. Mit dem AttributTable wird der Name der Tabelle übergeben, in der nach der Spalte gesucht werden soll. Über das Attribut Field wird die zu suchende Spalte festgelegt. Mit dem Attribut IgnoreError lassen sich Fehler beim Ausführen der Aktion ignorieren.

```text-x-trilium-auto
<MySQLExistsField Table="" Field="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLExistsTable
----------------

Die Aktion **MySQLExistsTable** prüft, ob eine Tabelle in der angegeben Datenverbindung Connection vorhanden ist. Mit dem Attribut Table wird der Name der Tabelle übergeben. Mit dem Attribut IgnoreError lassen sich Fehler beim Ausführen der Aktion ignorieren.

```text-x-trilium-auto
<MySQLExistsTable Table="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLLookup
-----------

Die Aktion **MySQLLookup** liest einen einzelnen Wert aus der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Mit dem Attribut Variable wird die Platzhalter-Variable bestimmt, in der sich nach Ausführung der Aktion der ausgelesene Wert befindet.

```text-x-trilium-auto
<MySQLLookup Table="" Field="" Where="" Connection="{@myConnection}" DefaultValue="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLReadData
-------------

Die Aktion **MySQLReadData** führt eine Datenbankabfrage, die im Attribut Query hinterlegt ist, aus. Das Ergebnis der Abfrage wird in der Platzhalter-Variable gespeichert, welche über das Attribut Data angegeben wird. Die einzelnen Ergebnis-Datensätze aus der Abfrage lassen sich anschließend mit dem ForEach-Konstrukt durchiterieren.

```text-x-trilium-auto
<MySQLReadData Data="{@myData}" Query="" Connection="{@myConnection}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLFileDownload
-----------------

Die Aktion **MySQLFileDownload** speichert eine Datei aus der Datenbank unter dem im Attribut FileName angegebenen Pfad. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt.

```text-x-trilium-auto
<MySQLFileDownload FileName="" Table="" Where="" DataField="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MySQLFileUpload
---------------

Die Aktion **MySQLFileUpload** speichert eine Datei aus einem unter dem Attribut FileName angegebenen Pfad in der Datenbank. Mit dem Attribut Table wird die Tabelle angegeben und mit Field der Feldnamen dessen Wert ausgelesen werden soll. Über das Attribut Where wird der Filter auf den auszulesenden Datensatz bestimmt. Zudem besteht die optionale Möglichkeit den Namen der Datei (Attribut: FileNameField) und die Dateiendung (Attribut: ExtensionField) in der Datenbank zu speichern.

```text-x-trilium-auto
<MySQLFileUpload FileName="" Table="" Where="" DataField="" FileNameField="" ExtensionField="" Connection="{@myConnection}" Condition="" Variable="{@Result}" IgnoreError="false" />
```