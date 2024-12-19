# Internet
HasInternetConnection
---------------------

Die Aktion HasInternetConnection prüft, ob eine Verbindung zu dem Internet aufgebaut werden kann. Falls ja wird true über das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<HasInternetConnection Condition="" Variable="{@Result}" IgnoreError="false" />
```

Ping
----

Die Aktion Ping prüft, ob eine Verbindung zu einer bestimmten Adresse per Ping durchgeführt werden kann. Falls ja wird true über das Attribut Variable zurückgegeben.

```text-x-trilium-auto
<Ping Address="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

GetLocalIPAddress
-----------------

Die Aktion GetLocalIPAddress liefert über die Variable die lokale IP Adresse der Netzwerkkarte die mit dem Standardgateway verbunden ist zurück.

```text-x-trilium-auto
<GetLocalIPAddress Condition="" Variable="{@Result}" IgnoreError="false" />
```

FileDownload
------------

Die Aktion FileDownload lädt die angegebene Datei aus dem Internet (Attribut: Source) und speichert die Datei in das angegebene Zielverzeichnis (Attribut: Destination).

```text-x-trilium-auto
<FileDownload Source="" Destination="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

InitSmtp
--------

Die Aktion InitSmtp stellt eine Verbindung mit dem angegebenen Smtp-Server her (Attribut: Server). Falls die Authentifizierung aktiviert ist (Attribut: Authentification) müssen für die Attribute Login und Passwort gültige Anmeldedaten eingetragen werden. Über das Attribut E-Mail kann die Absender E-Mail Adresse hinterlegt werden. Für das Attribut DisplayName wird der Anzeigename des Absenders hinterlegt, für das Attribut Port kann der für den SMTP-Server gültige Port eingetragen werden und über das Attribut EnableSSL wird festgelgt ob die Verbindung verschlüsselt werden soll.

```text-x-trilium-auto
<InitSmtp DisplayName="" Email="" Login="" Password="" Server="" Port="25" EnableSSL="false" Authentification="true" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SendMail
--------

Über die Aktion SendMail wird eine E-Mail an die in dem Attribut To hinterlegten E-Mail-Adresse versendet. Über das Attribut Cc wird eine Kopie, und über Bcc eine Blindkopie an die jeweils hinterlegte E-Mail versendet. Der Betreff der E-Mail wird über das Attribut Subject angegeben, die Nachricht über das Attribut Body. Enthält die Nachricht HTML Formatierungen wird die HTML Formatierung über das Attribut IsBodyHtml angegeben werden. Der E-Mail kann zudem über das Attribut Attachment eine Datei angehangen werden. Das Attribut Template bietet die Möglichkeit den Pfad zu einem Template zu hinterlegen. In dem Template können die aus den Batchpad Skripten typischen Variablen Bezeichnungen eingetragen werden wie z.B. {@Name}. Wird das Template geladen, werden diese Platzhalter, mit denen zur Laufzeit hinterlegten gleichnamigen Variablen, ersetzt. Das Template kann als HTML formatiertes Dokument oder als reines Textdokument hinterlegt werden. Hinweis: Das Template kann auch direkt im Batchpad Skript angelegt werden, siehe Abschnitt HTML in diesem Lexikoneintrag.

