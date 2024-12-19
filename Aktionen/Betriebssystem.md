# Betriebssystem
GetEnvironmentVariable
----------------------

Die Aktion **GetEnvironmentVariable** liest eine Umgebungsvariable aus und speichert ihren Wert in einer angegebenen Variable.

```text-x-trilium-auto
<GetEnvironmentVariable Name="" TargetProcess="false" TargetUser="false" TargetSystem="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name der zu lesenden Umgebungsvariable.
*   **TargetProcess**: Gibt an, ob die Variable für den aktuellen Prozess gilt (true oder false).
*   **TargetUser**: Gibt an, ob die Variable für den aktuellen Benutzer gilt (true oder false).
*   **TargetSystem**: Gibt an, ob die Variable für das gesamte System gilt (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in der der Wert der Umgebungsvariable gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<GetEnvironmentVariable Name="PATH" TargetSystem="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest die Umgebungsvariable **PATH** auf Systemebene aus und speichert sie in der Variable **{@Result}**.

SetEnvironmentVariable
----------------------

Die Aktion **SetEnvironmentVariable** setzt oder aktualisiert den Wert einer Umgebungsvariable.

```text-x-trilium-auto
<SetEnvironmentVariable Name="" Value="" TargetProcess="false" TargetUser="false" TargetSystem="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Name**: Der Name der zu setzenden Umgebungsvariable.
*   **Value**: Der Wert, der für die Umgebungsvariable gesetzt wird.
*   **TargetProcess**: Gibt an, ob die Variable für den aktuellen Prozess gilt (true oder false).
*   **TargetUser**: Gibt an, ob die Variable für den aktuellen Benutzer gilt (true oder false).
*   **TargetSystem**: Gibt an, ob die Variable für das gesamte System gilt (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<SetEnvironmentVariable Name="MY_APP_PATH" Value="C:\Programme\MeinApp" TargetUser="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Setzt die Umgebungsvariable **MY\_APP\_PATH** für den aktuellen Benutzer auf den Pfad **C:\\Programme\\MeinApp**.

GetFingerprint
--------------

Die Aktion **GetFingerprint** berechnet einen Fingerprint basierend auf der Hardware des Rechners und einem angegebenen Schlüssel.

```text-x-trilium-auto
<GetFingerprint Key="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key**: Der Schlüssel oder Wert, der für die Fingerprint-Berechnung verwendet wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der der ermittelte Fingerprint gespeichert wird.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<GetFingerprint Key="MeineProgrammLizenz" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Berechnet den Fingerprint für den Schlüssel **MeineProgrammLizenz** und speichert das Ergebnis in **{@Result}**.

ShellExecute
------------

Die Aktion **ShellExecute** führt ein externes Programm oder Skript aus und gibt die Ergebnisse zurück.

```text-x-trilium-auto
<ShellExecute File="" Arguments="" OutputData="{@OutputData}" ErrorData="{@ErrorData}" CreateNoWindow="true" RedirectStandardOutput="true" RedirectStandardError="true" UseShellExecute="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **File**: Der Pfad zur auszuführenden Datei.
*   **Arguments**: (Optional) Die Befehlszeilenargumente für das Programm.
*   **OutputData**: Variable, in der die Standardausgabe gespeichert wird.
*   **ErrorData**: Variable, in der die Fehlermeldungen gespeichert werden.
*   **CreateNoWindow:** Gibt an, ob das Programm ohne Fenster gestartet wird (true oder false).
*   **RedirectStandardOutput**: Gibt an, ob die Ausgabe des auszuführenden Programms in den Wert der Variablen unter OutputData geladen werden soll (true oder false).
*   **RedirectStandardError**: Gibt an, ob die Ausgabe des auszuführenden Programms in den Wert der Variablen unter ErrorData geladen werden soll (true oder false).
*   **UseShellExecute**: Gibt an, ob die Ausführung des Programms über die Kommandozeile stattfinden soll (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<ShellExecute File="cmd.exe" Arguments="/c dir C:\Daten" OutputData="{@Output}" ErrorData="{@Error}" CreateNoWindow="true" RedirectStandardOutput="true" UseShellExecute="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Führt den Befehl **dir C:\\Daten** aus und speichert die Standardausgabe in **{@Output}** und Fehlerausgaben in **{@Error}**.

IsProcessRunning
----------------

Die Aktion **IsProcessRunning** prüft, ob ein bestimmter Prozess läuft.

```text-x-trilium-auto
<IsProcessRunning ProcessName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ProcessName**: Der Name des zu prüfenden Prozesses (z. B. notepad.exe).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob der Prozess am laufen ist. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<IsProcessRunning ProcessName="notepad.exe" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob der Prozess **notepad.exe** läuft, und speichert das Ergebnis in **{@Result}**.

IsServiceInstalled
------------------

Die Aktion **IsServiceInstalled** prüft, ob ein bestimmter Windows-Dienst auf dem System installiert ist.

```text-x-trilium-auto
<IsServiceInstalled ServiceName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServiceName**: Der Name des zu prüfenden Dienstes.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob der Dienst installiert ist (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<IsServiceInstalled ServiceName="Spooler" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob der Windows-Dienst **Spooler** (Druckwarteschlange) auf dem System installiert ist, und speichert das Ergebnis in (true oder false) **{@Result}**.

IsServiceRunning
----------------

Die Aktion **IsServiceRunning** prüft, ob ein bestimmter Windows-Dienst aktuell läuft.

```text-x-trilium-auto
<IsServiceRunning ServiceName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServiceName:** Der Name des zu prüfenden Dienstes.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob der Dienst gestartet ist (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<IsServiceRunning ServiceName="Spooler" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob der Windows-Dienst **Spooler** (Druckwarteschlange) aktuell läuft, und speichert das Ergebnis (true oder false) in **{@Result}**.

ServiceInstall
--------------

Die Aktion **ServiceInstall** installiert einen neuen Windows-Dienst aus einer angegebenen Dienstdatei.

```text-x-trilium-auto
<ServiceInstall ServicePath="" ServiceFile="" ServiceName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServicePath**: Der Pfad, in dem der Dienst installiert wird.
*   **ServiceFile**: Die vollständige Datei des Dienstes (z. B. .exe oder .dll).
*   **ServiceName**: Der Name des zu installierenden Dienstes.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob der Dienst erfolgreich installiert wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<ServiceInstall ServicePath="C:\Programme\MeinDienst" ServiceFile="MeinDienst.exe" ServiceName="MeinService" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Installiert den Dienst **MeinService** aus der Datei **MeinDienst.exe** unter dem Pfad **C:\\Programme\\MeinDienst**.

ServiceUninstall
----------------

Die Aktion **ServiceUninstall** deinstalliert einen vorhandenen Windows-Dienst.

```text-x-trilium-auto
<ServiceUninstall ServicePath="" ServiceFile="" ServiceName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServicePath**: Der Pfad, aus dem der Dienst entfernt wird.
*   **ServiceFile**: Die Datei des zu deinstallierenden Dienstes.
*   **ServiceName**: Der Name des zu deinstallierenden Dienstes.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Eine Variable, in der gespeichert wird, ob der Dienst erfolgreich deinstalliert wurde (true oder false).
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<ServiceUninstall ServicePath="C:\Programme\MeinDienst" ServiceFile="MeinDienst.exe" ServiceName="MeinService" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Deinstalliert den Dienst **MeinService**, der unter dem Pfad **C:\\Programme\\MeinDienst** installiert ist.

ServiceStart
------------

Die Aktion **ServiceStart** startet einen Windows-Dienst und wartet optional auf den Status „Running“.

```text-x-trilium-auto
<ServiceStart ServiceName="" WaitForStatusRunning="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServiceName**: Der Name des zu startenden Dienstes.
*   **WaitForStatusRunning**: Gibt an, ob auf den Status "Running" gewartet wird (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<ServiceStart ServiceName="Spooler" WaitForStatusRunning="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Startet den Dienst **Spooler** (Druckwarteschlange) und wartet, bis der Status "Running" erreicht ist.

ServiceStop
-----------

Die Aktion **ServiceStop** stoppt einen Windows-Dienst und wartet optional auf den Status „Stopped“.

```text-x-trilium-auto
<ServiceStop ServiceName="" WaitForStatusStopped="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **ServiceName**: Der Name des zu stoppenden Dienstes.
*   **WaitForStatusStopped**: Gibt an, ob auf den Status „Stopped“ gewartet wird (true oder false).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<ServiceStop ServiceName="Spooler" WaitForStatusStopped="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Stoppt den Dienst **Spooler** (Druckwarteschlange) und wartet, bis der Status „Stopped“ erreicht ist.

KillTask
--------

Die Aktion **KillTask** beendet einen laufenden Prozess.

```text-x-trilium-auto
<KillTask Process="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Process**: Der Name des zu beendenden Prozesses (z. B. notepad.exe).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<KillTask Process="notepad.exe" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Beendet den Prozess **notepad.exe**, falls dieser läuft.

RegAsm
------

Die Aktion **RegAsm** registriert oder deregistriert eine .NET-Assembly-Datei (z. B. DLL).

```text-x-trilium-auto
<RegAsm File="" Arguments="" OutputData="{@OutputData}" ErrorData="{@ErrorData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **File:** Der Pfad zur .NET-Assembly-Datei.
*   **Arguments:** (Optional) Zusätzliche Argumente für den Befehl.
*   **OutputData:** Variable, in der die Standardausgabe gespeichert wird.
*   **ErrorData:** Variable, in der die Fehlermeldungen gespeichert werden.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegAsm File="C:\Programme\MeineLib.dll" Arguments="/codebase" OutputData="{@Output}" ErrorData="{@Error}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Registriert die .NET-Assembly **MeineLib.dll** mit dem Argument **/codebase**.

RegSvr32
--------

Die Aktion **RegSvr32** registriert oder deregistriert eine COM-DLL oder OCX-Datei.

```text-x-trilium-auto
<RegSvr32 File="" Arguments="" OutputData="{@OutputData}" ErrorData="{@ErrorData}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **File**: Der Pfad zur DLL- oder OCX-Datei.
*   **Arguments**: (Optional) Zusätzliche Argumente für die Registrierung (z. B. /u für Deregistrierung).
*   **OutputData:** Variable, in der die Standardausgabe gespeichert wird.
*   **ErrorData:** Variable, in der die Fehlermeldungen gespeichert werden.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegSvr32 File="C:\Programme\MeineKomponente.dll" Arguments="/s" OutputData="{@Output}" ErrorData="{@Error}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Registriert die **MeineKomponente.dll** still (ohne Dialog).

WindowsProductKey
-----------------

Die Aktion **WindowsProductKey** liest den Produktschlüssel der aktuellen Windows-Installation aus.

```text-x-trilium-auto
<WindowsProductKey Variable="{@Result}" />
```

Attribute:

*   **Variable:** Die Variable, in der der Produktschlüssel gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<WindowsProductKey Variable="{@WindowsKey}" />
```

Liest den Windows-Produktschlüssel aus und speichert ihn in die Variable **{@WindowsKey}**.

Parameter
---------

|     |     |
| --- | --- |
| **Parameter** | **Wert (Beispiel)** |
| {@CommandLine} | "C:\\Program Files (x86)\\LogiSoft Batchpad\\Batchpad.exe" |
| {@ComputerName} | DEVWIN10 |
| {@ComputerUser} | LogiSoft |
| {@ComputerDomain} | DEVWIN10 |
| {@SystemName} | Microsoft Windows 10 Pro |
| {@SystemVersion} | 6.2.9200.0 |
| {@Is64BitOperatingSystem} | True |
| {@InstalledUICulture} | de-DE |

GetWMIClassInstance
-------------------

Die Aktion **GetWMIClassInstance** liest eine bestimmte Instanz einer WMI-Klasse aus.

```text-x-trilium-auto
<GetWMIClassInstance Data="{@myList}" Class="Win32_Processor" Instance="0" Variable="{@Result}" />
```

Attribute:

*   **Data**: Variable, in der die WMI-Daten gespeichert werden.
*   **Class**: Der Name der WMI-Klasse (z. B. Win32\_Processor).
*   **Instance**: Der Index der Instanz (Standardwert: 0).
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<GetWMIClassInstance Data="{@myList}" Class="Win32_Processor" Instance="0" Variable="{@Result}" />
```

Liest die erste Instanz der **Win32\_Processor**\-Klasse aus und speichert die Ergebnisse in **{@myList}**.

GetWMIClassInstanceCount
------------------------

Die Aktion **GetWMIClassInstanceCount** ermittelt die verfügbaren Instanzen einer bestimmten WMI-Klasse.

```text-x-trilium-auto
<GetWMIClassInstanceCount Class="Win32_Processor" Variable="{@Result}" />
```

Attribute:

*   **Class**: Der Name der WMI-Klasse.
*   **Variable**: Variable, in der die Anzahl der Instanzen gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<GetWMIClassInstanceCount Class="Win32_LogicalDisk" Variable="{@Result}" />
```

Zählt die verfügbaren Instanzen der WMI-Klasse **Win32\_LogicalDisk** und speichert das Ergebnis in **{@Result}**. 

GetWMIDataValue
---------------

Die Aktion **GetWMIDataValue** liest einen bestimmten Wert aus einer WMI-Daten Instanz aus.

```text-x-trilium-auto
<GetWMIDataValue Data="{@myList}" Key="" Variable="{@Result}" />
```

Attribute:

*   **Data**: Die WMI-Daten Instanz, aus denen der Wert gelesen wird.
*   **Key**: Der Name des Wertes, der ausgelesen werden soll.
*   **Variable**: Variable, in der der ausgelesene Wert gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<GetWMIDataValue Data="{@myList}" Key="Name" Variable="{@Result}" />
```

Liest den Wert **Name** aus den gespeicherten WMI-Daten Instanz **{@myList}** und speichert ihn in die Variable **{@Result}**.

Übersicht von WMI Klassen
-------------------------

Es gibt viele interessante **WMI-Klassen**, die für verschiedene Zwecke nützlich sind. Hier ist eine Auswahl gängiger und hilfreicher WMI-Klassen, aufgeteilt nach Anwendungsfällen:

### Hardware-Informationen

Diese Klassen liefern Informationen über die Hardware des Systems.

*   **Win32\_Processor**  
    Informationen über die CPU, wie Name, Taktfrequenz und Anzahl der Kerne.
    *   Nützliche Eigenschaften: `Name`, `MaxClockSpeed`, `NumberOfCores`, `ProcessorId`
*   **Win32\_PhysicalMemory**  
    Details über den installierten Arbeitsspeicher (RAM).
    *   Nützliche Eigenschaften: `Capacity`, `Speed`, `Manufacturer`, `PartNumber`
*   **Win32\_DiskDrive**  
    Informationen zu Festplatten.
    *   Nützliche Eigenschaften: `Model`, `Size`, `SerialNumber`, `InterfaceType`
*   **Win32\_VideoController**  
    Informationen über die Grafikkarte.
    *   Nützliche Eigenschaften: `Name`, `AdapterRAM`, `DriverVersion`, `VideoModeDescription`
*   **Win32\_BIOS**  
    Informationen zum BIOS des Systems.
    *   Nützliche Eigenschaften: `Manufacturer`, `SMBIOSBIOSVersion`, `SerialNumber`, `ReleaseDate`

### Betriebssystem-Informationen

Diese Klassen helfen bei der Analyse des Betriebssystems.

*   **Win32\_OperatingSystem**  
    Details zum installierten Betriebssystem.
    *   Nützliche Eigenschaften: `Caption`, `Version`, `OSArchitecture`, `LastBootUpTime`, `InstallDate`
*   **Win32\_ComputerSystem**  
    Informationen zum Computer selbst.
    *   Nützliche Eigenschaften: `Manufacturer`, `Model`, `TotalPhysicalMemory`, `SystemType`
*   **Win32\_BootConfiguration**  
    Informationen zu den Boot-Einstellungen.
    *   Nützliche Eigenschaften: `BootDirectory`, `ConfigurationPath`

### Netzwerk-Informationen

Diese Klassen bieten Netzwerkdaten wie Adapter, IP-Adressen und Verbindungen.

*   **Win32\_NetworkAdapter**  
    Details zu Netzwerkadaptern.
    *   Nützliche Eigenschaften: `Name`, `MACAddress`, `NetEnabled`, `Speed`
*   **Win32\_NetworkAdapterConfiguration**  
    Konfigurationseinstellungen der Netzwerkadapter.
    *   Nützliche Eigenschaften: `IPAddress`, `IPSubnet`, `DefaultIPGateway`, `DHCPEnabled`, `MACAddress`
*   **Win32\_PingStatus**  
    Hilft beim Testen der Erreichbarkeit von Netzwerken.

### Speichernutzung und Laufwerke

*   **Win32\_LogicalDisk**  
    Informationen zu logischen Laufwerken (z. B. C:, D:).
    *   Nützliche Eigenschaften: `DeviceID`, `FreeSpace`, `Size`, `FileSystem`
*   **Win32\_Volume**  
    Informationen zu Laufwerksvolumen.
    *   Nützliche Eigenschaften: `DriveLetter`, `Capacity`, `FreeSpace`, `Label`
*   **Win32\_ShadowCopy**  
    Details zu Schattenkopien (Snapshots).

### Prozesse und Dienste

Diese Klassen überwachen laufende Prozesse und Dienste.

*   **Win32\_Process**  
    Informationen zu laufenden Prozessen.
    *   Nützliche Eigenschaften: `Name`, `ProcessId`, `ParentProcessId`, `CommandLine`, `ExecutablePath`
*   **Win32\_Service**  
    Informationen zu Diensten.
    *   Nützliche Eigenschaften: `Name`, `State`, `StartMode`, `PathName`, `DisplayName`

### Energieverwaltung

Für die Überwachung von Akkustatus und Stromverbrauch.

*   **Win32\_Battery**  
    Informationen zum Akku des Geräts.
    *   Nützliche Eigenschaften: `BatteryStatus`, `EstimatedChargeRemaining`, `EstimatedRunTime`
*   **Win32\_PowerPlan**  
    Informationen zu aktuellen Energieplänen.

### Benutzer und Sicherheit

*   **Win32\_UserAccount**  
    Details zu Benutzerkonten.
    *   Nützliche Eigenschaften: `Name`, `FullName`, `SID`, `LocalAccount`
*   **Win32\_Group**  
    Informationen zu Gruppen auf dem System.
    *   Nützliche Eigenschaften: `Name`, `Description`
*   **Win32\_LogonSession**  
    Informationen zu laufenden Anmeldesitzungen.
    *   Nützliche Eigenschaften: `LogonId`, `StartTime`, `AuthenticationPackage`

### Drucker und Peripheriegeräte

*   **Win32\_Printer**  
    Informationen zu installierten Druckern.
    *   Nützliche Eigenschaften: `Name`, `Default`, `PrinterStatus`, `Local`
*   **Win32\_USBController**  
    Details zu USB-Controllern und angeschlossenen Geräten.
    *   Nützliche Eigenschaften: `Name`, `Status`, `DeviceID`
*   **Win32\_PnPEntity**  
    Informationen zu Plug-and-Play-Geräten.

### Zeit und Systemereignisse

*   **Win32\_LocalTime**  
    Aktuelle Systemzeit und Datum.
*   **Win32\_SystemTimeZone**  
    Informationen zur Zeitzone des Systems.
*   **Win32\_NTLogEvent**  
    Zugriff auf Ereignisprotokolle (z. B. Anwendungs-, Sicherheits- und Systemprotokolle).
    *   Nützliche Eigenschaften: `EventCode`, `Type`, `SourceName`, `Message`, `TimeGenerated`

Mit diesen **WMI-Klassen** können nahezu alle Aspekte eines Systems überwacht, analysiert oder sogar automatisiert werden.

### Beispiel: Nutzung von WMI-Klassen

Ein **praktisches Beispiel**, um die CPU-Details (Win32\_Processor) auszulesen:

```text-x-trilium-auto
<GetWMIClassInstance Data="{@ProcessorData}" Class="Win32_Processor" Instance="0" Variable="{@Result}" />
<GetWMIDataValue Data="{@ProcessorData}" Key="Name" Variable="{@ProcessorName}" />
```

*   **Win32\_Processor** wird abgefragt.
*   Der CPU-Name wird über **GetWMIDataValue** aus den WMI-Daten extrahiert und in **{@ProcessorName}** gespeichert.