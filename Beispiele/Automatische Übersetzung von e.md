# Automatische Übersetzung von einem XML Dokument in verschiedene Sprachen
Das Beispiel zeigt eine automatische Übersetzung von einem XML-Dokument. Dabei wird das XML-Dokument ausgelesen und die zu überstenden Einträge an den google translate Service gesendet.  
Die Sprachen werden in einem Array gehalten und pro Sprache wird ein XML-Dokument mit den entsprechenden Übersetzungen generiert.

Im Anhang befindet sich das Dokument sample.xml, dass für die Ausführung des Beispiels verwendet werden kann.

```text-x-trilium-auto
<Batch>
    <!-- Parameter Sprachen und API-Key für google Translate -->
    <Set Variable="{@Languages}" Value="fr,it,pt,es,en" />
    <Set Variable="{@GoogleAPIKey}" Value="" />

    <!-- Die Sprachen in ein Array überführen, um über die Srachen iterieren zu können -->
     <StringSplit Data="{@myData}" Value="{@Languages}" Delimiter="," SplitLines="false" RemoveEmptyValues="false" DataCount="{@ResultCount}" />

    <ForEach Data="{@myData}" >
        <!-- über jede Sprache iterieren z.B. "en" -->
        <Set Variable="{@CurrentLanguage}" Value="{@Data:Value}" Condition=""  />
        <!-- Das zu übersetzende Dokument öffnen und das Body Element abrufen, wird für jede Übersetzung erneut geöffnet -->
        <XMLOpenDocument Document="{@myXml}" Content="" File="sample.xml" />
        <XMLGetElement Document="{@myXml}" Data="{@RootNode}" Path="/xliff/file/body" />
        
        <ForEach Data="{@RootNode}" >
            <!-- Über jeden zu übersetzenden Eintrag iterieren (Einträge befinden sich in sample.xml) -->
            <XMLGetAttribute Document="{@myXml}" Data="{@Data:Node}" Attribute="id" Variable="{@IDResult}" />
            <XMLGetElement Document="{@myXml}" Data="{@TransUnitChild}" Path="/xliff/file/body/trans-unit[@id='{@IDResult}']" />
            <XMLGetElement Document="{@myXml}" Data="{@ChildNode}" Path="/xliff/file/body/trans-unit[@id='{@IDResult}']/source" />
               
            <!-- Den String auslesen der übersetzt werden soll -->
            <XMLGetElementContent  Document="{@myXml}" Data="{@ChildNode}" InnerXml="true" Variable="{@Result}" />
            <StringTrim Value="{@Result}" Variable="{@Result}" />
            
            <!-- Den zu übersetzenden String an den google translate Server senden und Antwort erhalten -->
            <SendHttpRequest Url="https://translation.googleapis.com/language/translate/v2" UrlParameter="q={@Result}&amp;target={@CurrentLanguage}&amp;key={@GoogleAPIKey}" Response="{@ResponseResult}" Request="" Method="GET" Format="xml" Variable="{@RequestResult}" IgnoreError="true" />
                       
            <ConditionTrue Condition="{@RequestResult}">
                <!-- Das Ergebnis der Übersetzung von JSON zu XML umwandeln-->
                <JSONConvertToXML Document="{@myJsonToXML}" Json="{@ResponseResult}"  />
                <!-- Den übersetzten Wert auslesen -->
                <XMLGetElement Document="{@myJsonToXML}" Data="{@TranslationNode}" Path="/root/data/translations/item/translatedText" />
                <XMLGetElementContent Document="{@myJsonToXML}" Data="{@TranslationNode}" InnerXml="true" Variable="{@ResultTranslation}" />
                <!-- Dem Dokument, das später abgespeichert wird, ein Element mit der Übersetzung hinzufügen -->
                <XMLAddElement Document="{@myXml}" ParentData="{@TransUnitChild}" Data="{@TargetNode}" Name="target"/>
                <XMLSetElementContent Document="{@myXml}" Data="{@TargetNode}" Content="{@ResultTranslation}" />        
            </ConditionTrue>
        </ForEach>

        <!-- Das finale Dokument pro Sprache abspeichern -->
        <XMLSaveDocument Document="{@myXml}" File="sample.{@CurrentLanguage}.xml"  />        
    </ForEach>
</Batch>
```