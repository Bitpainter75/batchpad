# Dateien in Datenbank speichern und auslesen
Das Beispiel zeigt wie Dateien in der Datenbank abgelegt und ausgelesen werden können.

Für die Dateiablage in einer Datenbank sind folgende Attribute in der Aktion <SQLFileUpload...> verfügbar:

*   DataField: Binärdaten der Datei (Datentyp: varbinary)
*   FileNameFiled (Optional): Bezeichnung der Datei (Datentyp: varchar)
*   ExtensionField (Optional): Dateiendung der Datei z.B. ".jpg" (Datentyp: varchar)

Die Bezeichnung der Felder ist in der DB-Tabelle frei wählbar. Die Felder können dann für die Aktion <SQLFileUpload...> verwendet werden, siehe folgendes Beispiel:

```text-x-trilium-auto
<Batch>
    <!-- Verbindung zur Datenbank aufbauen und Daten lesen -->
    <SQLConnect  Connection="{@myConnection}" Server="{@SQLServername}" Database="FileDB" 
                 User="{@SQLUsername}" Password="{@SQLPassword}" />
                    
    <SQLReadData Data="{@myData}" Query="SELECT ID FROM Documents" Connection="{@myConnection}" />
    
    <!-- In jeden gefundenen Datensatz eine .jpg Datei in die Datenbank speichern und anschließend auslesen -->
    <ForEach Data="{@myData}">
    <!-- DataField > Feld das die Binärdaten der Datei hält; FileNameField (Optional) > Feld das die Bezeichnung der Datei hält; ExtensionField (Optional) > Feld das die Dateiendung der Datei hält-->
        <SQLFileUpload FileName="E:\LogiSoft.jpg" Table="Documents" Where="ID='{@Data:ID}'" 
                       DataField="Data" FileNameField="Filename" ExtensionField="Extension" 
                       Connection="{@myConnection}" />
                            
        <SQLFileDownload FileName="E:\{@Data:ID}.jpg" Table="Documents" Where="ID='{@Data:ID}'" 
                         DataField="Data" Connection="{@myConnection}" />
    </ForEach>
</Batch>
```