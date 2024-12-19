# Erweiterungen
mydatastreamInit
----------------

Die Aktion mydatastreamInit inititialisiert die Verbindung zu mydatastream. In dem Attribut wird die zu erreichende Portal Adresse eingetragen, beispielsweise "https://demo.mydata.stream/". Zudem muss der gültige Fingerprint (Attribut: LicenseNumber), ein gültiger Benutzer (Attribut: User) mit der Rolle Administrators und einem zugehörigen Passwort (Attribut: Password) hinterlegt werden.

```text-x-trilium-auto
<mydatastreamInit PortalUrl="https://domain.mydata.stream" LicenseNumber="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

mydatastreamSendMessage
-----------------------

Die Aktion mydatastreamSendMessage sendet an den unter "SendTo" angegebenen Benutzer (Benuterzname in mydatastream) einen Nachricht in den Benachrichtigungs-Raum des Chats. Hinweis: mydatastreamSendMessage muss in Verbindung mit mydatastreamInit verwendet werden. mydatastreamInit muss vor dieser Aktion ausgeführt werden.

```text-x-trilium-auto
<mydatastreamSendMessage SendTo="" Message="" Link="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

mydatastreamGetAccessLink
-------------------------

Die Aktion mydatastreamGetAccessLink erstellt einen Link auf ein Formular über den der Benutzer angemeldet wird und direkt auf das Formular weitergeleitet wird. Der Benutzer hat dabei nur Zugriff auf das freigegebene Formular. Für "SendTo" muss ein beliebiger Name angegeben werden. "FormularKey" kann aus dem AppBuilder entnommen werden, dort wird zu dem gewünschten Formular ein FormularKey hinterlegt. Der "Filter" bestimmt den Datensatz auf den der Link verweisen soll. Der Filter darf nur ein Ergebnis zurück liefern. "ExpireValue" in Verbindung mit "ExpireUnit" gibt an wie lange der Link gültig sein soll. Für 30 Tage wären die Angaben 30 und d einzutragen; Stunden: h; Minuten: m. Zusätzlich kann eine Passwort-Abfrage mit PasswordProtected="true" vorgelagert werden und der Dialog über die Attribute "PasswordButtonText" und "PasswordHeadline" individualisiert werden. Wird das Passwort zu oft falsch eingegeben (4 Versuche) wird der Link ungültig. Über MinutesCookieExpire wird angegeben wie lange die Sitzung ab Anmeldung über den Link gültig sein soll, bevor der Benutzer automatisch abgemeldet wird (Aber der Link ist unabhängig von der Session weiterhin gültig). Das Ergebnis wird über das Attribut "Link" ausgegeben und kann z.B. mit einer Print-Aktion in der Konsole des Batchpad ausgegeben werden. Hinweis: mydatastreamGetAccessLink muss in Verbindung mit mydatastreamInit verwendet werden. mydatastreamInit muss vor dieser Aktion ausgeführt werden.

```text-x-trilium-auto
<mydatastreamGetAccessLink SendTo="" FormularKey="" Filter="" ExpireValue="30" ExpireUnit="d|h|m" MinutesCookieExpire="30" Link="{@ResultLink}" PasswordProtected="false" PasswordQuestion="" PasswordAnswer="" PasswordButtonText="" PasswordHeadline="" RedirectUrl="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Wichtig: Wir empfehlen eine Legitimation in jedem erzeugtem Link mit anzugeben!

mydatastreamGetAuthLink
-----------------------

Die Aktion mydatastreamGetAuthLink erzeugt einen Link über den sich ein Benutzer direkt am mydatastream Portal anmeldet. "UserName" muss einem Benutzernamen aus der Benutzerverwaltung von mydatastream entsprechen und es darf sich nicht um einen Administrator-Account handeln (sonst wird bricht die Anfrage ab). Alle weiteren Angaben entsprechen den Attributen der Aktion mydatastreamGetAccessLink. Hinweis: mydatastreamGetAuthLink muss in Verbindung mit mydatastreamInit verwendet werden. mydatastreamInit muss vor dieser Aktion ausgeführt werden.

```text-x-trilium-auto
<mydatastreamGetAuthLink UserName="" ExpireValue="30" ExpireUnit="d|h|m" MinutesCookieExpire="30" Link="{@ResultLink}" PasswordProtected="false" PasswordQuestion="" PasswordAnswer="" PasswordButtonText="" PasswordHeadline="" RedirectUrl="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Es kann an den AuthLink eine Return-URL angehangen werden: "?ReturnUrl=". Die URL wird direkt nach der Authentifizierung geöffnet. Hinweis: App-Urls können über den Einstieg \[portalURL\]/pages/portal + öffnen der App in der Browser-Adresszeile angezeigt werden.

