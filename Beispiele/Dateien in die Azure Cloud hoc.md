# Dateien in die Azure Cloud hochladen
Das folgende Beispiel ermittelt die Dateien aus einem Verzeichnis und lädt die Dateien in die Azure Cloud hoch.

```text-x-trilium-auto
<Batch>

    <!-- Azure Zugangsdaten -->
    <Set Variable="{@AzureAccount}" Value="" />
    <Set Variable="{@AzureKey}" Value="" />
    <Set Variable="{@AzureContainer}" Value="" />

    <Set Variable="{@UploadDir}" Value="E:\Ablage"

    <FileListDirectory WithInformations="True" Source="{@UploadDir}" Data="{@myFiles}" />

    <ForEach Data="{@myFiles}" >

        <AzureBlobFileUpload Source="{@Data:FullName}" Destination="Ablage/{@Data:Value}" Account="{@AzureAccount}" Key="{@AzureKey}" Container="{@AzureContainer}" Condition="{@Data:IsFile}" Variable="{@UploadResult}" IgnoreError="true" />
        <!--<FileDelete File="{@Data:FullName}" Condition="{@Data:IsFile} AND {@UploadResult}" IgnoreError="true" />-->

    </ForEach>

</Batch>
```