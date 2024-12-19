# Grafiken
Das Beispiel zeigt wie mit dem Batchpad Operationen auf einem Bild möglich sind. Dabei werden Bildwerte ausgelesen, das Bild manipuliert und in verschiedenen Formaten abgespeichert.

```text-x-trilium-auto
<Batch>
    <ImageLoad InputFile="E:\Original.jpg" />

    <ConditionTrue>
    
        <ImageGetWidth Condition="" Variable="{@ResultWidth}" />
        <ImageGetHeight Condition="" Variable="{@ResultHeight}" />

        <Print Text="Bildbreite: {@ResultWidth}" />
        <Print Text="Bildhoehe: {@ResultHeight}" />

        <ImageResizeToMaxSize MaxSize="1000" />

        <ImageToGrayscale />

        <ImageSaveAsPng OutputFile="E:\Kopie.png" />
        <ImageSaveAsBmp OutputFile="E:\Kopie.bmp" />
        <ImageSaveAsJpeg OutputFile="E:\Kopie.jpg" Quality="95" />
    
    </ConditionTrue>

</Batch>
```