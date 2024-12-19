# Syntax
Aufbau des Skripts
------------------

Das Skript muss ein Stammelement enthalten, das allen anderen Elemente übergeordnet ist. Für die Syntax des Batchpad ist dies der Batch-Tag:

```text-x-trilium-auto
<Batch ActionLog="true" ConditionLog="false">
...
</Batch>
```

Alle weiteren verfügbaren Tags müssen in diesem Stammelement verschachtelt werden.

Hinweis: Über die Attribute **ActionLog** und **ConditionLog** kann die Ausgabe in das Protokoll im Ausgabefenster gesteuert werden.

Tags
----

Analog zu der XML-Syntax werden diese Elemente, wie z.B. das Stammelement "<Batch>" auch Tags genannt.

Dabei ist "<Batch>" der öffnende Tag und "</Batch>" der schließende Tag.

Ein Tag muss immer geschlossen werden. Wenn kein weiteres Tag in einem Tag verschachtelt werden soll kann auch das öffnende Tag durch ein Slash (/) am Ende des öffnenden Tags geschlossen werden:

```text-x-trilium-auto
<Print Text="Hello World!" Variable="{@Result}" />
```

Innerhalb von dem Batch-Tag können weitere Tags, wie z.B. der Print-Tag verschachtelt werden:

```text-x-trilium-auto
<Batch ActionLog="true" ConditionLog="false"> 
    <Print Text="Hello World!" Variable="{@Result}" /> 
</Batch>
```

Es werden nur die Tags die das Batchpad zur Verfügung stellt verarbeitet. Text in Tag-Elemente zu verschachteln wird nicht unterstützt und kann zu Fehlern führen. Für Anmerkungen innerhalb des Batchpads siehe Abschnitt Kommentare.

Die Tags entsprechen den Aktionen die das Batchpad bei der Ausführung des Skriptes durchführen soll.

Hinweis: Im Normalfall werden die Aktionen über den Bereich "Aktionen & Parameter" oder über die Autovervollständigung hinzugefügt. Das Hinzufügen von vorgefertigten Tags erleichtert die Einhaltung der Syntax-Regeln.

Attribute
---------

Innerhalb eines öffnenden Tags können Attribute verwendet werden:

```text-x-trilium-auto
<Print Text="Hello World!" Variable="{@Result}" />
```

In dem Beispiel sind die Attribute **Text** und **Variable** angegeben. Die Werte des Attributs müssen innerhalb von zwei Anführungszeichen ("...") stehen.

Allgemeine Attribute
--------------------

Die allgemeinen Attribute **IgnoreError**, **Variable** und **Condition** können bei allen Tags bzw. Aktionen angegeben werden. Die Attribute sind optional und brauchen nur bei Bedarf hinterlegt werden. Wenn diese für eine Aktion nicht benötigt werden, können diese aber auch zur besseren Lesbarkeit des Skriptes entfernt werden.

### IgnoreError

Das optionale Attribut **IgnoreError** gibt an, ob bei einem Fehler die Ausführung des Batchpad Skriptes abbricht oder das Skript weiter ausgeführt werden soll. Der Wert muss dem Typ Boolean (true oder false) entsprechen.

```text-x-trilium-auto
Beispiel: IgnoreError="true" 
```

### Variable

Das optionale Attribut **Variable** kann immer dann verwendet werden, wenn man das Ergebnis einer auszuführenden Aktion ermitteln möchte.

```text-x-trilium-auto
Beispiel: Variable="{@ResultFileExists}"
```

Die Ergebnisse sind je nach ausgeführter Aktion vom Typ her unterschiedlich, oft ist es ein Boolean (true oder false) der angibt ob die Aktion erfolgreich war. Bei Aktionen für Zeichenketten sind die Ergebnisse dann meistens vom Typ String und bei Berechnungen dann vom Typ Integer oder Double usw.  
 

### Condition

