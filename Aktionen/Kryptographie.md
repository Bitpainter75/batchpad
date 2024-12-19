# Kryptographie
GetMD5Hash
----------

Die Aktion **GetMD5Hash** berechnet den MD5-Hashwert eines angegebenen Wertes.

```text-x-trilium-auto
<GetMD5Hash Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Eingabewert, für den der MD5-Hash berechnet wird.
*   **Variable**: Variable, in der der berechnete MD5-Hash gespeichert wird.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<GetMD5Hash Value="HelloWorld" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Berechnet den MD5-Hashwert des Strings **HelloWorld** und speichert ihn in der Variablen **{@Result}**.

GetSHA1Hash
-----------

Die Aktion **GetSHA1Hash** berechnet den SHA1-Hashwert eines angegebenen Wertes.

```text-x-trilium-auto
<GetSHA1Hash Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Eingabewert, für den der SHA1-Hash berechnet wird.
*   **Variable**: Variable, in der der berechnete SHA1-Hash gespeichert wird.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<GetSHA1Hash Value="HelloWorld" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Berechnet den SHA1-Hashwert des Strings **HelloWorld** und speichert ihn in der Variablen **{@Result}**.

EncryptAES
----------

Die Aktion **EncryptAES** verschlüsselt einen Wert mit dem AES-Algorithmus.

```text-x-trilium-auto
<EncryptAES Value="" Key="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Wert, der verschlüsselt werden soll.
*   **Key**: Der Schlüssel mit dem die Verschlüsselung durchgeführt wird.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<EncryptAES Value="HelloWorld" Key="1234567890123456" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Verschlüsselt den String **HelloWorld** mit dem AES-Schlüssel **1234567890123456** und speichert den verschlüsselten Wert in **{@Result}**.

DecryptAES
----------

Die Aktion **DecryptAES** entschlüsselt einen mit AES verschlüsselten Wert.

```text-x-trilium-auto
<DecryptAES Value="" Key="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Wert, der entschlüsselt werden soll.
*   **Key**: Der Schlüssel mit dem die Entschlüsselung durchgeführt wird.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<DecryptAES Value="EncryptedValue" Key="1234567890123456" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Entschlüsselt den Wert **"EncryptedValue"** mit dem AES-Schlüssel **"1234567890123456"** und speichert den entschlüsselten Wert in **{@Result}**.

EncodeBase64
------------

Die Aktion **EncodeBase64** kodiert einen Wert im Base64-Format.

```text-x-trilium-auto
<EncodeBase64 Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Wert, der kodiert werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<EncodeBase64 Value="HelloWorld" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Kodiert den String **HelloWorld** im Base64-Format und speichert das Ergebnis in **{@Result}**.

DecodeBase64
------------

Die Aktion **DecodeBase64** dekodiert einen Base64-kodierten Wert.

```text-x-trilium-auto
<DecodeBase64 Value="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Value**: Der Wert, der dekodiert werden soll.
*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<DecodeBase64 Value="SGVsbG9Xb3JsZA==" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Dekodiert den Base64-kodierten Wert **SGVsbG9Xb3JsZA==** und speichert das Ergebnis in **{@Result}**.

GetRandomKey
------------

Die Aktion **GetRandomKey** erzeugt einen zufälligen Schlüssel bestehend aus den Zeichen 0-9 und A-F.

```text-x-trilium-auto
<GetRandomKey Length="" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<GetRandomKey Length="16" Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erzeugt einen 16 Zeichen langen zufälligen Schlüssel und speichert ihn in **{@Result}**.

CreateNewGuid
-------------

Die Aktion **CreateNewGuid** erzeugt eine neue GUID.

```text-x-trilium-auto
<CreateNewGuid Condition="" Variable="{@Result}" IgnoreError="false" />
```

Attribute:

*   **Condition**: (Optional) Eine Bedingung, die erfüllt sein muss, damit die Aktion ausgeführt wird.
*   **Variable**: Die Variable, in der das Ergebnis gespeichert wird.
*   **IgnoreError**: (Optional) Gibt an, ob Fehler ignoriert werden sollen. Standardwert: false.

Beispiel:

```text-x-trilium-auto
<CreateNewGuid Condition="" Variable="{@Result}" IgnoreError="false" />
```

Erzeugt eine neue GUID und speichert sie in **{@Result}**. Beispielausgabe: **d94f3f01-2b1f-4a8e-b19d-c3a953f12345**.