Wichtig: Wir empfehlen die Zwei-Faktor-Authentifizierung für jeden dem Link zugeordneten Benutzer zu aktivieren!

Sage100Init
-----------

Die Aktion Sage100Init Initialisiert den Zugriff auf den Sage 100 Applikationsserver.

```text-x-trilium-auto
<Sage100Init Server="" Port="" Datasource="" Mandant="" User="" Password="" Https="false" Timeout="00:02:00" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Sage100Execute
--------------

Mit der Aktion Sage100Execute kann eine Funktion auf dem Sage 100 Applikationsserver ausgeführt werden.

```text-x-trilium-auto
<Sage100Execute Service="" Config="" Data="" Message="" Mode="" Args="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Extension
---------

Die Aktion Extension erweitert die Funktion des Batchpad über die angegebene .dll Datei (Attribut: Name). 

```text-x-trilium-auto
<Extension Name="" Mode="" Args="" ResultMessage="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Um eine eigene Erweiterung erstellen muss man ein eigenes .Net Projekt anlegen welches das Interface IExtension aus der Assembly LogiSoft.Batchpad.Extension.dll implementieren

```text-x-trilium-auto
Public Class Extension
   Implements LogiSoft.Batchpad.Extension.IExtension
   Public Function Execute(Mode As String, Arguments As String, Variables As Dictionary(Of String, Object), Connections As Dictionary(Of String, DbConnection), DataTables As Dictionary(Of String, DataTable), ByRef ResultMessage As String, Optional IgnoreError As Boolean = False) As IExtension.Result Implements IExtension.Execute
       Try
           Select Case Mode
               Case "CountVariables"
                   ResultMessage = String.Format("Es sind {0} Variablen vorhanden", Variables.Count)
               Case "CountConnections"
                   ResultMessage = String.Format("Es sind {0} Connection vorhanden", Connections.Count)
               Case "CountDataTables"
                   ResultMessage = String.Format("Es sind {0} DataTable vorhanden", DataTables.Count)
               Case "CountKHKArtikel"
                   Dim oConnection As SqlConnection
                   If Connections.ContainsKey("{@myConnection}") Then
                       oConnection = Connections("{@myConnection}")
                       If oConnection IsNot Nothing Then
                           ResultMessage = String.Format("Es sind {0} Artikel vorhanden", Convert.ToInt32(sqlTools.Aggregate(oConnection, "KHKArtikel", "")))
                       End If
                   End If
               Case "ShowKHKArtikelMatchcodes"
                   Dim oConnection As SqlConnection
                   If Connections.ContainsKey("{@myConnection}") Then
                       oConnection = Connections("{@myConnection}")
                       If oConnection IsNot Nothing Then
                           Dim oReader As System.Data.Common.DbDataReader
                           oReader = sqlTools.GetDataReader(oConnection, "SELECT Matchcode FROM KHKArtikel")
                           If oReader IsNot Nothing Then
                               Do While oReader.Read
                                   ResultMessage += oReader.GetString((oReader.GetOrdinal("Matchcode"))) & vbCrLf
                               Loop
                           End If
                       End If
                   End If
               Case Else
                   ResultMessage = "Mode not found"
                   Return IExtension.Result.Failed
           End Select
           Return IExtension.Result.Successful
       Catch ex As Exception
           ResultMessage = ex.Message
           Return IExtension.Result.Failed
       End Try
   End Function
End Class
```