# Zeichenketten
StringLeft
----------

Die Aktion **StringLeft** extrahiert die ersten N Zeichen aus einer angegebenen Zeichenfolge und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringLeft Value="" Length="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, aus der die Teilzeichenfolge extrahiert werden soll.
*   **Length**: Die Anzahl der zu extrahierenden Zeichen von links.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Extraktion gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringLeft Value="Beispieltext" Length="7" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird aus der Zeichenfolge Beispieltext die Teilzeichenfolge **Beispie** extrahiert, bestehend aus den ersten sieben Zeichen. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringMid
---------

Die Aktion **StringMid** extrahiert eine Teilzeichenfolge aus einer angegebenen Zeichenfolge. Die extrahierte Teilzeichenfolge wird in der im Attribut **Variable** angegebenen Variablen gespeichert.

```text-x-trilium-auto
<StringMid Value="" Start="" Length="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, aus der die Teilzeichenfolge extrahiert werden soll.
*   **Start**: Die Startposition der Extraktion, angegeben als ganze Zahl. Zählung beginnt bei 1.
*   **Length**: Die Anzahl der zu extrahierenden Zeichen.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Extraktion gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringMid Value="Beispieltext" Start="2" Length="5" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird aus der Zeichenfolge Beispieltext die Teilzeichenfolge **eispi** extrahiert, beginnend bei der zweiten Position und mit einer Länge von fünf Zeichen. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringRight
-----------

Die Aktion **StringRight** extrahiert die letzten N Zeichen aus einer angegebenen Zeichenfolge und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringRight Value="" Length="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, aus der die Teilzeichenfolge extrahiert werden soll.
*   **Length**: Die Anzahl der zu extrahierenden Zeichen von rechts.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Extraktion gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringRight Value="Beispieltext" Length="4" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird aus der Zeichenfolge **Beispieltext** die Teilzeichenfolge **text** extrahiert, bestehend aus den letzten vier Zeichen. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringLength
------------

Die Aktion **StringLength** ermittelt die Anzahl der Zeichen in einer angegebenen Zeichenfolge und speichert das Ergebnis als ganze Zahl in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringLength Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, deren Länge ermittelt werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der die Länge der Zeichenfolge gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringLength Value="Beispieltext" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Länge der Zeichenfolge **Beispieltext** ermittelt, die **12** Zeichen beträgt. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringReplace
-------------

Die Aktion **StringReplace** ersetzt alle Vorkommen einer bestimmten Teilzeichenfolge in einer angegebenen Zeichenfolge durch eine andere Teilzeichenfolge und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringReplace Value="" Search="" Replace="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die ursprüngliche Zeichenfolge, in der die Ersetzungen vorgenommen werden sollen.
*   **Search**: Die Teilzeichenfolge, die ersetzt werden soll.
*   **Replace**: Die Teilzeichenfolge, die als Ersatz verwendet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Ersetzung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringReplace Value="Hallo Welt" Search="Welt" Replace="Universum" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird in der Zeichenfolge **Hallo Welt** das Wort **Welt** durch **Universum** ersetzt, sodass das Ergebnis **Hallo Universum** lautet. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringContains
--------------

Die Aktion **StringContains** überprüft, ob eine bestimmte Teilzeichenfolge in einer angegebenen Zeichenfolge enthalten ist, und gibt **true** oder **false** zurück. Das Ergebnis wird in der im Attribut **Variable** angegebenen Variablen gespeichert.

Attribute:

*   **Value**: Die Zeichenfolge, die durchsucht werden soll.
*   **Search**: Die Teilzeichenfolge, nach der gesucht wird.
*   **Not**: (Optional) Wenn auf true gesetzt, wird das Ergebnis negiert. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Überprüfung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringContains Value="Hallo Welt" Search="Welt" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird überprüft, ob die Teilzeichenfolge **Welt** in der Zeichenfolge **Hallo Welt** enthalten ist. Da dies der Fall ist, wird **true** in der Variable **{@Result}** gespeichert.

StringIndexOf
-------------

Die Aktion **StringIndexOf** ermittelt die Position des ersten Vorkommens einer bestimmten Teilzeichenfolge in einer angegebenen Zeichenfolge und speichert die Position als ganze Zahl in der im Attribut **Variable** angegebenen Variablen. Die Zählung beginnt bei **1**. Wenn die angegebene Zeichenfolge nicht gefunden wird bekommt man die Zahl **0** als Ergebnis zurück.

```text-x-trilium-auto
<StringIndexOf Value="" Search="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, die durchsucht werden soll.
*   **Search**: Die Teilzeichenfolge, deren Position ermittelt werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der die Position der Teilzeichenfolge gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringIndexOf Value="Hallo Welt" Search="Welt" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Position des ersten Vorkommens der Teilzeichenfolge **Welt** in der Zeichenfolge **Hallo Welt** ermittelt. Da Welt an der Position 7 beginnt, wird **7** in der Variable **{@Result}** gespeichert.

