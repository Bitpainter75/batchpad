# XML & JSON
XMLCreateDocument
-----------------

Erstellt ein neues XML-Dokument.

```text-x-trilium-auto
<XMLCreateDocument Document="{@myXml}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: Variable, in der das neue XML-Dokument erzeugt wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLOpenDocument
---------------

Öffnet ein bestehendes XML-Dokument aus einem Dateipfad oder Inhalt.

```text-x-trilium-auto
<XMLOpenDocument Document="{@myXml}" Content="" File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: Variable, in der das neue XML-Dokument gespeichert wird.
*   **Content**: Inhalt eines XML-Dokuments als Zeichenkette.
*   **File**: Pfad zur XML-Datei, die geöffnet werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLSaveDocument
---------------

Speichert ein XML-Dokument in eine Datei.

```text-x-trilium-auto
<XMLSaveDocument Document="{@myXml}" File="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, das gespeichert werden soll.
*   **File**: Dateipfad, in den das XML-Dokument gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLHasElement
-------------

Prüft, ob ein bestimmtes Element in einem XML-Dokument vorhanden ist.

```text-x-trilium-auto
<XMLHasElement Document="{@myXml}" Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, das durchsucht wird.
*   **Path**: XPath-Pfad zum zu prüfenden Element.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLGetElement
-------------

Liest ein Element aus einem XML-Dokument.

```text-x-trilium-auto
<XMLGetElement Document="{@myXml}" Data="" Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, aus dem das Element gelesen wird.
*   **Data**: Variable, in der der Inhalt des Elements gespeichert wird.
*   **Path**: XPath-Pfad zum Element.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLAddElement
-------------

Fügt ein neues Element zu einem bestehenden XML-Dokument hinzu.

```text-x-trilium-auto
<XMLAddElement Document="{@myXml}" ParentData="" Data="" Name="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, zu dem das neue Element hinzugefügt wird.
*   **ParentData**: XPath-Pfad oder Element, unter dem das neue Element erstellt wird.
*   **Data**: Variable, in der das neue Element gespeichert wird.
*   **Name**: Name des neuen Elements.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLRemoveElement
----------------

Entfernt ein Element aus einem XML-Dokument.

```text-x-trilium-auto
<XMLRemoveElement Document="{@myXml}" Data="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, aus dem das Element entfernt wird.
*   **Data**: XPath-Pfad zum zu entfernenden Element.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLHasChildElements
-------------------

Prüft, ob ein bestimmtes XML-Element untergeordnete Elemente (Child-Elements) enthält.

```text-x-trilium-auto
<XMLHasChildElements Document="{@myXml}" Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, das analysiert wird.
*   **Path**: XPath-Pfad zum zu prüfenden Element.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob untergeordnete Elemente vorhanden sind. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLHasAttribute
---------------

Prüft, ob ein bestimmtes Attribut in einem XML-Element existiert.

```text-x-trilium-auto
<XMLHasAttribute Document="{@myXml}" Data="" Path="" Attribute="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, das geprüft wird.
*   **Data**: Variable, die das Element enthält.
*   **Path**: XPath-Pfad zum Element.
*   **Attribute**: Name des Attributs, das geprüft werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob das gesuchte Attribut vorhanden ist. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLGetAttribute
---------------

Liest den Wert eines Attributs aus einem XML-Element.

```text-x-trilium-auto
<XMLGetAttribute Document="{@myXml}" Data="" Path="" Attribute="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, aus dem das Attribut gelesen wird.
*   **Data**: Variable, die das Element enthält.
*   **Path**: (Optional) XPath-Pfad zum gewünschten Element.
*   **Attribute**: Name des Attributs.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLSetAttribute
---------------

Setzt den Wert eines Attributs in einem XML-Element.

```text-x-trilium-auto
<XMLSetAttribute Document="{@myXml}" Data="" Path="" Attribute="" Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, das bearbeitet wird.
*   **Data**: Variable, die das Element enthält.
*   **Path**: XPath-Pfad zum Ziel-Element.
*   **Attribute**: Name des Attributs.
*   **Value**: Wert, der für das Attribut gesetzt werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLRemoveAttribute
------------------

Entfernt ein Attribut aus einem XML-Element.

```text-x-trilium-auto
<XMLRemoveAttribute Document="{@myXml}" Data="" Path="" Attribute="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, aus dem das Attribut entfernt wird.
*   **Data**: Variable, die das Element enthält.
*   **Path**: XPath-Pfad zum Ziel-Element.
*   **Attribute**: Name des zu entfernenden Attributs.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLGetDocumentContent
---------------------

