---
description: Das abort-Flag kann in doPlugins festgelegt werden, damit der aktuelle Nachverfolgungsaufruf nicht gesendet wird.
keywords: Analytics-Implementierung
seo-description: Das abort-Flag kann in doPlugins festgelegt werden, damit der aktuelle Nachverfolgungsaufruf nicht gesendet wird.
seo-title: Flag „s.abort“
solution: Analytics
title: Flag „s.abort“
topic: Entwickler und Implementierung
uuid: 0c6ec8c7-d136-4851-8cb6-6cb1b7f6f0dc
translation-type: ht
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Flag „s.abort“

Das abort-Flag kann in doPlugins festgelegt werden, damit der aktuelle Nachverfolgungsaufruf nicht gesendet wird.

Das abort-Flag wird bei jedem Nachverfolgungsaufruf zurückgesetzt. Wenn also auch ein nachfolgender Nachverfolgungsaufruf abgebrochen werden muss, muss das Flag erneut in doPlugins eingestellt werden.

```js
s.doPlugins = function(s) { 
     s.campaign = s.getQueryParam("cid"); 
     if ((!s.campaign) && (!s.events)) { 
          s.abort = true; 
     } 
};
```

Damit können Sie die Logik zentralisieren, mit der Sie Aktivitäten ermitteln, die Sie nicht nachverfolgen möchten, z. B. einige benutzerspezifische Links oder externe Links in Display-Anzeige.
