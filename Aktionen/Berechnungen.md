# Berechnungen
CalculateAddition
-----------------

Die Aktion **CalculateAddition** addiert die Werte der Attribute **Value1** und **Value2** und speichert das Ergebnis in der angegebenen Variablen. Über das Attribut **Float** kann festgelegt werden, ob das Ergebnis als Fließkommazahl zurückgegeben wird.

```text-x-trilium-auto
<CalculateAddition Value1="" Value2="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Erster Summand.
*   **Value2**: Zweiter Summand.
*   **Float** (optional, Standard: false): Gibt an, ob das Ergebnis als Fließkommazahl zurückgegeben wird.
*   **Condition** (optional): Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError** (optional, Standard: false): Gibt an, ob Fehler ignoriert werden sollen.

Beispiel:

```text-x-trilium-auto
<CalculateAddition Value1="5" Value2="3" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird **5** **\+ 3** berechnet, und das Ergebnis **8** wird in der Variablen **{@Result}** gespeichert.

CalculateSubtraction
--------------------

Die Aktion **CalculateSubtraction** subtrahiert **Value2** von **Value1** und speichert das Ergebnis in der angegebenen Variablen. Über das Attribut **Float** kann festgelegt werden, ob das Ergebnis als Fließkommazahl zurückgegeben wird.

```text-x-trilium-auto
<CalculateSubtraction Value1="" Value2="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Minuend.
*   **Value2**: Subtrahend.
*   **Float** (optional, Standard: false): Gibt an, ob das Ergebnis als Fließkommazahl zurückgegeben wird.
*   **Condition** (optional): Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError** (optional, Standard: false): Gibt an, ob Fehler ignoriert werden sollen.

Beispiel:

```text-x-trilium-auto
<CalculateSubtraction Value1="10" Value2="4" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird **10 - 4** berechnet, und das Ergebnis **6** wird in der Variablen **{@Result}** gespeichert.

CalculateMultiplication
-----------------------

Die Aktion **CalculateMultiplication** multipliziert die Werte der Attribute **Value1** und **Value2** und speichert das Ergebnis in der angegebenen Variablen. Über das Attribut **Float** kann festgelegt werden, ob das Ergebnis als Fließkommazahl zurückgegeben wird.

```text-x-trilium-auto
<CalculateMultiplication Value1="" Value2="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Erster Faktor.
*   **Value2**: Zweiter Faktor.
*   **Float** (optional, Standard: false): Gibt an, ob das Ergebnis als Fließkommazahl zurückgegeben wird.
*   **Condition** (optional): Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError** (optional, Standard: false): Gibt an, ob Fehler ignoriert werden sollen.

Beispiel:

```text-x-trilium-auto
<CalculateMultiplication Value1="7" Value2="6" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird **7 \* 6** berechnet, und das Ergebnis **42** wird in der Variablen **{@Result}** gespeichert.

CalculateDivision
-----------------

Die Aktion **CalculateDivision** dividiert **Value1** durch **Value2** und speichert das Ergebnis in der angegebenen Variablen. Über das Attribut **Float** kann festgelegt werden, ob das Ergebnis als Fließkommazahl zurückgegeben wird.

```text-x-trilium-auto
<CalculateDivision Value1="" Value2="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Dividend.
*   **Value2**: Divisor.
*   **Float** (optional, Standard: false): Gibt an, ob das Ergebnis als Fließkommazahl zurückgegeben wird.
*   **Condition** (optional): Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError** (optional, Standard: false): Gibt an, ob Fehler ignoriert werden sollen.

Beispiel:

```text-x-trilium-auto
<CalculateDivision Value1="20" Value2="4" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird **20 / 4** berechnet, und das Ergebnis **5** wird in der Variablen **{@Result}** gespeichert.

CalculateMax
------------

Die Aktion **CalculateMax** ermittelt den maximalen Wert zwischen **Value1** und **Value2** und speichert diesen in der angegebenen Variablen.

