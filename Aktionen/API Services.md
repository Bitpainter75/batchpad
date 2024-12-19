# API Services
SendMessageToGotify
-------------------

Die Aktion **SendMessageToGotify** sendet eine Nachricht an einen Gotify-Server.

```text-x-trilium-auto
<SendMessageToGotify Url="" Token="" Title="" Message="" Priority="2" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Url**: Die URL des Gotify-Servers.
*   **Token**: Der API-Token für die Authentifizierung.
*   **Title**: Der Titel der Nachricht.
*   **Message**: Der Inhalt der Nachricht.
*   **Priority**: Die Priorität der Nachricht (Standardwert: 2).
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<SendMessageToGotify Url="https://gotify.example.com" Token="abcdef123456" Title="Alarm" Message="Ein Fehler ist aufgetreten" Priority="5" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Sendet eine Nachricht mit dem Titel **Alarm** und der Priorität **5** an den Gotify-Server.

SendMessageToNtfy
-----------------

Die Aktion **SendMessageToNtfy** sendet eine Nachricht an einen Ntfy-Server.

```text-x-trilium-auto
<SendMessageToNtfy Url="" Token="" Title="" Message="" Priority="default" Tags="" Click="" Markdown="false" Delay="0" Attach="" Icon="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Url**: Die URL des Ntfy-Servers.
*   **Token**: Der API-Token für die Authentifizierung.
*   **Title**: Der Titel der Nachricht.
*   **Message**: Der Inhalt der Nachricht.
*   **Priority**: Die Priorität der Nachricht (default, high, low).
*   **Tags**: (Optional) Eine kommagetrennte Liste von Tags.
*   **Click**: (Optional) URL, die geöffnet wird, wenn auf die Benachrichtigung geklickt wird.
*   **Markdown**: (Optional) Gibt an, ob der Nachrichteninhalt als Markdown interpretiert werden soll. Mögliche Werte sind true oder false. 
*   **Attach**: (Optional) Eine URL zu einer Datei, die mit der Nachricht verknüpft wird. Der Ntfy-Server lädt die Datei herunter und stellt sie als Anhang bereit.
*   **Icon**: (Optional) Eine URL zu einem benutzerdefinierten Symbol, das in der Benachrichtigung angezeigt wird.
*   **Delay**: (Optional) Verzögert die Zustellung der Nachricht um eine bestimmte Zeitspanne. Angabe in Sekunden.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<SendMessageToNtfy Url="https://ntfy.example.com/mytopic" Token="your_api_token" Title="System Alert" Message="Disk space is running low." Priority="high" Tags="warning,disk" Click="https://example.com/disk-usage" Attach="https://example.com/reports/disk-usage.pdf"  Icon="https://example.com/icons/warning.png" Markdown="true" Delay="60" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Dieses Beispiel sendet eine Nachricht mit dem Titel **System Alert** und dem Inhalt **Disk space is running low.** an das Ntfy-Thema **mytopic**. Die Nachricht hat eine hohe Priorität, ist mit den Tags **warning** und **disk** versehen und enthält einen Anhang sowie ein benutzerdefiniertes Symbol. Beim Klicken auf die Benachrichtigung wird die angegebene URL geöffnet. Der Nachrichteninhalt wird als Markdown interpretiert, und die Zustellung erfolgt mit einer Verzögerung von 60 Sekunden.

SendMailViaSendGrid
-------------------

Die Aktion **SendMailViaSendGrid** versendet eine E-Mail über die SendGrid-API.

```text-x-trilium-auto
<SendMailViaSendGrid ApiKey="" From="" To="" Cc="" Bcc="" Subject="" Body="" IsBodyHtml="false" Attachment="" Template="" Variable="{@Result}" />
```

Attribute:

*   **ApiKey**: Der API-Schlüssel für den Zugriff auf die SendGrid-API.
*   **From**: Die Absenderadresse der E-Mail.
*   **To, Cc, Bcc**: Kommagetrennte Listen von Empfängeradressen.
*   **Body**: Der Inhalt der E-Mail.
*   **IsBodyHtml**: Gibt an, ob der Nachrichteninhalt HTML ist (true oder false).
*   **Attachment:** (Optional) Kommagetrennte Liste mit Pfaden zu Dateien, die angehängt werden.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: (Optional) Eine Variable, in der gespeichert wird, ob die Aktion erfolgreich durchgeführt wurde. true oder false.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<SendMailViaSendGrid ApiKey="SG.abcdef123456" From="noreply@example.com" To="user@example.com" Subject="Willkommen" Body="Willkommen bei unserem Service!" IsBodyHtml="true" Variable="{@Result}" />
```

Sendet eine E-Mail mit dem Betreff **Willkommen** über SendGrid.

GoogleMapsCoordinates
---------------------

Die Aktion **GoogleMapsCoordinates** ruft die geografischen Koordinaten einer Adresse ab.

```text-x-trilium-auto
<GoogleMapsCoordinates Address="" ApiKey="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Address**: Die Adresse, deren Koordinaten abgerufen werden sollen.
*   **ApiKey**: Der API-Schlüssel für den Zugriff auf die Google Maps API.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<GoogleMapsCoordinates Address="Maibachstrasse 7, 35683 Dillenburg" ApiKey="AIzaSy123456" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Ruft die Breiten- und Längengradkoordinaten der angegebenen Adresse ab.

GoogleTranslateText
-------------------

Die Aktion **GoogleTranslateText** übersetzt einen Text in eine andere Sprache.

```text-x-trilium-auto
<GoogleTranslateText Text="" ApiKey="" SourceLanguage="" TargetLanguage="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Text**: Der zu übersetzende Text.
*   **SourceLanguage**: Die Sprache des Ausgangstextes (z. B. en für Englisch).
*   **TargetLanguage**: Die Zielsprache (z. B. de für Deutsch).
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<GoogleTranslateText Text="Hello, how are you?" ApiKey="AIzaSy123456" SourceLanguage="en" TargetLanguage="de" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Übersetzt den Text **Hello, how are you?** von Englisch nach Deutsch.

ChatGPTSendPrompt
-----------------

Die Aktion **ChatGPTSendPrompt** sendet eine Anfrage (Prompt) an die ChatGPT-API und gibt die Antwort zurück.

```text-x-trilium-auto
<ChatGPTSendPrompt Prompt="" ApiKey="" Model="gpt-3.5-turbo" Temperature="0.7" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Prompt**: Der Text der Anfrage, die an ChatGPT gesendet wird.
*   **ApiKey**: Der API-Schlüssel für den Zugriff auf die OpenAI API.
*   **Model**: Das zu verwendende Modell (gpt-3.5-turbo, gpt-4).
*   **Temperature**: Steuerung der Kreativität der Antwort (Standard: 0.7).
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<ChatGPTSendPrompt Prompt="Schreibe ein Gedicht über den Winter." ApiKey="sk-abcdef123456" Model="gpt-4" Temperature="0.8" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Sendet den Prompt **Schreibe ein Gedicht über den Winter.** an ChatGPT und gibt die Antwort in **{@Result}** zurück.