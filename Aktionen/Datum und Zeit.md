# Datum und Zeit
DateAdd
-------

Die Aktion **DateAdd** addiert zu dem Attribut Date, welches ein Datum enthalten muss, einen Zeitintervall. 

Das Attribut Intervall kann die Werte aus folgenden Tabelle enthalten:

|     |     |
| --- | --- |
| **Intervall** | **Beschreibung** |
| yyyy | Jahr |
| q   | Quartal |
| m   | Monat |
| y   | Tag des Jahres |
| d   | Tag |
| w   | Wochentag |
| ww  | Woche |
| h   | Stunde |
| n   | Minute |
| s   | Sekunden |

Über das Attribut Value wird die Anzahl der Intervalle bestimmt. Das Ergebnis wird über das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<DateAdd Date="" Interval="" Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateDiff
--------

Die Aktion **DateDiff** ermittelt den Unterschied in Intervallen zwischen den Attributen Date1 und Date2, welche ein Datum enthalten müssen. Das Attribut Interval kann die Werte aus Tabelle 1 erhalten. Das Ergebnis wird über das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<DateDiff Date1="" Date2="" Interval="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DatePart
--------

Die Aktion **DatePart** ermittelt eine bestimmte Komponente des Attributs Date, welches ein Datum enthalten muss. Das Attribut Interval gibt dabei an, welcher Teil des Datums ermittelt werden soll. Für das Attribut Intervall sind die Werte aus Tabelle 1 möglich. Das Ergebnis wird über das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<DatePart Date="" Interval="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateSerial
----------

Die Aktion **DateSerial** gibt über das Attribut Variable einen Wert zurück der ein angegebenes Jahr (Attribut: Year), einem angegebenen Monat (Attribut: Month) und einen angegebenen Tag (Attribut: Day) darstellt.

```text-x-trilium-auto
<DateSerial Year="" Month="" Day="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

TimeSerial
----------

Die Aktion **TimeSerial** gibt über das Attribut Variable einen Wert zurück der eine angegebene Stunde (Attribut: Hour), einer angegebenen Minute (Attribut: Minute) und einer angegebenen Sekunde (Attribut: Second) darstellt.

```text-x-trilium-auto
<TimeSerial Hour="" Minute="" Second="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

MonthName
---------

Die Aktion **MonthName** gibt über das Attribut Variable den Monat des in dem Attribut Date angegebenen Datum zurück.

```text-x-trilium-auto
<MonthName Date="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

WeekdayName
-----------

Die Aktion **WeekdayName** gibt über das Attribut Variable den Wochentag des in dem Attribut Date angegebenen Datum zurück.

```text-x-trilium-auto
<WeekdayName Date="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateToLocalDateTime
-------------------

Die Aktion **DateToLocalDateTime** konvertiert ein UTC Datum mit Uhrzeit in das lokale Datum mit Uhrzeit.

```text-x-trilium-auto
<DateToLocalDateTime Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateToUniversalDateTime
-----------------------

Die Aktion **DateToUniversalDateTime** konvertiert ein lokales Datum mit Uhrzeit in das UTC Datum mit Uhrzeit.

```text-x-trilium-auto
<DateToUniversalDateTime Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateToISO8601Format
-------------------

Die Aktion **DateToISO8601Format** konvertiert ein Datum in das ISO 8601 Datumsformat

```text-x-trilium-auto
<DateToISO8601Format Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

DateToTimestamp
---------------

Die Aktion **DateToTimestamp** konvertiert das Attribut Value in einen Timestamp und gibt das Ergebnis über das Attribut Variable zurück.

```text-x-trilium-auto
<DateToTimestamp Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

TimestampToDate
---------------

Die Aktion **TimestampToDate** konvertiert das Attribut Value in ein Datum und gibt das Ergebnis über das Attribut Variable zurück.

```text-x-trilium-auto
<TimestampToDate Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Parameter
---------

|     |     |
| --- | --- |
| **Parameter** | **Wert** |
| {@SystemDate} | Aktuelles Systemdatum |
| {@SystemDay} | Aktueller Tag des Systemdatum |
| {@SystemMonth} | Aktueller Monat des Systemdatums |
| {@SystemYear} | Aktuelles Jahr des Systemdatums |
| {@SystemHour} | Aktuelle Stunde des Systemdatums |
| {@SystemMinute} | Aktuelle Minute des Systemdatums |
| {@SystemSecond} | Aktuelle Sekunde des Systemdatums |