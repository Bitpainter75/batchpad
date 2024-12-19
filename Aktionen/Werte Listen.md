# Werte Listen
KeyValueListAdd
---------------

Die Aktion **KeyValueListAdd** fügt ein Schlüssel-Wert-Paar zu einer bestehenden Key-Value-Liste hinzu.

```text-x-trilium-auto
<KeyValueListAdd Data="{@myList}" Key="" Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Key-Value-Liste, zu der das neue Paar hinzugefügt wird.
*   **Key**: Der Schlüssel des neuen Eintrags.
*   **Value**: Der Wert, der dem Schlüssel zugeordnet wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KeyValueListAdd Data="{@myList}" Key="Username" Value="MaxMustermann" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Fügt der Key-Value-Liste **{@myList}** ein Paar hinzu, bei dem **Username** der Schlüssel und **MaxMustermann** der Wert ist.

KeyValueListGet
---------------

Die Aktion **KeyValueListGet** liest den Wert eines bestimmten Schlüssels aus einer Key-Value-Liste.

```text-x-trilium-auto
<KeyValueListGet Data="{@myList}" Key="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Key-Value-Liste, aus der der Wert gelesen wird.
*   **Key**: Der Schlüssel, dessen Wert abgerufen werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in die der Wert gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KeyValueListGet Data="{@myList}" Key="Username" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest den Wert zum Schlüssel **Username** aus der Key-Value-Liste **{@myList}** und speichert ihn in der Variable **{@Result}**.

KeyValueListRemove
------------------

Die Aktion **KeyValueListRemove** entfernt einen Eintrag mit einem bestimmten Schlüssel aus der Key-Value-Liste.

```text-x-trilium-auto
<KeyValueListRemove Data="{@myList}" Key="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Key-Value-Liste, aus der der Eintrag entfernt wird.
*   **Key**: Der Schlüssel des zu entfernenden Eintrags.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KeyValueListRemove Data="{@myList}" Key="Username" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Entfernt den Eintrag mit dem Schlüssel **Username** aus der Key-Value-Liste **{@myList}**.

KeyValueListClear
-----------------

Die Aktion **KeyValueListClear** löscht alle Einträge aus der Key-Value-Liste.

```text-x-trilium-auto
<KeyValueListClear Data="{@myList}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Key-Value-Liste, die geleert werden soll.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KeyValueListClear Data="{@myList}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht alle Einträge aus der Key-Value-Liste **{@myList}**.

KeyValueListToUrlEscapedString
------------------------------

Die Aktion **KeyValueListToUrlEscapedString** wandelt die Einträge einer Key-Value-Liste in eine URL-escaped Zeichenkette um.

```text-x-trilium-auto
<KeyValueListToUrlEscapedString Data="{@myList}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Die Key-Value-Liste, die in eine URL-escaped Zeichenkette konvertiert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in die die Zeichenkette gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KeyValueListToUrlEscapedString Data="{@myList}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Konvertiert die Key-Value-Liste **{@myList}** in einen URL-escaped String und speichert ihn in **{@Result}**.  
 

Beispiel-Ausgabe: **Username=MaxMustermann&Password=1234&City=Berlin.**