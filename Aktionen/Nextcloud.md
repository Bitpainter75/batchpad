# Nextcloud
NextcloudFileUpload
-------------------

Die Aktion **NextcloudFileUpload** führt einen Datei-Upload zu dem Nextcloud-Dateispeicher durch.

```text-x-trilium-auto
<NextcloudFileUpload Source="" Destination="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der lokale Pfad der Datei, die hochgeladen werden soll (inkl. Dateiname und Dateiendung).
*   **Destination**: Der Zielpfad auf Nextcloud, in dem die Datei hochgeladen wird. Der Pfad muss den Dateinamen und die Dateiendung enthalten.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileUpload Source="C:\Daten\Bericht.pdf" Destination="/Freigaben/Bericht.pdf" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** von **C:\\Daten** in den Nextcloud-Ordner **/Freigaben/** hoch.

NextcloudFileDownload
---------------------

Die Aktion **NextcloudFileDownload** führt einen Datei-Download aus dem Nextcloud-Dateispeicher durch.

```text-x-trilium-auto
<NextcloudFileDownload Source="" Destination="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei auf Nextcloud (inkl. Dateiname und Dateiendung).
*   **Destination**: Der lokale Pfad, in dem die Datei gespeichert wird (inkl. Dateiname und Dateiendung).
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileDownload Source="/Freigaben/Bericht.pdf" Destination="C:\Downloads\Bericht.pdf" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Lädt die Datei **Bericht.pdf** aus dem Nextcloud-Pfad **/Freigaben/** herunter und speichert sie in **C:\\Downloads**.

NextcloudFileDelete
-------------------

Die Aktion **NextcloudFileDelete** löscht eine Datei aus dem Nextcloud-Dateispeicher.

```text-x-trilium-auto
<NextcloudFileDelete Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur zu löschenden Datei (inkl. Dateiname und Dateiendung).
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileDelete Source="/Freigaben/Bericht.pdf" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Datei **Bericht.pdf** aus dem Nextcloud-Pfad **/Freigaben/**.

NextcloudPathCreate
-------------------

Die Aktion **NextcloudPathCreate** erstellt einen neuen Pfad (Ordner) auf dem Nextcloud-Dateispeicher.

```text-x-trilium-auto
<NextcloudPathCreate Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad des neuen Ordners, der erstellt werden soll.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudPathCreate Source="/Freigaben/NeuerOrdner" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erstellt den Ordner **NeuerOrdner** im Nextcloud-Pfad **/Freigaben/**.

NextcloudPathOrFileExists
-------------------------

Die Aktion **NextcloudPathOrFileExists** prüft, ob ein Pfad oder eine Datei auf dem Nextcloud-Dateispeicher existiert.

```text-x-trilium-auto
<NextcloudPathOrFileExists Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, der geprüft werden soll.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Die Variable, in der gespeichert wird, ob die Datei oder der Ordner gefunden wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudPathOrFileExists Source="/Freigaben/Bericht.pdf" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Datei **Bericht.pdf** im Nextcloud-Pfad **/Freigaben/** existiert.

NextcloudListDirectory
----------------------

Die Aktion **NextcloudListDirectory** listet alle Dateien und Ordner aus einem angegebenen Pfad auf und speichert die Ergebnisse als Daten-Tabelle.

```text-x-trilium-auto
<NextcloudListDirectory Data="" DataCount="" Source="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Data**: Variable, in der die Liste der Dateien und Ordner gespeichert wird.
*   **DataCount**: Variable, in der die Anzahl der gefundenen Dateien und Ordner gespeichert wird.
*   **Source**: Der Pfad des zu durchsuchenden Ordners.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudListDirectory Data="{@myFiles}" DataCount="{@ResultCount}" Source="/Freigaben" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Listet alle Dateien und Ordner aus dem Nextcloud-Pfad **/Freigaben/** auf, speichert die Inhalte in **{@myFiles}** und die Anzahl der Einträge in **{@ResultCount}**.

NextcloudFileShareCreate
------------------------

Erstellt eine Freigabe für eine Datei oder einen Ordner in Nextcloud mit konfigurierbaren Berechtigungen.

```text-x-trilium-auto
<NextcloudFileShareCreate Source="" Label="" AllowRead="true" AllowUpdate="true" AllowCreate="true" AllowDelete="true" AllowShare="true" SharePassword="" ExpireDate="" Note="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner in Nextcloud, der freigegeben werden soll.
*   **Label**: Ein benutzerdefinierter Name (Label) für die Freigabe.
*   **AllowRead**: Gibt an, ob die Freigabe Leserechte erlaubt. Werte: true oder false.
*   **AllowUpdate**: Gibt an, ob die Freigabe das Bearbeiten erlaubt. Werte: true oder false.
*   **AllowCreate**: Gibt an, ob das Erstellen von Dateien in der Freigabe erlaubt ist. Werte: true oder false.
*   **AllowDelete**: Gibt an, ob das Löschen von Dateien erlaubt ist. Werte: true oder false.
*   **AllowShare**: Gibt an, ob weitere Freigaben erstellt werden dürfen. Werte: true oder false.
*   **SharePassword**: (Optional) Ein Passwort, das für den Zugriff auf die Freigabe benötigt wird.
*   **ExpireDate**: (Optional) Ablaufdatum der Freigabe
*   **Note**: (Optional) Eine zusätzliche Notiz zur Freigabe.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileShareCreate Source="/Dokumente/Projektplan.pdf" Label="Freigabe1234" AllowRead="true" AllowUpdate="false" AllowCreate="false" AllowDelete="false" AllowShare="true" SharePassword="Secure123" ExpireDate="2024-02-01" Note="Freigabe für das Projektteam" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

In diesem Beispiel wird die Datei **Projektplan.pdf** freigegeben:

*   Freigabe erlaubt **Leserechte** und das Erstellen weiterer Freigaben.
*   Ein Passwort **Secure123** schützt die Freigabe.
*   Die Freigabe läuft am **1\. Februar 2024** ab.

NextcloudFileShareUpdate
------------------------

Aktualisiert eine bestehende Freigabe für eine Datei oder einen Ordner in Nextcloud.

```text-x-trilium-auto
<NextcloudFileShareUpdate Source="" Label="" AllowRead="true" AllowUpdate="true" AllowCreate="true" AllowDelete="true" AllowShare="true" SharePassword="" ExpireDate="" Note="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur bestehenden Freigabe.
*   **Label**: Ein benutzerdefinierter Name (Label) für die Freigabe.
*   **AllowRead**: Gibt an, ob die Freigabe Leserechte erlaubt. Werte: true oder false.
*   **AllowUpdate**: Gibt an, ob die Freigabe das Bearbeiten erlaubt. Werte: true oder false.
*   **AllowCreate**: Gibt an, ob das Erstellen von Dateien in der Freigabe erlaubt ist. Werte: true oder false.
*   **AllowDelete**: Gibt an, ob das Löschen von Dateien erlaubt ist. Werte: true oder false.
*   **AllowShare**: Gibt an, ob weitere Freigaben erstellt werden dürfen. Werte: true oder false.
*   **SharePassword**: (Optional) Ein Passwort, das für den Zugriff auf die Freigabe benötigt wird.
*   **ExpireDate**: (Optional) Ablaufdatum der Freigabe
*   **Note**: (Optional) Eine zusätzliche Notiz zur Freigabe.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.  
     

Beispiel:

```text-x-trilium-auto
<NextcloudFileShareUpdate Source="/Dokumente/Projektplan.pdf" Label="Freigabe1234" AllowRead="true" AllowUpdate="true" AllowCreate="false" AllowDelete="false" AllowShare="true" ExpireDate="2024-03-01" Note="Aktualisierte Freigabe" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Aktualisiert die Freigabe **Freigabe1234** für die Datei **Projektplan.pdf** mit neuen Berechtigungen und einem Ablaufdatum **1\. März 2024**.

NextcloudFileShareDelete
------------------------

Löscht eine bestehende Freigabe für eine Datei oder einen Ordner in Nextcloud.

```text-x-trilium-auto
<NextcloudFileShareDelete Source="" Label="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, dessen Freigabe gelöscht werden soll.
*   **Label**: Der benutzerdefinierte Name der Freigabe.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileShareDelete Source="/Dokumente/Projektplan.pdf" Label="Freigabe1234" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Löscht die Freigabe **Freigabe1234** für die Datei **Projektplan.pdf**.

NextcloudFileShareExists
------------------------

Prüft, ob eine Freigabe für eine Datei oder einen Ordner mit einem entsprechenden Label in Nextcloud existiert.

```text-x-trilium-auto
<NextcloudFileShareExists Source="" Label="" Username="" Password="" Hostname="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Source**: Der Pfad zur Datei oder zum Ordner, für die geprüft wird, ob eine Freigabe existiert.
*   **Label**: Der benutzerdefinierte Name der Freigabe.
*   **Username**: Der Benutzername für den Zugriff auf Nextcloud.
*   **Password**: Das Passwort für den Zugriff auf Nextcloud.
*   **Hostname**: Die URL oder der Hostname des Nextcloud-Servers.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Wenn auf true gesetzt, werden auftretende Fehler ignoriert und die Aktion wird fortgesetzt.

Beispiel:

```text-x-trilium-auto
<NextcloudFileShareExists Source="/Dokumente/Projektplan.pdf" Label="Projektfreigabe" Username="admin" Password="Passwort123" Hostname="https://nextcloud.example.com" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Prüft, ob die Freigabe **Projektfreigabe** für die Datei **Projektplan.pdf** existiert.