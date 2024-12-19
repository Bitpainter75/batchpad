# Hello World
Hello World - Beispiele zum Einstieg in das Thema Batchpad

Inhalt des Beispiels

*   Werte im Ausgabefenster ausgeben (Print)
*   Variablen verwenden
*   String Operationen
*   Bedingungen und Schleifen
*   Kalkulationen
*   Funktionen und Aufruf der Funktionen

```text-x-trilium-auto
<Batch>
    
    <Print Text="Ich zähle jetzt bis zehn... und überspringe die fünf" />
    
    <Repeat Count="10" Variable="{@CurrentCount}" >
        <ContinueRepeat Condition="{@CurrentCount}=5" />
        <Print Text="Die aktuelle Zahl ist {@CurrentCount}" />
    </Repeat>    
    
    <Print Text="Ich zähle jetzt ein paar Namen aus einer kommaseparierten Zeichenkette String auf" />

    <Set Variable="{@myString}" Value="Hans,Peter,Klaus,Timo,Andreas,Oliver" />
    
    <StringSplit Data="{@myData}" Value="{@myString}" Delimiter="," SplitLines="false" RemoveEmptyValues="false" />
    
    <ForEach Data="{@myData}" Condition="" IgnoreError="false">
        <Print Text="Der Name lautet {@Data:Value}" />
    </ForEach>
    
    <Print Text="Jetzt rufe ich eine Unterfunktion mehrmals auf und Addiere eine Zahl und zeige das Ergebnis an" />

    <Set Variable="{@myValue1}" Value="5" />
    <Set Variable="{@myValue2}" Value="3" />
    
    <CallFunction Name="Addieren" />
    <Set Variable="{@myValue1}" Value="{@ResultAddieren}" />
    <CallFunction Name="Addieren" />
    <Set Variable="{@myValue1}" Value="{@ResultAddieren}" />
    <CallFunction Name="Addieren" />
    
    <Function Name="Addieren">
        <CalculateAddition Value1="{@myValue1}" Value2="{@myValue2}" Float="false" Variable="{@ResultAddieren}" />
        <Print Text="Die addierte Zahl ist {@ResultAddieren}" />
    </Function>    
    
    <Print Text="Jetzt werte ich die letzte addierte Zahl aus" />
    
    <ConditionGreaterThan Value1="{@ResultAddieren}" Value2="10" Numeric="true" Not="false" Variable="{@ResultGreatherThan}" />
    
    <ConditionTrue Condition="{@ResultGreatherThan}" >
        <Print Text="Die Zahl {@ResultAddieren} ist größer 10" />
    </ConditionTrue>
    
    <ConditionTrue Condition="NOT {@ResultGreatherThan}" >
        <Print Text="Die Zahl {@ResultAddieren} ist kleiner gleich 10" />
    </ConditionTrue>    
    
</Batch>
```