# SFTP Datei Download
```text-x-trilium-auto
<Batch ActionLog="false" ConditionLog="false">
        
    <Set Variable="{@BackupFolder}" Value="C:\Backup\" />
    <PathExists Path="{@BackupFolder}" Variable="{@ResultExists}" />
    <PathCreate Path="{@BackupFolder}" Condition="NOT {@ResultExists}" />
        
    <Set Variable="{@ServerNames}" Value="abc.de;vwx.yz;logisoft.de" />
    <StringSplit Data="{@ServerNamesData}" Value="{@ServerNames}" Delimiter=";" SplitLines="false" RemoveEmptyValues="false" />
    
    <ForEach Data="{@ServerNamesData}">
        <Print Text="Sichere Dateien von WebServer {@Data:Value}" />
        <Set Variable="{@WebServerName}" Value="{@Data:Value}" />
        
        <Set Variable="{@SiteBackupFolder}" Value="{@BackupFolder}\{@WebServerName}\" />
        <PathExists Path="{@SiteBackupFolder}" Variable="{@ResultExists}" />
        <PathCreate Path="{@SiteBackupFolder}" Condition="NOT {@ResultExists}" />

        <SFTPListDirectory Data="{@myFiles}" Source="/var/backup" Servername="{@WebServerName}" User="{@WebServerUsername}" 
        				   Password="{@WebServerPassword}" />

        <ForEach Data="{@myFiles}">
            <Print Text="{@Data:Value}" />
            <SFTPFileDownload Source="/var/backup/{@Data:Value}" Destination="{@SiteBackupFolder}\{@Data:Value}"
            				  Servername="{@WebServerName}" User="{@WebServerUsername}" Password="{@WebServerPassword}" />
        </ForEach>

    </ForEach>
</Batch>
```