```text-x-trilium-auto
<SendMail To="" Cc="" Bcc="" Subject="" Body="" IsBodyHtml="false" Attachment="" Template="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

SendHttpRequest
---------------

Über die Aktion SendHttpRequest können Request an die in dem Attribut Url hinterlegte Adresse versendet werden. Abhängig von der Methode (Attribut: Method) können für z.B. für die Methode GET URL-Parameter über das Attribut UrlParameter angehangen werden. Für die Methode POST können die zu übertragenden Werte in dem Attribut Request angegeben werden. Der Content-Type des Request kann über das das Attribut Format bestimmt werden. Ist die URL durch eine Http-Authentifizierung geschützt, können die Anmeldedaten über die Attribute User und Password hinterlegt werden.

```text-x-trilium-auto
<SendHttpRequest Url="" UrlParameter="" Response="" Request="" Method="GET" Format="" User="" Password="" Condition="" Variable="{@Result}" IgnoreError="false" Header="{@HeaderList}" />
```

  
Über das Header-Attribut können Header Informationen mit angegeben werden die an den Server geschickt werden solle:

```text-x-trilium-auto
<KeyValueListAdd Data="{@HeaderList}" Key="Key1" Value="1234" />
```

SendTcpClientMessage
--------------------

Die Aktion **SendTcpClientMessage** ermöglicht das Senden einer Nachricht über eine TCP-Client-Verbindung an einen Server und empfängt optional eine Antwort.

```text-x-trilium-auto
<SendTcpClientMessage IPAddress="" Port="" Timeout="" Message="" Response="{@Response}" Variable="{@Result}" />
```

Attribute:

*   **IPAddress**: Die IP-Adresse des Servers, zu dem die Verbindung hergestellt wird.
*   **Port**: Der Port des Servers, auf den die Verbindung abzielt.
*   **Timeout**: Die maximale Wartezeit in Millisekunden, bevor die Verbindung abbricht.
*   **Message**: Die Nachricht, die an den Server gesendet werden soll.
*   **Response**: (Optional) Variable, in der die Antwort des Servers gespeichert wird.
*   **Variable**: Variable, in der gespeichert wird, ob die Nachricht erfolgreich gesendet wurde (true oder false).

Beispiel:

```text-x-trilium-auto
<SendTcpClientMessage IPAddress="192.168.1.10" Port="8080" Timeout="5000" Message="Hello, Server!" Response="{@Response}" Variable="{@Result}" />
```

Sendet die Nachricht **"Hello, Server!"** an den Server mit der IP-Adresse **192.168.1.10** und Port **8080**. Die Antwort wird in **{@Response}** gespeichert, und der Status der Aktion (true oder false) wird in **{@Result}** gespeichert.

SSLCertificateValidation
------------------------

Die Aktion **SSLCertificateValidation** steuert, ob SSL-Zertifikate während einer HTTPS-Verbindung überprüft werden sollen.

```text-x-trilium-auto
<SSLCertificateValidation Ignore="true" Variable="{@Result}" />
```

Attribute:

*   **Ignore**: Gibt an, ob die Validierung von SSL-Zertifikaten ignoriert wird (true oder false).
*   **Variable**: (Optional) Variable, in der gespeichert wird, ob die Aktion erfolgreich ausgeführt wurde (true oder false).

Beispiel:

```text-x-trilium-auto
<SSLCertificateValidation Ignore="true" Variable="{@Result}" />
```

Setzt die SSL-Zertifikatüberprüfung auf **ignorieren**. Dies kann nützlich sein, wenn mit selbstsignierten Zertifikaten gearbeitet wird oder wenn keine Validierung erforderlich ist.

HttpTextEscape
--------------

Die Aktion **HttpTextEscape** wandelt einen Text in eine HTTP-escaped Zeichenkette um (z. B. für URLs oder HTTP-Parameter).

```text-x-trilium-auto
<HttpTextEscape Text="" Variable="{@Result}" />
```

Attribute:

*   **Text**: Der Text, der in eine HTTP-escaped Zeichenkette konvertiert werden soll.
*   **Variable**: Variable, in der die konvertierte Zeichenkette gespeichert wird.

Beispiel:

```text-x-trilium-auto
<HttpTextEscape Text="Hello, World!" Variable="{@Result}" />
```

Konvertiert den Text **Hello, World!** in eine HTTP-escaped Zeichenkette, z. B. **Hello%2C%20World%21**, und speichert sie in **{@Result}**.

HttpTextUnescape
----------------

Die Aktion **HttpTextUnescape** wandelt eine HTTP-escaped Zeichenkette in ihren ursprünglichen Text um.

```text-x-trilium-auto
<HttpTextUnescape Text="" Variable="{@Result}" />
```

Attribute:

*   **Text**: Die HTTP-escaped Zeichenkette, die dekodiert werden soll.
*   **Variable**: Variable, in der der dekodierte Text gespeichert wird.

Beispiel:

```text-x-trilium-auto
<HttpTextUnescape Text="Hello%2C%20World%21" Variable="{@Result}" />
```

Dekodiert die Zeichenkette **Hello%2C%20World%21** in den ursprünglichen Text **Hello, World!** und speichert ihn in **{@Result}**.

SSHExecuteCommand
-----------------

Die Aktion **SSHExecuteCommand** führt einen Befehl auf einem entfernten Server über eine SSH-Verbindung aus.

```text-x-trilium-auto
<SSHExecuteCommand Command="" Servername="" User="" Password="" Port="22" Sudo="false" SudoPassword="" Message="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Command**: Der auszuführende Befehl auf dem Remote-Server.
*   **Servername**: Der Hostname oder die IP-Adresse des Remote-Servers.
*   **User**: Der Benutzername für die SSH-Authentifizierung.
*   **Password**: Das Passwort für die SSH-Authentifizierung.
*   **Port**: Der SSH-Port des Servers (Standardwert: 22).
*   **Sudo**: Gibt an, ob der Befehl mit **sudo** ausgeführt werden soll (true oder false).
*   **SudoPassword**: (Optional) Das Passwort für die **sudo**\-Authentifizierung, falls benötigt.
*   **Message**: Variable, in der die Ausgabe des ausgeführten Befehls gespeichert wird.
*   **Condition**: (Optional) Steuert die Ausführung der Aktion. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen.
*   **Variable**: Variable, in der gespeichert wird, ob der Befehl erfolgreich ausgeführt wurde (true oder false).
*   **IgnoreError**: (Optional) Gibt an, ob Fehler bei der Ausführung ignoriert werden sollen (true oder false).

