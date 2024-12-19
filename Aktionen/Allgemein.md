# Allgemein
### Set

Mit der Aktion **Set** kann ein Wert in eine Platzhalter-Variable gesetzt werden. Diese Variable kann im späteren Ablauf des Skripts beliebig oft verwendet werden.

```text-x-trilium-auto
<Set Variable="" Value="" Condition="" />
```

### Print

Die Aktion **Print** erzeugt einen Text im Protokoll der ausgeführten Definition. Das Argument Text beinhaltet den zu protokollierenden Text. Das Attribut Variable enthält den Rückgabewert der Aktion vom Typ Boolean und gibt an, ob die Aktion erfolgreich ausgeführt wurde.

```text-x-trilium-auto
<Print Text="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### ThrowError

Die Aktion **ThrowError** lässt das Skript z.B. abhängig von einer Bedingung in Condition mit dem angegebenen Text als Fehler beenden. Das Argument Text beinhaltet den Text für die Fehlermeldung.

```text-x-trilium-auto
<ThrowError Text="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### Select

Das **Select**\-Konstrukt ermöglicht die bedingte Ausführung von Anweisungen basierend auf dem Wert einer Variablen. Mit diesem flexiblen Konstrukt können komplexe Entscheidungsstrukturen innerhalb von Workflows oder Skripten realisiert werden.

```text-x-trilium-auto
<Select Case="{@Value}" Condition="" >

	<Case Value="A">
		<Print Text="Wert ist A" />	
	</Case>

	<Case Value="B">	
		<Print Text="Wert ist B" />	
	</Case>
	
	<Case Value="C">	
		<Print Text="Wert ist C" />	
	</Case>
	
	...
	
	<CaseElse>	
		<Print Text="Wert ist unbekannt" />	
	</CaseElse>

</Select>
```

Attribute:

*   **Case**: Gibt den Wert an, gegen den die eingegebene Variable überprüft wird.
*   **Condition:** (Optional) Steuert die Ausführung des gesamten Select-Konstrukts. Wenn die Bedingung nicht erfüllt ist, wird die Ausführung übersprungen.
*   **Value:** Der Vergleichswert für das jeweilige **Case**\-Element.
*   **CaseElse:** Optionaler Block, der ausgeführt wird, wenn kein Wert in den **Case**\-Elementen übereinstimmt.

### ForEach

Die Aktion **ForEach** iteriert über das Objekt welche dem Attribut Data zugewiesen werden. Auf die Werte kann innerhalb des Tags über {@Data:Value} zugegriffen werden.

Value ist dabei nur ein Beispiel. Für diesen Wert muss beispielsweise die Bezeichnung der Tabellenspalte stehen über die iteriert wird.

Bei jedem Schleifendurchlauf werden die in ForEach verschachtelten Aktionen durchgeführt.

```text-x-trilium-auto
<ForEach Data="{@myData}" Condition="" >
... {@Data: ... } ...
</ForEach>
```

### ContinueForEach

Die Aktion **ContinueForEach** bricht die aktuelle Iteration der **ForEach** Schleife ab und führt die nächste Iteration aus.

```text-x-trilium-auto
<ContinueForEach Condition="" />
```

### ExitForEach

Die Aktion **ExitForEach** verlässt die **ForEach** Schleife. Es werden keinen weiteren Iterationen durchgeführt.

```text-x-trilium-auto
<ExitForEach Condition="" />
```

### Repeat

Die Aktion **Repeat** wiederholt die Schleife bis der {@RepeatCount} Wert erreicht wird. Dabei wird der Count bei jedem Durchlauf um 1 inkrementiert. Der Wert des Counts pro Iteration zur Laufzeit hält dabei die Variable {@CurrentCount}.

Hinweis: Die Variable {@CurrentCount} wird von der Aktion Repeat deklariert und muss daher nicht zusätzlich über die Aktion SetVariable deklariert werden. 

Bei jedem Schleifendurchlauf werden die in Repeat verschachtelten Aktionen durchgeführt.