StringStartsWith
----------------

Die Aktion **StringStartsWith** prüft, ob eine Zeichenfolge mit einer bestimmten Teilzeichenfolge beginnt, und speichert das Ergebnis (**true** oder **false**) in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringStartsWith Value="" Search="" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die zu prüfende Zeichenfolge.
*   **Search**: Die Teilzeichenfolge, die am Anfang der Zeichenfolge erwartet wird.
*   **Not**: (Optional) Negiert das Ergebnis der Prüfung. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Prüfung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringStartsWith Value="Hallo Welt" Search="Hallo" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird geprüft, ob die Zeichenfolge **Hallo Welt** mit **Hallo** beginnt. Da dies der Fall ist, wird das Ergebnis **true** in der Variablen **{@Result}** gespeichert.

StringEndsWith
--------------

Die Aktion **StringEndsWith** prüft, ob eine Zeichenfolge mit einer bestimmten Teilzeichenfolge endet, und speichert das Ergebnis (**true** oder **false**) in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringEndsWith Value="" Search="" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die zu prüfende Zeichenfolge.
*   **Search**: Die Teilzeichenfolge, die am Ende der Zeichenfolge erwartet wird.
*   **Not**: (Optional) Negiert das Ergebnis der Prüfung. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Prüfung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringEndsWith Value="Hallo Welt" Search="Welt" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird geprüft, ob die Zeichenfolge **Hallo Welt** mit **Welt** endet. Da dies der Fall ist, wird das Ergebnis **true** in der Variablen **{@Result}** gespeichert.

StringToLower
-------------

Die Aktion **StringToLower** konvertiert alle Buchstaben einer angegebenen Zeichenfolge in Kleinbuchstaben und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringToLower Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, die in Kleinbuchstaben umgewandelt werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der die umgewandelte Zeichenfolge gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringToLower Value="Hallo Welt" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Zeichenfolge **Hallo Welt** in **hallo welt** umgewandelt. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringToUpper
-------------

Die Aktion **StringToUpper** konvertiert alle Buchstaben einer angegebenen Zeichenfolge in Großbuchstaben und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringToUpper Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute

*   **Value**: Die Zeichenfolge, die in Großbuchstaben umgewandelt werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der die umgewandelte Zeichenfolge gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel

```text-x-trilium-auto
<StringToUpper Value="Hallo Welt" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Zeichenfolge **Hallo Welt** in **HALLO WELT** umgewandelt. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringTrim
----------

Die Aktion **StringTrim** entfernt führende und/oder nachfolgende Leerzeichen aus einer angegebenen Zeichenfolge und speichert das bereinigte Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringTrim Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, die bereinigt werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der die bereinigte Zeichenfolge gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringTrim Value="   Hallo Welt   " Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Zeichenfolge    **Hallo Welt**    bereinigt, sodass das Ergebnis **Hallo Welt** lautet. Das Ergebnis wird in der Variable **{@Result}** gespeichert.

StringFormat
------------

Die Aktion **StringFormat** formatiert eine Zeichenfolge basierend auf einem angegebenen Formatausdruck und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen. Der Formatausdruck kann Platzhalter (**{0}**, **{1}**, ...) enthalten, die durch Werte ersetzt werden.

```text-x-trilium-auto
<StringFormat Value="" Format="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die ursprüngliche Zeichenfolge, die formatiert werden soll.
*   **Format**: Der Formatausdruck, der verwendet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Formatierung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel 1: Einfacher Platzhalter

