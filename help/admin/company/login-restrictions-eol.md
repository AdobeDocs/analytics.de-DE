---
title: Ende der Lebensdauer für [!UICONTROL IP-Anmeldebeschränkungen erzwingen]
description: Erfahren Sie mehr über das Ende der Lebensdauer und die Auswirkungen auf [!UICONTROL Erzwingt IP-Anmeldebeschränkungen]
translation-type: tm+mt
source-git-commit: 940638b77f800b471f1ce4097a8ca6de98d518d3

---


# Ende der Lebensdauer für [!UICONTROL Enforce IP login restrictions]

Mit der Funktion **[IP-Anmeldebeschränkungen erzwingen](/help/admin/company/security-manager.md)**in Adobe Analytics können Sie bestimmte IP-Adressen (die als sicher gelten) auf eine Whitelist setzen, um eine erfolgreiche Anmeldung und den Zugriff auf Ihre Adobe Analytics-Umgebung zu ermöglichen. In vielen Fällen wird diese Funktion verwendet, um eine Unternehmens-IP-Adresse als einzige sichere IP-Adresse einzurichten, von der aus Benutzer sich anmelden können. Um Adobe Analytics verwenden zu können, müssen sich die Benutzer daher entweder in einem Unternehmensbüro befinden oder sich über VPN im Netzwerk anmelden.

Wir planen, diese Funktion im Januar 2021 zu beenden.

## Warum schaffen wir diese Funktion ab?

Diese Funktion wird unter bestimmten Umständen durch die Migration der Experience Cloud-Anmeldung und/oder die Experience Cloud-Anmeldung beeinträchtigt. Es ist bekannt, dass es für Kunden, die **[!UICONTROL Customer Attributes]** oder **[!UICONTROL Audience Library]** verwenden, kaputt ist.

Wenn Sie über mehrere Experience Cloud-Lösungen verfügen, können Sie diese Anforderung umgehen, indem Sie sich mit einer der anderen Lösungen bei der Experience Cloud anmelden, da diese Funktion außerhalb von Analytics selbst nicht vorhanden ist oder nicht unterstützt wird. Benutzer können dies auch über IP-Spoofing umgehen.

Schließlich verfügt Adobe über eine funktionierende und weit überlegene Alternativlösung mit Single Sign-On und Federated IDs. Diese Funktion bietet Ihnen mehr Kontrolle und Sicherheit über die Anmeldeerfahrung Ihrer Benutzer. Weitere Informationen finden Sie unten.

## Wie wirkt sich die Abschaffung dieser Funktion auf Sie aus?

Für alle Kunden, die diese Funktion **[!UICONTROL Enforce IP login restrictions]** eingerichtet haben, wird diese Funktion im Januar 2021 entfernt. Zu diesem Zeitpunkt werden noch festgelegte IP-Anmeldebeschränkungen nicht mehr erzwungen. Wenn Sie die Anmeldung weiterhin nach IP-Adresse beschränken müssen, sollten Sie die empfohlene Lösung für Single Sign-On und Federated IDs (weitere Informationen und Ressourcen unten) prüfen und implementieren.

Additionally, the **[!UICONTROL Enforce IP login restrictions]** setting will be removed from the **[!UICONTROLAdmin > Company Settings > Security Manager]** in the Analytics UI (as shown below).

![](assets/sec-manager2.png)

## Welche anderen Optionen haben Sie?

Wie oben erläutert, wird diese Analytics-Funktion abgeschafft. Damit Sie Zeit haben, SSO- und Federated IDs zu implementieren, haben wir das EOL-Datum auf Januar 2021 verschoben.

Sowohl SSO als auch Federated IDs sind modernere und überlegene Lösungen für die IP-Anmeldebeschränkung und bieten Ihnen mehr Kontrolle und Sicherheit und mehr Funktionen. Informationen zum Einrichten von SSO/Federated IDs finden Sie in der folgenden Hilfedokumentation. Sie sollten sie gründlich lesen und mit Ihrer IT-Abteilung bei der Implementierung zusammenarbeiten:

* [Single Sign-On und die Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [Admin Console – Dokumentation zur Identitätseinrichtung](https://helpx.adobe.com/de/enterprise/using/set-up-identity.html)
* [Admin Console – Tutorial zur Identitätseinrichtung (Video)](https://helpx.adobe.com/de/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [Tutorial zur Konfiguration von Federated IDs (Video)](https://helpx.adobe.com/de/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [Single Sign-On – Häufig gestellte Fragen](https://helpx.adobe.com/de/enterprise/using/sso-faq.html)
* [Von Adobe unterstützte Identitätstypen](https://helpx.adobe.com/de/enterprise/using/identity.html)

Wenn Sie weiterhin Ihre Unterstützung für IP-Anmeldebeschränkungen äußern und beantragen möchten, dass diese Funktion von Experience Cloud bereitgestellt wird, können Sie auf unserer [Forumsseite](https://forums.adobe.com/ideas/11648) für diese Funktion stimmen.