Das optionale Attribut **Condition** gibt an, ob die Aktion ausgeführt werden soll. Hierzu wird der Inhalt des Attributes als logischer Ausdruck auf Wahr oder Falsch geprüft. Der Ausdruck sollte dem Typ Boolean (true oder false) entsprechen.  
Der Ausdruck kann auch logische Operatoren wie NOT, AND, OR und XOR auswerten.  
Mit dem Condition Attribut wertet man in der Regel Variablen aus, die Ergebnisse aus zuvor durchgeführten Aktionen enthalten. 

```text-x-trilium-auto
Beispiel: Condition="NOT {@ResultFileExists}"
```

Variablen und Parameter
-----------------------

Innerhalb von Attributen können Variablen und Parameter verwendet werden. Wie Beispielsweise die Variable **{@Result}** in folgendem Beispiel:

```text-x-trilium-auto
<CalculateAddition Value1="" Value2="" Float="false" Variable="{@Result}" />
```

Variablen und Parameter werden über die gleiche Syntax eingebunden. Parameter werden von dem Batchpad verwaltet (siehe Seite Hauptmenü), Variablen werden innerhalb des Skripts über die Aktion <Set Variable="" Value="" /> gesetzt:

```text-x-trilium-auto
<Batch>
    <Set Variable="{@TestVariable}" Value="Test Wert" />
    <Print Text="{@TestVariable}" />
</Batch>

<!-- Ausgabe: "Test Wert" -->
```

Darüber hinaus gibt es Variablen die von den jeweiligen Aktionen bereitgestellt werden sowie Zugriffsmöglichkeiten auf die Werte von Objekten.

Wie diese Variablen eingesetzt werden ist auf den Seiten unter **Aktionen** zu der jeweiligen Aktion dokumentiert. 

Beispielsweise stellt die ForEach Schleife eine Variable **{@Data:**…**}** für die Daten aus dem {@myData} Objekt zur Verfügung:

```text-x-trilium-auto
    <SQLReadData Data="{@myData}" Query="SELECT Bezeichnung FROM Artikel" Connection="{@myConnection}" />
        <ForEach Data="{@myData}">
            <Print Text="{@Data:Bezeichnung}" />
        </ForEach>
...
```

Kommentare
----------

Kommentare werden XML-typisch wie folgt geschrieben: 

**<!-- Das ist ein Kommentar -->** 

Kommentare können in Tags verschachtelt werden oder auch außerhalb von dem Stammelement "<Batch>" platziert werden.

Nicht erlaubt sind zwei Striche innerhalb von einem Kommentar wie z.B. 

**<!-- Das ist ein nicht erlaubter -- Kommentar-->**

Sonderzeichen
-------------

Die Sonderzeichen < > und & können nicht verwendet werden. Hierzu müssen diese Sonderzeichen gegen ein Ersetzungszeichen getauscht werden.  Es können sowohl die XML als auch die Batchpad eigenen Ersetzungszeichen verwendet werden. Es gibt folgende vordefinierte Ersetzungszeichen.

|     |     |     |     |
| --- | --- | --- | --- |
| **Bedeutung** | **Zeichen** | **XML Ersetzungszeichen** | **Batchpad Ersetzungszeichen** |
| Kleiner als | <   | &lt; | \[\*l\] |
| Größer als | \>  | &gt; | \[\*g\] |
| Ampersand | &   | &amp; | \[\*a\] |
| Anführungszeichen | "   | &quot; | \[\*q\] |
| Tabulator |     | &#09; | \[\*t\] |
| Zeilenumbruch |     | &#13;&#10; | \[\*n\] |

Zum Beispiel erzeugt die Aktion Print:

```text-x-trilium-auto
<Print Text="[*l]Hello[*g] [*t]World![*n][*a]Neue Zeile" Variable="{@Result}" />
```

folgende Ausgabe im Ausgabefenster:

```text-x-trilium-auto
<Hello>     World! 
&Neue Zeile
```