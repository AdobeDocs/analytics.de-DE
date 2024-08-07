---
title: Dynamische Suchen
description: Erfahren Sie, was dynamische Suchen sind und wie sie aktiviert werden. Enthält Träger, Attribute für Mobilgeräte und Betriebssystemtypen.
exl-id: 12327239-06a2-4092-b27d-b94da39abf30
feature: Data Feeds
source-git-commit: 6b8366b451be1612331f517ee80fd57744deafdc
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Dynamische Suchen

Mit dynamischen Suchen können Sie zusätzliche Lookup-Dateien in Ihrem Daten-Feed erhalten, wenn sie andernfalls nicht verfügbar sind. Mit dieser Einstellung können die folgenden Suchtabellen mit jeder Daten-Feed-Datei gesendet werden:

* **Betreibername**: Stellt zusätzlichen Kontext für die Spalte `carrier` bereit. Der einbezogene Dateiname ist `carrier.tsv`.
* **Mobile Attribute**: Bietet zusätzlichen Kontext für die Spalte `mobile_id`, einschließlich aller für jedes Mobilgerät verfolgten Funktionen. Der einbezogene Dateiname ist `mobile_attributes.tsv`.
* **Betriebssystemtyp**: Stellt einen alternativen Kontext für die Spalte `os` bereit. Sowohl `operating_systems.tsv` als auch `operating_system_type.tsv` verwenden die Spalte `os` als Schlüssel, aber nur `operating_system_type.tsv` ist eine dynamische Suche.

## Dynamische Suchen aktivieren

Wenn Sie die erwähnten Lookup-Dateien erhalten möchten, müssen Sie alle folgenden Voraussetzungen erfüllen:

* Die Schlüsselspalte muss im Daten-Feed enthalten sein.
   * Für `carrier.tsv` müssen Sie `carrier` einbeziehen.
   * Für `mobile_attributes.tsv` müssen Sie `mobile_id` einbeziehen.
   * Für `operating_system_type.tsv` müssen Sie `os` einbeziehen.
* Die folgenden Spalten müssen **excluded** sein. Wenn eine dieser Spalten im Daten-Feed enthalten ist, wird die dynamische Suche `mobile_attributes.tsv` nicht einbezogen.
   * `user_agent`
   * `ch_hdr`
   * `ch_js`

Sobald Ihr Daten-Feed die Aufnahme- und Ausschlussanforderungen für Spalten erfüllt, wenden Sie sich mit der Daten-Feed-ID an die Kundenunterstützung und fordern Sie die Aktivierung dynamischer Suchen an.

## Lookup-Kopfzeilenreferenz

Spaltenüberschriften für diese Lookup-Dateien ändern sich im Laufe der Zeit nicht, sodass Header nicht in jeder Daten-Feed-Datei enthalten sind. Verwenden Sie diese Spaltenüberschriften als Referenz oder laden Sie die entsprechende `.tsv` -Datei herunter.

+++**Betreibername**
Laden Sie [carrier_headers.tsv](assets/carrier_headers.tsv) herunter oder referenzieren Sie die folgenden Header.

`carrier`
`Carrier Name`
+++

+++**Mobile Attribute**
Laden Sie [mobile_attributes_headers.tsv](assets/mobile_attributes_headers.tsv) herunter oder referenzieren Sie die folgenden Header.

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
Laden Sie [operating_system_type_headers.tsv](assets/operating_system_type_headers.tsv) herunter oder referenzieren Sie die folgenden Header.

`os`
`Operating System Type`
+++
