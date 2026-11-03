---
title: Referrer-Typ
description: Der Typ des Referrers, je nachdem, woher der Besucher stammt.
feature: Dimensions
exl-id: a6cfcbf4-cd08-4e7f-8e86-47488ceb0ea3
TQID: 'https://experienceleague.adobe.com/KPTS2iWls0V8I2gI0xcH1V89w0stZyVq6jWdQyEyrLY'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: b7156124-d291-4de4-ac0c-ed17d8078449
    internal-label: AI Tools
  - id: b8734a57-d5fb-44a8-8ee1-65225cecaeae
    internal-label: Data configuration and collection
subfeature_v2:
  - id: b22bc0f7-b089-4966-95a1-31e7b3b69b79
    internal-label: Dimensions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: b4c7365f660ff093731d55c7aba9cae5ade76789
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 47%
---
# Referrer-Typ

Der „Referrer-Typ[&#x200B; (Dimension](overview.md) zeigt an, welche allgemeinen Kanäle Besucher durchgeklickt haben, um zu Ihrer Site zu gelangen. Im Gegensatz zu [Marketing-Kanälen](marketing-channel.md), bei denen Ihre Organisation Regeln für jeden Kanal verwaltet, verwaltet Adobe die Regeln für jedes Dimensionselement.

## Füllen dieser Dimension mit Daten

Adobe leitet diese Dimension vom [Referrer](referrer.md) jedes Treffers ab und ordnet sie mehreren Adobe-internen Suchtabellen zu. Es gibt keine Variable zum Festlegen. Da jeder Wert vom Referrer abhängt, stellen Sie sicher, dass die Dimension „Referrer“ und [Interne URL-Filter](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) korrekt konfiguriert sind.

| Eigenschaft | Wert |
| --- | --- |
| **AppMeasurement-Variable** | Keine (abgeleitet vom Referrer) |
| **Feld Web SDK/XDM** | Keine (abgeleitet vom Referrer) |
| **Abfrageparameter** | k. A. |
| **XML-Tag** | k. A. |
| **Byte-Grenze** | k. A. |
| **Persistenz** | nicht angegeben |

## Dimensionselemente

Zu den Dimensionselementen gehören die Typen der Referrer des Treffers. Zu den spezifischen Werten gehören die folgenden:

* **Eingegeben/mit Lesezeichen versehen**: Für den Treffer liegen keine Daten zum Referrer vor. Dieser Wert umfasst Besuche von [konversationalen KI-Tools, die Links ohne Referrer öffnen](#include-ai-traffic-that-has-no-referrer).
* **Suchmaschinen**: Der Referrer kam von einer anerkannten Suchmaschine, die eine Abfragezeichenfolge mit Suchbegriffen enthält.
* **Konversationelle KI-Tools**: Der Referrer stammt aus einem anerkannten konversativen KI-Tool.
* **Soziale Netzwerke**: Die Referrer-Daten gehörten zu einem von Adobe anerkannten sozialen Netzwerk.
* **Andere Websites**: Die Referrer-Daten gehörten nicht zu einer Suchmaschine oder einem sozialen Netzwerk, die/das von Adobe erkannt wird.
* **Keine JavaScript**: Die verweisende Stelle kam von einem Browser, für den JavaScript nicht aktiviert war.
* **Festplatte**: Der Referrer stammt von einer lokalen Kopie einer Webseite auf der Festplatte des Besuchers.
* **E-Mail**: Der Referrer stammt aus einer URL mit einem `imap://`- oder `mail://`-Protokoll. Dies umfasst keine Online-E-Mail-Dienste, da diese normalerweise ein `https://`-Protokoll verwenden.

### Konversationelle KI-Tools

>[!IMPORTANT]
>
>Dieser Wert umfasst nur Besuche mit einem Referrer aus der folgenden Liste. Einige KI-Tools für Gespräche, wie ChatGPT, senden beim Öffnen von Links keinen Referrer, sodass ihre Besuche nicht eingeschlossen sind. Weitere Informationen finden Sie unter [Einbeziehen von KI-Traffic ohne Referrer](#include-ai-traffic-that-has-no-referrer).

Die folgende Liste verweist auf die von Adobe verwendete Lookup-Tabelle „Conversational AI-Tools“. Adobe stellt diese Liste den Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domain hinzufügt, bitten Sie einen Support-Mitarbeiter in Ihrem Unternehmen, sich an die Kundenunterstützung zu wenden.

* `https://chatgpt.com`
* `https://chat.com`
* `https://chat.deepseek.com`
* `https://chat.openai.com`
* `https://doubao.com`
* `https://duck.ai`
* `https://gemini.google.com`
* `https://copilot.microsoft.com`
* `https://m365.cloud.microsoft`
* `https://perplexity.ai`
* `https://labs.perplexity.ai`
* `https://playground.perplexity.ai`
* `https://claude.ai`
* `https://grok.com`
* `https://komo.ai`
* `https://phind.com`
* `https://poe.com`
* `https://blackbox.ai`
* `https://chat.mistral.ai`
* `https://meta.ai`
* `https://you.com`

#### KI-Traffic ohne Referrer einbeziehen

Einige KI-Tools für Gespräche, einschließlich ChatGPT, öffnen Links, ohne einen Referrer zu senden. Adobe meldet diese Besuche unter „Eingegeben/Mit Lesezeichen versehen“ anstelle von „Konversations-KI-Tools“. KI-Tools können jederzeit ändern, wie sie Links öffnen. Wenn der Traffic Ihrer „Konversations-KI-Tools“ sinkt, hat ein Tool möglicherweise angehalten, einen Referrer zu senden. Der Rückgang bedeutet nicht, dass Adobe Analytics Daten verloren hat.

Anstelle eines Referrers fügen einige dieser Tools den Links, die sie öffnen, einen UTM-Abfragezeichenfolgenparameter hinzu, z. B. `utm_source=chatgpt.com` oder `utm_source=perplexity`. Verwenden Sie den UTM-Parameter zusammen mit dem Wert „Conversational AI Tools“, um eine vollständige Anzahl des Traffics von Konversations-KI-Tools zu erhalten:

* **Erfassen des UTM-Parameters in einer**: Setzen Sie eine eVar auf den `utm_source` Wert der Landingpage-URL. Verwenden Sie das [`getQueryParam`](/help/implement/vars/plugins/getqueryparam.md)-Plug-in, die URL-Parameterfunktionen in der Web-SDK- oder Adobe Analytics-Erweiterung oder eine [Verarbeitungsregel](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-use-cases.md) die den Abfragezeichenfolgenparameter liest.
* **Erstellen eines Marketing-Kanals für KI** Tools: Erstellen Sie eine [Marketing-Kanal-Verarbeitungsregel](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md) die übereinstimmt, wenn eine der Bedingungen erfüllt ist. Fügen Sie **[!UICONTROL Bedingung „Referrer Is Conversational AI]** und eine **[!UICONTROL Query String Parameter]** `utm_source` für jeden Wert hinzu, den KI-Tools verwenden, z. B. `chatgpt.com` oder `perplexity`.
* **Segment erstellen**: Erstellen Sie ein [Segment](/help/components/segmentation/seg-overview.md), das entweder „Referrer-Typ“ gleich „Konversationelle KI-Tools“ übereinstimmt oder Ihr UTM-eVar einen von KI-Tools verwendeten Wert enthält. Da die Dimension [Seiten](page-url.md)URL) Abfragezeichenfolgen enthält, können Sie auch Seiten-URLs mit `utm_source=chatgpt.com` abgleichen. Diese Option funktioniert ohne Implementierungsänderungen.

Einige KI-Tools senden weder einen Referrer noch einen UTM-Parameter. Sie können Traffic von diesen Tools nicht als KI-Traffic identifizieren.

### Soziale Netzwerke

Die folgende Liste verweist auf die von Adobe verwendete Nachschlagetabelle „Soziale Netzwerke“. Adobe stellt diese Liste den Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domain hinzufügt, bitten Sie einen Support-Mitarbeiter in Ihrem Unternehmen, sich an die Kundenunterstützung zu wenden.

>[!NOTE]
>
>Diese Liste unterscheidet sich von der standardmäßigen Liste von sozialen Netzwerken in den [Verarbeitungsregeln für Marketing-Kanäle](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md).

* `12seconds.tv`
* `4travel.jp`
* `advogato.org`
* `ameba.jp`
* `anobii.com`
* `answers.yahoo.com`
* `asmallworld.net`
* `avforums.com`
* `backtype.com`
* `badoo.com`
* `bebo.com`
* `bigadda.com`
* `bigtent.com`
* `biip.no`
* `blackplanet.com`
* `blog.seesaa.jp`
* `blogspot.com`
* `blogster.com`
* `blomotion.jp`
* `bolt.com`
* `brightkite.com`
* `bsky.app`
* `buzznet.com`
* `cafemom.com`
* `care2.com`
* `classmates.com`
* `cloob.com`
* `collegeblender.com`
* `cyworld.co.kr`
* `cyworld.com.cn`
* `dailymotion.com`
* `delicious.com`
* `deviantart.com`
* `digg.com`
* `diigo.com`
* `disqus.com`
* `draugiem.lv`
* `facebook.com`
* `faceparty.com`
* `fc2.com`
* `flickr.com`
* `flixster.com`
* `fotolog.com`
* `foursquare.com`
* `friendfeed.com`
* `friendsreunited.com`
* `friendsreunited.co.uk`
* `friendster.com`
* `fubar.com`
* `gaiaonline.com`
* `geni.com`
* `go.bsky.app`
* `goodreads.com`
* `plus.google.com`
* `plus.url.google.com`
* `grono.net`
* `habbo.com`
* `hatena.ne.jp`
* `hi5.com`
* `hotnews.infoseek.co.jp`
* `hyves.nl`
* `ibibo.com`
* `identi.ca`
* `t.ifeng.com`
* `imeem.com`
* `instagram.com`
* `intensedebate.com`
* `irc-galleria.net`
* `iwiw.hu`
* `jaiku.com`
* `jp.myspace.com`
* `kaixin001.com`
* `kakaku.com`
* `kanshin.com`
* `kozocom.com`
* `last.fm`
* `likeshop.me`
* `linkedin.com`
* `linkin.bio`
* `livejournal.com`
* `lnkd.in`
* `meetup.com`
* `me2day.net`
* `mister-wong.com`
* `mixi.jp`
* `mixx.com`
* `mouthshut.com`
* `mp.weixin.qq.com`
* `multiply.com`
* `mumsnet.com`
* `myheritage.com`
* `mylife.com`
* `myspace.com`
* `myyearbook.com`
* `nasza-klasa.pl`
* `matome.naver.jp`
* `netlog.com`
* `nettby.no`
* `netvibes.com`
* `nextdoor.com`
* `nicovideo.jp`
* `ning.com`
* `odnoklassniki.ru`
* `ok.ru`
* `orkut.com`
* `pakila.jp`
* `photobucket.com`
* `pinterest.com`
* `pinterest.co.uk`
* `plaxo.com`
* `plurk.com`
* `po.st`
* `reddit.com`
* `renren.com`
* `skyrock.com`
* `slideshare.net`
* `smcb.jp`
* `smugmug.com`
* `snapchat.com`
* `sonico.com`
* `studivz.net`
* `stumbleupon.com`
* `t.163.com`
* `t.co`
* `t.hexun.com`
* `t.people.com.cn`
* `t.qq.com`
* `t.sina.com.cn`
* `t.sohu.com`
* `tabelog.com`
* `tagged.com`
* `taringa.net`
* `thefancy.com`
* `threads.com`
* `threads.net`
* `tiktok.com`
* `toutiao.com`
* `tripit.com`
* `trombi.com`
* `trytrend.jp`
* `tuenti.com`
* `tumblr.com`
* `twine.com`
* `twitter.com`
* `uhuru.jp`
* `viadeo.com`
* `vimeo.com`
* `vk.com`
* `wayn.com`
* `web-cdn.bsky.app`
* `weibo.com`
* `weourfamily.com`
* `wer-kennt-wen.de`
* `wordpress.com`
* `x.com`
* `xanga.com`
* `xing.com`
* `yammer.com`
* `yaplog.jp`
* `yelp.com`
* `yelp.co.uk`
* `youku.com`
* `youtube.com`
* `yozm.daum.net`
* `yuku.com`
* `zooomr.com`
* `zhihu.com`

### Suchmaschinen im Dimensionselement „Andere Websites“

Wenn Sie bestimmte Domänen in der Dimension „Referrer-Typ“ anzeigen, kann es vorkommen, dass Domänen, die Sie unter „Suchmaschinen“ erwarten würden, stattdessen unter „Andere Websites“ aufgeführt sind. Beispielsweise sehen Sie möglicherweise `'google.com'` unter „Andere Websites“.

* **Suchmaschinendomänen im Dimensionselement „Suchmaschinen“**: Der Referrer erfüllte alle Kriterien, um von Adobe als Suchmaschine klassifiziert zu werden. Die Referrer-Domäne ist eine gültige Suchmaschine *und* die Referrer-URL enthält einen Abfragezeichenfolgenparameter für Suchbegriffe.
* **Suchmaschinendomänen im Dimensionselement „Andere Websites“**: Die Referrer-URL erfüllte nicht alle Kriterien, um als Suchmaschine klassifiziert zu werden. Häufige Beispiele sind Unterdomänen, die neben der Suche anderen Funktionen gewidmet sind. Zum Beispiel sind `mail.google.com` und `autos.yahoo.com` keine Suchmaschinen, sondern befinden sich in einer Domain auf oberster Ebene, die normalerweise mit der Suche verbunden ist. Diese Unterdomänen enthalten keine Abfragezeichenfolge für Suchbegriffe. Daher werden sie unter „Andere Websites“ und nicht unter „Suchmaschinen“ aufgeführt.
