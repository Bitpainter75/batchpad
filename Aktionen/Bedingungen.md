# Bedingungen
ConditionTrue
-------------

Mit der Aktion **ConditionTrue** wird geprüft, ob die Bedingung in dem Attribut Condition zutrifft. Falls ja werden die in ConditionTrue verschachtelten Aktionen ausgeführt.

Hinweis: Der Wert in dem Attribut Condition wird als Boolean (true/false) ausgewertet, hier stehen auch die logischen Operatoren NOT, AND, OR und XOR zur Verfügung.

```text-x-trilium-auto
<ConditionTrue Condition="" IgnoreError="false">
...
</ConditionTrue>
```

ConditionBetween
----------------

Die Aktion **ConditionBetween** prüft, ob der Wert in dem Attribut Value zwischen den Werten in MinValue und MaxValue liegt. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionBetween verschachtelt werden.

```text-x-trilium-auto
<ConditionBetween Value="" MinValue="" MaxValue="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionBetweenOrEqualTo
-------------------------

Die Aktion **ConditionBetweenOrEqualTo** prüft, ob der Wert in dem Attribut Value zwischen den Werten MinValue und MaxValue liegt. Zusätzlich wird geprüft, ob der Wert Value dem Wert MinValue oder MaxValue entspricht. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionBetweenOrEqualTo verschachtelt werden.

```text-x-trilium-auto
<ConditionBetweenOrEqualTo Value="" MinValue="" MaxValue="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionEqualTo
----------------

Die Aktion **ConditionEqualTo** prüft, ob der Wert von dem Attribut Value1 dem Wert von dem Attribut Value2 entspricht. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionEqualTo verschachtelt werden.

```text-x-trilium-auto
<ConditionEqualTo Value1="" Value2="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionGreaterThan
--------------------

Die Aktion **ConditionGreaterThan** prüft, ob der Wert von Value1 größer als der Wert von Value2 ist. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionGreaterThan verschachtelt werden.

```text-x-trilium-auto
<ConditionGreaterThan Value1="" Value2="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionGreaterThanOrEqualTo
-----------------------------

Die Aktion **ConditionGreaterThanOrEqualTo** prüft, ob der Wert von Value1 größer oder gleich Value2 ist. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionGreaterThanOrEqualTo verschachtelt werden.

```text-x-trilium-auto
<ConditionGreaterThanOrEqualTo Value1="" Value2="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionLessThan
-----------------

Die Aktion **ConditionLessThan** prüft, ob der Wert von Value1 kleiner als Value2 ist. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionLessThan verschachtelt werden.

```text-x-trilium-auto
<ConditionLessThan Value1="" Value2="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionLessThanOrEqualTo
--------------------------

Die Aktion **ConditionLessThanOrEqualTo** prüft, ob der Wert von Value1 kleiner oder gleich Value2 ist. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionLessThanOrEqualTo verschachtelt werden.

```text-x-trilium-auto
<ConditionLessThanOrEqualTo Value1="" Value2="" Numeric="false" Not="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConditionIsEmpty
----------------

Die Aktion **ConditionIsEmpty** prüft, ob der Wert von Value leer bzw. nicht definiert ist. Die Aktion gibt das Ergebnis über das Attribut Variable zurück. Und wenn die Bedingung zutrifft können alle Aktionen ausführt werden, die in ConditionIsEmpty verschachtelt werden.

```text-x-trilium-auto
<ConditionIsEmpty Value="" Variable="{@Result}" />
```