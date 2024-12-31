---
title: s_objectID
description: Hilft Activity Map, eindeutige Links auf Ihrer Website zu identifizieren.
feature: Variables
exl-id: 7c0cb750-2bfe-41ca-ab27-30dda4b3a7fa
role: Admin, Developer
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 80%

---

# s_objectID

Die `s_objectID`-Variable stellt eine eindeutige Kennung für einen Link bereit. Damit werden Berichte in [Activity Map](/help/analyze/activity-map/overview.md) genauer. Wenn Sie Links auf einer Seite haben, die sich häufig ändern, können Sie die `s_objectID`-Variable verwenden, um Activity Map die Position eines eindeutigen Links anzuzeigen, damit die Daten nach Wunsch korrekt gruppiert werden können.

Wenn die Activity Map-Genauigkeit für Ihr Unternehmen von entscheidender Bedeutung ist, empfiehlt Adobe, die Variable `s_objectID` im `onClick` von Links auf Ihrer Site einzubeziehen.

## Objekt-ID bei Verwendung der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s_objectID im AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s_objectID`-Variable ist eine globale Variable, d. h. sie funktioniert unabhängig vom Analytics-Tracking-Objekt (standardmäßig `s`). Beliebige Zeichenfolgen mit einer Länge von bis zu 100 Byte können gültige Werte für diese Variable sein. Wenn diese Variable nicht definiert ist, verwendet Activity Map den Link-Text als Kennung für den Link.

Diese Variable wird normalerweise im `onClick`-Ereignis eines HTML-Links gesetzt.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Fügen Sie immer das Semikolon ein, das eine JavaScript-Anweisung abschließt. Das Semikolon ist erforderlich, damit Activity Map funktioniert.

## Anwendungsbeispiele

Die `s_objectID`-Variable ist immer dann nützlich, wenn Sie eine höhere Genauigkeit in Activity Map-Berichten wünschen.

### Aggregieren von Links aus hochdynamischen Inhalten

Einige Websites verfügen über hochdynamische Inhalte, z. B. Nachrichten- oder Retail-Websites mit häufig wechselnden Artikeln. Da Activity Map standardmäßig die Link-URL als Kennung verwendet, ist es schwierig, die am häufigsten geklickten Bereiche auf Seiten zu verstehen, deren Links sich häufig ändern. Wenn Sie die `s_objectID` innerhalb dieser Links verwenden, versteht Activity Map, welche Links aggregiert werden können, unabhängig von den URLs, auf die sie verweisen.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Unabhängig davon, wohin die Links zeigen oder wie oft Sie diese Links ändern, aggregiert Activity Map die Daten auf der Grundlage des Wertes in `s_objectID`.

### Links auf einer Seite getrennt halten

Einige Websites verfügen über Links, die an verschiedenen Stellen auf dieselbe Stelle verweisen. Beispiel: Ein Link zur Homepage in der Kopf- und Fußzeile Ihrer Website. Da diese Links dieselbe URL haben, aggregiert Activity Map ihre Daten. Sie können sie mithilfe der `s_objectID`-Variablen trennen:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Selbst wenn Links auf dieselbe URL verweisen, kann Activity Map die Variable `s_objectID` verwenden, um sie beim Reporting korrekt zu unterscheiden.