Liest den gesamten Inhalt eines XML-Dokuments als Zeichenkette.

```text-x-trilium-auto
<XMLGetDocumentContent Document="{@myXml}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, dessen Inhalt ausgelesen wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Variable, in der der gesamte XML-Inhalt als Zeichenkette gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLGetElementContent
--------------------

Liest den Inhalt eines bestimmten XML-Elements.

```text-x-trilium-auto
<XMLGetElementContent Document="{@myXml}" Data="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, dessen Inhalt ausgelesen wird.
*   **Data**: Variable, die das Ziel-Element enthält.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Variable, in der der Inhalt des Elements gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XMLSetElementContent
--------------------

Setzt den Inhalt eines XML-Elements.

```text-x-trilium-auto
<XMLSetElementContent Document="{@myXml}" Data="" Content="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: XML-Dokument, in dem das Element bearbeitet wird.
*   **Data**: Variable, die das Ziel-Element enthält.
*   **Content**: Neuer Inhalt des Elements.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

XML
---

Der Tag XML bietet die Möglichkeit direkt in dem Batchpad-Skript ein XML-Dokument zu hinterlegen. Das Dokument kann anschließend in der Form {@XML:Test} angesprochen werden. Wobei in dem Beispiel die Zeichenfolge "Test" dem Attribut Name entsprechen muss.

```text-x-trilium-auto
<XML Name="">

</XML>
```

JSONConvertToXML
----------------

Wandelt ein JSON-Dokument in ein XML-Dokument um.

```text-x-trilium-auto
<JSONConvertToXML Document="{@myXml}" Json="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Document**: Variable, in der das konvertierte XML-Dokument gespeichert wird.
*   **Json**: JSON-Inhalt, der umgewandelt werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

JSONGetValue
------------

Liest einen Wert aus einem JSON-Dokument basierend auf einem Pfad.

```text-x-trilium-auto
<JSONGetValue Json="{@myJson}" Path="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Json**: JSON-Dokument, aus dem der Wert gelesen wird.
*   **Path**: Pfad zum gewünschten Wert im JSON-Dokument.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Variable, in der der Wert gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

JSONGetValueList
----------------

Liest mehrere Werte aus einem JSON-Dokument in eine Liste.

```text-x-trilium-auto
<JSONGetValueList Data="{@myData}" Json="{@myJson}" Path="" Recursiv="false" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die gefundenen Werte gespeichert werden.
*   **Json**: JSON-Dokument, das analysiert wird.
*   **Path**: Pfad zu den gewünschten Werten.
*   **Recursiv**: Ob rekursiv gesucht werden soll (true oder false).
*   **DataCount**: (Optional) Variable, in der die Anzahl der gefundenen Werte gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

JSONGetDataTable
----------------

Wandelt JSON-Daten in eine Datentabelle um.

```text-x-trilium-auto
<JSONGetDataTable Data="{@myData}" Json="{@myJson}" Path="" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Datentabelle gespeichert wird.
*   **Json**: JSON-Dokument, das konvertiert wird.
*   **Path**: Pfad zu den Daten im JSON-Dokument.
*   **DataCount**: (Optional) Variable, die die Anzahl der erstellten Tabellenzeilen speichert.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

ConvertDataTableToJSON
----------------------

Wandelt eine Datentabelle in ein JSON-Dokument um.

```text-x-trilium-auto
<ConvertDataTableToJSON Data="{@myData}" Json="{@myJson}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Datentabelle, die konvertiert werden soll.
*   **Json**: Variable, in der das erstellte JSON-Dokument gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

ConvertJSONToDataTable
----------------------

Wandelt ein JSON-Dokument in eine Datentabelle um.

```text-x-trilium-auto
<ConvertJSONToDataTable Data="{@myData}" Json="{@myJson}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Datentabelle gespeichert wird.
*   **Json**: JSON-Dokument, das umgewandelt wird.
*   **DataCount**: (Optional) Variable, die die Anzahl der erstellten Tabellenzeilen speichert.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.