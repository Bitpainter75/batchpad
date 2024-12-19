# Windows Registry
RegKeyExists
------------

Die Aktion **RegKeyExists** prüft, ob der angegebene Schlüssel in der Windows-Registry existiert.

```text-x-trilium-auto
<RegKeyExists Key="" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad des zu prüfenden Registrierungs-Schlüssels.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable:** (Optional) Eine Variable, in der gespeichert wird, ob der Schlüssel existiert (true oder false).
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegKeyExists Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob der Schlüssel **SOFTWARE\\MeinProgramm** in **HKEY\_LOCAL\_MACHINE** existiert, und speichert das Ergebnis in **{@Result}**.

RegCreateKey
------------

Die Aktion **RegCreateKey** erstellt einen neuen Schlüssel in der Windows-Registry.

```text-x-trilium-auto
<RegCreateKey Key="" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad des zu erstellenden Registrierungs-Schlüssels.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegCreateKey Key="SOFTWARE\MeinProgramm\Settings" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt den Schlüssel **SOFTWARE\\MeinProgramm\\Settings** in **HKEY\_LOCAL\_MACHINE**.

RegDeleteKey
------------

Die Aktion **RegDeleteKey** löscht einen Schlüssel aus der Windows-Registry.

```text-x-trilium-auto
<RegDeleteKey Key="" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad des zu löschenden Registrierungs-Schlüssels.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegDeleteKey Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Schlüssel **SOFTWARE\\MeinProgramm** aus **HKEY\_LOCAL\_MACHINE**.

RegGetValue
-----------

Die Aktion **RegGetValue** liest den Wert eines Registry-Eintrags aus und speichert ihn in der angegebenen Variable.

```text-x-trilium-auto
<RegGetValue Key="" Root="HKEY_LOCAL_MACHINE" ValueName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel unter dem der Wert des Registry-Eintrags ausgelesen werden soll. 
*   **ValueName:** Der Name des Wertes, der ausgelesen werden soll.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable in der der Wert des Registry-Eintrags gespeichert wird
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegGetValue Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" ValueName="InstallPath" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Liest den Wert **InstallPath** aus dem Schlüssel **SOFTWARE\\MeinProgramm** in **HKEY\_LOCAL\_MACHINE** und speichert das Ergebnis in **{@Result}**.

RegSetValue
-----------

Die Aktion **RegSetValue** erstellt oder aktualisiert einen Wert in der Windows-Registry.

```text-x-trilium-auto
<RegSetValue Key="" Root="HKEY_LOCAL_MACHINE" ValueName="" Value="" Dword="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel unter dem der Wert des Registry-Eintrags gesetzt werden soll. 
*   **ValueName:** Der Name des zu erstellenden oder zu aktualisierenden Wertes.
*   **Value:** Der Wert, der gesetzt werden soll.
*   **Dword:** Gibt an, ob der Wert als DWORD gespeichert werden soll (true oder false).
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegSetValue Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" ValueName="InstallPath" Value="C:\Programme\MeinProgramm" Dword="false" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Setzt den Wert **InstallPath** auf **C:\\Programme\\MeinProgramm** im Schlüssel **SOFTWARE\\MeinProgramm**.

RegDeleteValue
--------------

Die Aktion **RegDeleteValue** löscht einen Wert aus einem Registry-Schlüssel.

```text-x-trilium-auto
<RegDeleteValue Key="" Root="HKEY_LOCAL_MACHINE" ValueName="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel unter dem der Wert des Registry-Eintrags gelöscht werden soll. 
*   **ValueName:** Der Name des zu löschenden Wertes.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegDeleteValue Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" ValueName="InstallPath" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht den Wert **InstallPath** aus dem Schlüssel **SOFTWARE\\MeinProgramm**.

RegGetSubKeyByValue
-------------------

Die Aktion **RegGetSubKeyByValue** sucht nach einem Unterschlüssel, der einen bestimmten Wert enthält.

```text-x-trilium-auto
<RegGetSubKeyByValue Key="SOFTWARE" Root="HKEY_LOCAL_MACHINE" ValueName="InstallPath" Value="MeinProgramm" Instr="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel unter dem der Wert gesucht werden soll. 
*   **ValueName:** Der Name des Registry-Eintrags mit dem zu suchenden Wert.
*   **Value:** Der zu suchende Wert.
*   **Instr:** Gibt an, ob die Suche eine Teilzeichenkette berücksichtigt (true oder false).
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable in der der gefundene Registry-Eintrag gespeichert wird.
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegGetSubKeyByValue Key="SOFTWARE" Root="HKEY_LOCAL_MACHINE" ValueName="InstallPath" Value="MeinProgramm" Instr="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Sucht im Unterschlüssel **SOFTWARE** nach einem Schlüssel, dessen Wert **InstallPath** die Teilzeichenkette **MeinProgramm** enthält.

RegGetListValueNames
--------------------

Ermittelt alle Registry-Einträge eines Registry-Schlüssels.

```text-x-trilium-auto
<RegGetListValueNames Key="" Root="HKEY_LOCAL_MACHINE" Data="{@myData}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel von dem die Registry-Einträge aufgelistet werden sollen. 
*   **Data**: Variable, in der die ermittelten Registry-Einträge gespeichert werden.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Elemente gespeichert wird.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegGetListValueNames Key="SOFTWARE\MeinProgramm" Root="HKEY_LOCAL_MACHINE" Data="{@myValues}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Alle ausgelesenen Registry-Einträge aus dem Unterschlüssel **SOFTWARE\\MeinProgramm** werden in das Daten-Objekt **{@myValues}** gespeichert.

RegGetListSubKeys
-----------------

Ermittelt alle Unterschlüssel eines Registry-Schlüssels.

```text-x-trilium-auto
<RegGetListSubKeys Key="" Root="HKEY_LOCAL_MACHINE" Data="{@myData}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Key:** Der Pfad zum Registrierungs-Schlüssel von dem die Unterschlüssel aufgelistet werden sollen. 
*   **Data**: Variable, in der die ermittelten Unterschlüssel gespeichert werden.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Elemente gespeichert wird.
*   **Root:** Der Hauptzweig der Windows-Registry. Standardwert ist HKEY\_LOCAL\_MACHINE. Mögliche Werte:
    *   HKEY\_LOCAL\_MACHINE
    *   HKEY\_CURRENT\_USER
    *   HKEY\_CLASSES\_ROOT
    *   HKEY\_USERS
    *   HKEY\_CURRENT\_CONFIG
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false
*   **IgnoreError:** (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<RegGetListSubKeys Key="SOFTWARE" Root="HKEY_LOCAL_MACHINE" Data="{@mySubKeys}" DataCount="{@ResultCount}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Unterschlüssel im **SOFTWARE**\-Zweig auf und speichert die Liste in **{@mySubKeys}**.