```text-x-trilium-auto
<CalculateMax Value1="" Value2="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Erster Wert.
*   **Value2**: Zweiter Wert.
*   **Condition** (optional): Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError** (optional, Standard: false): Gibt an, ob Fehler ignoriert werden sollen.

Beispiel:

```text-x-trilium-auto
<CalculateMax Value1="15" Value2="25" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird der maximale Wert zwischen **15** und **25** ermittelt, und das Ergebnis **25** wird in der Variablen **{@Result}** gespeichert.

CalculateMin
------------

Die Aktion **CalculateMin** vergleicht zwei Zahlen und gibt den kleineren der beiden Werte zurück. Das Ergebnis wird in der im Attribut **Variable** angegebenen Variablen gespeichert.

```text-x-trilium-auto
<CalculateMin Value1="" Value2="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value1**: Die erste Zahl, die verglichen werden soll.
*   **Value2**: Die zweite Zahl, die verglichen werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<CalculateMin Value1="10" Value2="20" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Von den beiden Werten **10** und **20** wird der kleinere Wert **10** ermittelt und in der Variablen **{@Result}** gespeichert.

ConvertToNumber
---------------

Die Aktion **ConvertToNumber** konvertiert eine Zeichenfolge in eine Zahl und gibt entweder eine ganze Zahl oder eine Fließkommazahl zurück. Das Ergebnis wird in der im Attribut **Variable** angegebenen Variablen gespeichert.

```text-x-trilium-auto
<ConvertToNumber Value="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zeichenfolge, die in eine Zahl umgewandelt werden soll.
*   **Float**: (Optional) Gibt an, ob der Rückgabewert eine Fließkommazahl sein soll. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<ConvertToNumber Value="42.5" Float="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Die Zeichenfolge **"42.5"** wird in die Fließkommazahl **42.5** umgewandelt und in der Variablen **{@Result}** gespeichert.

MathAbs
-------

Die Aktion **MathAbs** berechnet den absoluten Wert einer Zahl und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<MathAbs Value="" Float="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zahl, deren absoluter Wert berechnet werden soll.
*   **Float**: (Optional) Gibt an, ob die Zahl eine Fließkommazahl ist. Standardwert: false.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<MathAbs Value="-15.7" Float="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Der absolute Wert von **\-15.7** ist **15.7.** Dieser Wert wird in der Variablen **{@Result}** gespeichert.

MathTruncate
------------

Die Aktion **MathTruncate** gibt den ganzzahligen Teil einer Dezimalzahl zurück und speichert das Ergebnis in der im Attribut **Variable** angegebenen Variablen.

```text-x-trilium-auto
<MathTruncate Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Dezimalzahl, deren ganzzahliger Teil berechnet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<MathTruncate Value="12.89" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Der ganzzahlige Teil von **12.89** ist **12**. Dieser Wert wird in der Variablen **{@Result}** gespeichert.

MathRound
---------

Die Aktion **MathRound** rundet einen Dezimalwert auf die nächstgelegene ganze Zahl und rundet Mittelpunktwerte auf die nächstgelegene gerade Zahl. Das Ergebnis wird in der angegebenen Variablen gespeichert.

```text-x-trilium-auto
<MathRound Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zahl, die gerundet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<MathRound Value="2.5" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Die Zahl **2.5** wird auf die nächste gerade Zahl gerundet, also **2**. Dieser Wert wird in der Variablen **{@Result}** gespeichert.

MathFloor
---------

Die Aktion **MathFloor** gibt die größte Ganzzahl zurück, die kleiner oder gleich der angegebenen Zahl ist. Das Ergebnis wird in der angegebenen Variablen gespeichert.

```text-x-trilium-auto
<MathFloor Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zahl, die abgerundet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<MathFloor Value="5.9" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Die Zahl **5.9** wird auf **5** abgerundet und in der Variablen **{@Result}** gespeichert.

MathCeiling
-----------

Die Aktion **MathCeiling** gibt die kleinste Ganzzahl zurück, die größer oder gleich der angegebenen Zahl ist. Das Ergebnis wird in der angegebenen Variablen gespeichert.

```text-x-trilium-auto
<MathCeiling Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Die Zahl, die aufgerundet werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<MathCeiling Value="5.1" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Die Zahl **5.1** wird auf **6** aufgerundet und in der Variablen **{@Result}** gespeichert.