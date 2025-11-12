---
title: Dynamische Suchen
description: Erfahren Sie, was dynamische Suchen sind und wie Sie sie aktivieren. Umfasst Provider, Attribute für Mobilgeräte und Betriebssystemtypen.
exl-id: 12327239-06a2-4092-b27d-b94da39abf30
feature: Data Feeds
source-git-commit: 705a1716ed0205594fc6c75023c8805024ce7df7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 2%

---

# Dynamische Suchen

Dynamische Suchen ermöglichen es Ihnen, zusätzliche Suchdateien in Ihrem Daten-Feed zu erhalten, die sonst nicht verfügbar sind. Mit dieser Einstellung können die folgenden Lookup-Tabellen mit jeder Daten-Feed-Datei gesendet werden:

* **Betreibername**: Bietet zusätzlichen Kontext für die `carrier`. Der eingeschlossene Dateiname lautet `carrier.tsv`.
* **Mobile-Attribute**: Bietet zusätzlichen Kontext für die Spalte &quot;`mobile_id`&quot;, einschließlich aller für jedes Mobilgerät verfolgten Funktionen. Der eingeschlossene Dateiname lautet `mobile_attributes.tsv`.
* **Betriebssystemtyp**: Bietet einen alternativen Kontext für die `os`. Sowohl `operating_systems.tsv` als auch `operating_system_type.tsv` verwenden die `os` als Schlüssel. Nur `operating_system_type.tsv` ist eine dynamische Suche.

## Dynamische Suchen aktivieren {#enable-dynamic-lookups}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="aa_datafeed_dynamic_lookups"
>title="Dynamische Suchen aktivieren"
>abstract="Wählen Sie diese Option, um zusätzliche Lookup-Dateien in Ihrem Daten-Feed zu erhalten, die sonst nicht verfügbar sind. Mit dieser Einstellung können die folgenden Lookup-Tabellen mit jeder Daten-Feed-Datei gesendet werden:<ul><li>Betreibername</li><li>Mobile Attribute</li><li>Betriebssystemtyp</li></ul>"

<!-- markdownlint-enable MD034 -->

Wenn Sie die genannten Lookup-Dateien erhalten möchten, müssen Sie alle folgenden Voraussetzungen erfüllen:

* Die Schlüsselspalte muss im Daten-Feed enthalten sein.
   * `carrier.tsv` müssen Sie `carrier` einbeziehen.
   * `mobile_attributes.tsv` müssen Sie `mobile_id` einbeziehen.
   * `operating_system_type.tsv` müssen Sie `os` einbeziehen.
* Die folgenden Spalten müssen **ausgeschlossen** sein. Wenn eine dieser Spalten im Daten-Feed enthalten ist, wird die `mobile_attributes.tsv` dynamische Suche nicht einbezogen.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

Sobald Ihr Daten-Feed die Spalten-Ein- und Ausschlussanforderungen erfüllt, wenden Sie sich mit der Daten-Feed-ID und der Anfrage an die Kundenunterstützung, um dynamische Suchen zu aktivieren.

## Kopfzeilenreferenz nachschlagen

Die Spaltenüberschriften für diese Lookup-Dateien ändern sich im Laufe der Zeit nicht, sodass keine Kopfzeilen in jeder Daten-Feed-Datei enthalten sind. Verwenden Sie diese Spaltenüberschriften als Referenz oder laden Sie die entsprechende `.tsv` herunter.

+++**Betreibername**
Laden Sie [carrier_headers.tsv](assets/carrier_headers.tsv) herunter oder verweisen Sie auf die folgenden Kopfzeilen.

`carrier`
`Carrier Name`
+++

+++**Attribute für Mobilgeräte**
Laden Sie [mobile_attributes_headers.tsv](assets/mobile_attributes_headers.tsv) herunter oder verweisen Sie auf die folgenden Kopfzeilen.

`mobile_id`
`Manufacturer`
`Device`
`Device Type`
`Operating System`
`Diagonal Screen Size`
`Screen Height`
`Screen Width`
`Cookie Support`
`Color Depth`
`MP3 Audio Support`
`AAC Audio Support`
`AMR Audio Support`
`Midi Monophonic Audio Support`
`Midi Polyphonic Audio Support`
`QCELP Audio Support`
`GIF87 Image Support`
`GIF89a Image Support`
`PNG Image Support`
`JPG Image Support`
`3GPP Video Support`
`MPEG4 Video Support`
`3GPP2 Video Support`
`WMV Video Support`
`MPEG4 Part 2 Video Support`
`Stream MP4 AAC LC Video Support`
`Stream 3GP H264 Level 10b Video Support`
`Stream 3GP AAC LC Video Support`
`3GP AAC LC Video Support`
`Stream MP4 H264 Level 11 Video Support`
`Stream MP4 H264 Level 13 Video Support`
`Stream 3GP H264 Level 12 Video Support`
`Stream 3GP H264 Level 11 Video Support`
`Stream 3GP H264 Level 10 Video Support`
`Stream 3GP H264 Level 13 Video Support`
`3GP AMR NB Video Support`
`3GP AMR WB Video Support`
`MP4 H264 Level 11 Video Support`
`3GP H263 Video Support`
`MP4 H264 Level 13 Video Support`
`Stream 3GP H263 Video Support`
`Stream 3GP AMR WB Video Support`
`3GP H264 Level 10b Video Support`
`MP4 ACC LC Video Support`
`Stream 3GP AMR NB Video Support`
`3GP H264 Level 10 Video Support`
`3GP H264 Level 13 Video Support`
`3GP H264 Level 11 Video Support`
`3GP H264 Level 12 Video Support`
`Stream HTTP Live Streaming Video Support`
+++

+++**Betriebssystemtyp**
Laden Sie [Operating_System_Type_Headers.tsv](assets/operating_system_type_headers.tsv) herunter oder verweisen Sie auf die folgenden Header.

`os`
`Operating System Type`
+++