Beispiel:

```text-x-trilium-auto
<SSHExecuteCommand Command="ls -la /var/log" Servername="192.168.1.100" User="root" Password="securepassword123" Port="22"  Sudo="true" SudoPassword="securepassword123" Message="{@ResultMessage}" Condition="" Variable="{@Result}" IgnoreError="false" />
```

*   Führt den Befehl **ls -la /var/log** auf dem Server **192.168.1.100** aus.
*   Der Benutzer **root** wird verwendet, und die Authentifizierung erfolgt über das Passwort **securepassword123**.
*   Der Befehl wird mit **sudo** ausgeführt, und das **sudoPassword** ist ebenfalls **securepassword123**.
*   Die Ausgabe des Befehls wird in der Variable **{@ResultMessage}** gespeichert.
*   Der Status der Ausführung (true/false) wird in **{@Result}** gespeichert.

Besondere Hinweise:

*   Der Standard-SSH-Port ist **22**, kann aber durch Angabe eines anderen Werts angepasst werden.
*   Wenn **Sudo="true"** verwendet wird, muss das Attribut **SudoPassword** angegeben sein, falls der Benutzer ein Passwort für sudo benötigt.
*   Die Ausgabe des Befehls, wie Fehlermeldungen oder Standardausgabe, wird in **Message** gespeichert.

HTML
----

Der Tag HTML bietet die Möglichkeit direkt in dem Batchpad-Skript ein HTML-Dokument zu hinterlegen. Das Dokument kann anschließend in der Form {@HTML:Beispiel} angesprochen werden. Wobei wie in dem Beispiel die Zeichenfolge "Beispiel" als Wert für das Attribut Name angegeben werden muss.

```text-x-trilium-auto
<HTML Name="Beispiel">
...
</HTML>
```