```text-x-trilium-auto
<Repeat Count="{@RepeatCount}" Condition="" Variable="{@CurrentCount}">
...
</Repeat>
```

### ContinueRepeat

Die Aktion **ContinueRepeat** bricht die aktuelle Iteration der **Repeat** Schleife ab und führt die nächste Iteration durch.

```text-x-trilium-auto
<ContinueRepeat Condition="" />
```

### ExitRepeat

Die Aktion **ExitRepeat** verlässt die **Repeat** Schleife. Es werden keinen weiteren Iterationen durchgeführt.

```text-x-trilium-auto
<ExitRepeat Condition="" />
```

### Function

Innerhalb der Aktion **Function** können Aktionen hinterlegt werden, welche nur durchlaufen werden, wenn die Funktion aufgerufen wird. Siehe **CallFunction**.

```text-x-trilium-auto
<Function Name="">
...
</Function>
```

### CallFunction

Die Aktion **CallFunktion** ruft die im Attribut Name aufgeführte Aktion aus. Das Attribut Variable enthält den Rückgabewert der Aktion vom Typ Boolean und gibt an ob die Aktion erfolgreich ausgeführt wurde.

```text-x-trilium-auto
<CallFunction Name="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### CallModule

Die Aktion **CallModule** ruft das unter dem Attribut Name angegebene Modul auf. Hier kann ein Pfad angegeben werden wo die Datei mit dem Batchpad-Skript des Moduls abgelegt ist. Das Attribut Variable enthält den Rückgabewert der Aktion vom Typ Boolean und gibt an ob die Aktion erfolgreich ausgeführt wurde.

```text-x-trilium-auto
<CallModule Name="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### Eval

Die Aktion **Eval** führt ein VB-Skript zum Ermitteln eines Ergebnisses aus. Mit dem Argument Script wird der zu prüfende VB-Skript Ausdruck angegeben. Die angegebene Variable im Argument Variable erhält nach Prüfung des Skriptes das Ergebnis vom Typ Boolean.

```text-x-trilium-auto
<Eval Script="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### Sleep

Die Aktion **Sleep** verzögert die Ausführung des Skripts für den im Attribut Milliseconds angegebenen Zeitraum. Das Attribut Variable enthält den Rückgabewert der Aktion vom Typ Boolean und gibt an ob die Aktion erfolgreich ausgeführt wurde.

```text-x-trilium-auto
<Sleep Milliseconds="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

### Pause

Die Aktion **Pause** pausiert die Ausführung des Skripts. Der Einsatzzweck der Aktion Pause ist das Debuggen des Skripts. Anschließend kann ab dieser Position im Einzelschritten fortgefahren werden.

```text-x-trilium-auto
<Pause Condition="" />
```

### Stop

Die Aktion **Stop** stoppt die Ausführung des Skripts.

```text-x-trilium-auto
<Stop Condition="" />
```

### ClearLog

Die Aktion **ClearLog** leert die Ausgabe im Ausgabefenster.

```text-x-trilium-auto
<ClearLog Condition="" />
```

### RemoteBatch

Mit der Aktion **RemoteBatch** kann man ein Batchpad-Skript direkt an den Batchpad Aufgabenplaner Dienst zur Ausführung schicken. Über das Attribut RemoteServer kann auch ein Dienst der auf einem anderen Server läuft angesprochen werden indem die entsprechende IP-Adresse eingetragen wird. Als RemoteParameter definiert man die Werte, die aus der aktuellen Ausführung an den Dienst übergeben werden sollen. Mit dem Attribut RemoteResults gibt man an, welche Variablen als Ergebnis von der Ausführung des Dienstes zurück kommen sollen. Per RemoteScript wird die Datei mit  dem Batchpad-Skript angegeben.

```text-x-trilium-auto
<RemoteBatch ActionLog="true" ConditionLog="false" RemoteServer="127.0.0.1" RemotePort="18611" RemoteTimeout="10000" RemoteParameter="{@myVariable};{@myData}" RemoteResults="{@myVariable};{@myData}" RemoteScript="" Condition="" Variable="{@Result}" IgnoreError="false" />
```