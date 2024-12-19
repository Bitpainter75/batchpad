# Bildmanipulation
ImageLoad
---------

Die Aktion ImageLoad lädt die angegebene Bild-Datei (Attribut: InputFile) in den Arbeitsspeicher. Die geladene Datei steht implizit für weitere Aktionen auf dieser Datei zur Verfügung und wird nicht über eine Variable angegeben. Es werden folgende Bildformate unterstützt: BMP, GIF, JPEG, PNG und TIFF.

```text-x-trilium-auto
<ImageLoad InputFile="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageSaveAsBmp
--------------

Die Aktion ImageSaveAsBmp speichert eine Bilddatei unter dem angegebenen Pfad (Attribut: OutputFile) im Bmp Format ab. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt.

```text-x-trilium-auto
<ImageSaveAsBmp OutputFile="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageSaveAsPng
--------------

Die Aktion ImageSaveAsPng speichert eine Bilddatei unter dem angegebenen Pfad (Attribut: OutputFile) im Png Format ab. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt.

```text-x-trilium-auto
<ImageSaveAsPng OutputFile="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageSaveAsJpeg
---------------

Die Aktion ImageSaveAsJpeg speichert eine Bilddatei unter dem angegebenen Pfad (Attribut: OutputFile) im Jpeg Format ab. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt.

Über das Attribut Quality wird die Qualität des zu speichernden Jpeg angegeben. Der Wertebereich von dem Attribut Quality liegt zwischen 0 und 100. Wobei der Wert 100 für die beste Qualität steht.

```text-x-trilium-auto
<ImageSaveAsJpeg OutputFile="" Quality="75" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageGetWidth
-------------

Die Aktion ImageGetWidth gibt über das Attribut Variable die Breite einer Bilddatei zurück. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt.

```text-x-trilium-auto
<ImageGetWidth Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageGetHeight
--------------

Die Aktion ImageGetHeight gibt über das Attribut Variable die Höhe einer Bilddatei zurück. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt.

```text-x-trilium-auto
<ImageGetHeight Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageCrop
---------

Die Aktion ImageCrop führt die Operation "Zuschneiden" auf einer Bilddatei aus. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Der auszuschneidende Bereich wird über die Höhe (Attribut Height) und die Weite (Attribut Width) bestimmt. Zudem kann die Position des auszuschneidenden Bereiches vertikal (Attribut Y) und horizontal (Attribut X) positioniert werden. Wobei die Werte X="0" und Y="0" einer Positionierung des auszuschneidenden Bereiches in der oberen linken Ecke gleichkommt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageCrop Width="" Height="" X="" Y="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageResize
-----------

Die Aktion ImageResize führt die Operation "Größe verändern" auf einer Bilddatei aus. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die neue Höhe des Bildes wird über das Attribut Height und die neue Breite des Bildes über das Attribut Width angegeben. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageResize Width="" Height="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageResizeToMaxSize
--------------------

Die Aktion ImageResizeToMaxSize verändert die Bildgröße und bezieht sich dabei auf den größeren Wert der zwei Werte Breite und Höhe eines Bildes. Von den zwei Werten wird der größere Wert auf die angegebene Größe in Pixeln (Attribut: MaxSize) geändert und ist der Bezugswert für den anderen Wert. Der andere Wert wird dann im Verhältnis zu der Änderung des Bezugswertes neu berechnet. Hinweis: Der Bezugswert wird entweder vergrößert oder verkleinert, um dem angegebenen Wert in dem Attribut MaxSize zu entsprechen.

```text-x-trilium-auto
<ImageResizeToMaxSize MaxSize="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageRotate90
-------------

Die Aktion ImageRotate90 führt die Operation "Rotierung um 90 Grad im Uhrzeigersinn" auf einer Bilddatei aus. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageRotate90 Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageRotate180
--------------

Die Aktion ImageRotate180 führt die Operation "Rotierung um 180 Grad im Uhrzeigersinn" auf einer Bilddatei aus. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageRotate180 Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageRotate270
--------------

Die Aktion ImageRotate270 führt die Operation "Rotierung um 270 Grad im Uhrzeigersinn" auf einer Bilddatei aus. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageRotate270 Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageFlipX
----------

Die Aktion ImageFlipX führt die Operation "Spiegeln anhand der horizontalen Achse" durch. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageFlipX Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageFlipY
----------

Die Aktion ImageFlipY führt die Operation "Spiegeln anhand der vertikalen Achse" durch. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageFlipY Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageFlipXY
-----------

Die Aktion ImageFlipXY führt die Operation "Spiegeln anhand der vertikalen Achse und horizontalen Achse" durch. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageFlipXY Condition="" Variable="{@Result}" IgnoreError="false" />
```

ImageToGrayscale
----------------

Die Aktion ImageToGrayscale führt die Operation "Konvertierung der Farbwerte zu Graustufen" durch. Die Bilddatei wird dabei implizit über die Aktion ImageLoad bereitgestellt. Die verarbeitete Bilddatei wird implizit für weitere Aktionen bereitgestellt und wird nicht über eine Variable angegeben.

```text-x-trilium-auto
<ImageToGrayscale Condition="" Variable="{@Result}" IgnoreError="false" />
```

ConvertToIcon
-------------

Die Aktion ConvertToIcon konvertiert eine beliebige Grafik in eine .ico Datei. Dabei kann über das  Attribut Size noch die Größe in Pixel des Icons festgelegt werden.

```text-x-trilium-auto
<ConvertToIcon InputFile="" OutputFile="" Size="16" Condition="" Variable="{@Result}" IgnoreError="false" />
```