```text-x-trilium-auto
<StringFormat Value="Hallo" Format="{0} Welt" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird der Platzhalter **{0}** durch den Wert **Hallo** ersetzt. Das Ergebnis **Hallo Welt** wird in der Variablen **{@Result}** gespeichert.

Beispiel 2: Mehrere Platzhalter

```text-x-trilium-auto
<StringFormat Value="Welt,2024" Format="Hallo {0}, das Jahr ist {1}!" Variable="{@Result}" IgnoreError="false" />
```

Hier wird die Zeichenfolge **Welt,2024** verwendet. Die Werte werden automatisch auf die Platzhalter **{0}** und **{1}** abgebildet. **Hallo Welt, das Jahr ist 2024!** wird in der Variablen **{@Result}** gespeichert.

Beispiel 3: Formatierung von Zahlen

```text-x-trilium-auto
<StringFormat Value="1234.567" Format="Der Wert beträgt {0:F2}" Variable="{@Result}" IgnoreError="false" />
```

**{0:F2}** formatiert den Wert als Fließkommazahl mit 2 Dezimalstellen. Das Ergebnis lautet dann **1234,57**.

Beispiel 4: Datum formatieren

```text-x-trilium-auto
<StringFormat Value="2024-06-16" Format="Das Datum ist {0:yyyy/MM/dd}" Variable="{@Result}" IgnoreError="false" />
```

Formatiert das angegebene Datum **2024-06-16** in das Ergebnis **Das Datum ist 2024/06/16**.

Diese zusätzlichen Beispiele zeigen, wie flexibel **StringFormat** ist, insbesondere in Kombination mit Zahlen-, Datums- oder mehrteiligen Zeichenfolgen.

StringAppend
------------

Die Aktion **StringAppend** verknüpft zwei Zeichenfolgen miteinander und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen. Optional kann ein Zeilenumbruch zwischen den Zeichenfolgen eingefügt werden.

```text-x-trilium-auto
<StringAppend Value1="" Value2="" NewLine="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Die erste Zeichenfolge, die verknüpft werden soll.
*   **Value2**: Die zweite Zeichenfolge, die verknüpft werden soll.
*   **NewLine**: (Optional) Gibt an, ob zwischen den Zeichenfolgen ein Zeilenumbruch eingefügt werden soll. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Verknüpfung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringAppend Value1="Hallo" Value2="Welt" NewLine="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Das Ergebnis **HalloWelt** wird in der Variablen **{@Result}** gespeichert.

StringEmpty
-----------

Die Aktion **StringEmpty** prüft, ob eine Zeichenfolge leer ist, und speichert das Ergebnis (**true** oder **false**) in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringEmpty Value="" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die zu prüfende Zeichenfolge.
*   **Not**: (Optional) Negiert das Ergebnis der Prüfung. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Prüfung gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringEmpty Value="Test" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird geprüft, ob die Zeichenfolge **Test** leer ist. Da dies nicht der Fall ist, wird das Ergebnis **false** in der Variablen **{@Result}** gespeichert.

StringSplit
-----------

Die Aktion **StringSplit** teilt eine Zeichenfolge basierend auf einem Trennzeichen oder Zeilenumbruch in mehrere Teilzeichenfolgen und speichert diese in dem Attribut **Data** angegebenen Datenobjekt. Über das Datenobjekt kann anschließend über eine ForEach Schleife iteriert werden (Siehe: Allgemein/ForEach).

```text-x-trilium-auto
<StringSplit Data="{@myData}" Value="" Delimiter=";" SplitLines="false" RemoveEmptyValues="false" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die zu teilende Zeichenfolge.
*   **Delimiter**: Das Trennzeichen, anhand dessen die Zeichenfolge geteilt wird.
*   **SplitLines**: (Optional) Gibt an, ob die Zeichenfolge an Zeilenumbrüchen aufgeteilt werden soll. Standardwert: false.
*   **RemoveEmptyValues**: (Optional) Gibt an, ob leere Einträge verworfen werden sollen. Standardwert: false.
*   **Data**: Die Variable, in der das Datenobjekt mit den Teilzeichenfolgen gespeichert wird.
*   **DataCount**: (Optional) Die Anzahl der Teilzeichenfolgen im Datenobjekt.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringSplit Value="a,b,c" Delimiter="," SplitLines="false" RemoveEmptyValues="true" Data="{@myData}" DataCount="{@ResultCount}" Condition="" IgnoreError="false" />
```

In diesem Beispiel wird die Zeichenfolge **a,b,c** am Trennzeichen **,** geteilt, sodass das Datenobjekt **{@myData}** die Werte **a**, **b** und **c** enthält. Die Anzahl der Elemente (**3**) wird in der Variablen **{@ResultCount}** gespeichert.

StringBetween
-------------

Die Aktion **StringBetween** extrahiert eine Teilzeichenfolge, die zwischen zwei bestimmten Zeichenfolgen liegt, und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<StringBetween Value="" StartText="" EndText="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die ursprüngliche Zeichenfolge, aus der die Teilzeichenfolge extrahiert werden soll.
*   **StartText**: Die Anfangszeichenfolge, nach der gesucht wird.
*   **EndText**: Die Endzeichenfolge, nach der gesucht wird.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis der Extraktion gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<StringBetween Value="Hallo [Welt]!" StartText="[" EndText="]" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird aus der Zeichenfolge **Hallo \[Welt\]!** die Teilzeichenfolge **Welt** extrahiert und in der Variablen **{@Result}** gespeichert.