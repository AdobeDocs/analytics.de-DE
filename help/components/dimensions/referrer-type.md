---
title: Referrer-Typ
description: Der Typ des Referrers, je nachdem, woher der Besucher stammt.
feature: Dimensions
exl-id: a6cfcbf4-cd08-4e7f-8e86-47488ceb0ea3
source-git-commit: 400f0170f13e95c401f3c4c329d23d63dcd70443
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 88%

---

# Referrer-Typ

Der „Referrer-Typ[ (Dimension](overview.md) zeigt an, welche allgemeinen Kanäle Besucher durchgeklickt haben, um zu Ihrer Site zu gelangen. Im Gegensatz zu [Marketing-Kanälen](marketing-channel.md), bei denen Ihre Organisation Regeln für jeden Kanal verwaltet, verwaltet Adobe die Regeln für jedes Dimensionselement.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist auf mehrere interne Suchtabellen von Adobe. Jeder Wert basiert auf dem [Referrer](referrer.md) des Treffers, der von [internen URL-Filtern](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md) abhängig ist. Vergewissern Sie sich, dass die Dimension „Referrer“ und die internen URL-Filter korrekt konfiguriert sind.

## Dimensionselemente

Zu den Dimensionselementen gehören die Typen der Referrer des Treffers. Zu den spezifischen Werten gehören die folgenden:

* **Eingegeben/mit Lesezeichen versehen**: Für den Treffer liegen keine Daten zum Referrer vor.
* **Suchmaschinen**: Der Referrer kam von einer anerkannten Suchmaschine, die eine Abfragezeichenfolge mit Suchbegriffen enthält.
* **Konversationelle KI-Tools**: Der Referrer stammt aus einem anerkannten konversativen KI-Tool.
* **Soziale Netzwerke**: Die Referrer-Daten gehörten zu einem von Adobe anerkannten sozialen Netzwerk.
* **Andere Websites**: Die Referrer-Daten gehörten nicht zu einer Suchmaschine oder einem sozialen Netzwerk, die/das von Adobe erkannt wird.
* **Keine JavaScript**: Die verweisende Stelle kam von einem Browser, für den JavaScript nicht aktiviert war.
* **Festplatte**: Der Referrer stammt von einer lokalen Kopie einer Webseite auf der Festplatte des Besuchers.
* **E-Mail**: Der Referrer stammt aus einer URL mit einem `imap://`- oder `mail://`-Protokoll. Dies umfasst keine Online-E-Mail-Dienste, da diese normalerweise ein `https://`-Protokoll verwenden.

### Konversationelle KI-Tools

Die folgende Liste verweist auf die von Adobe verwendete Lookup-Tabelle „Conversational AI-Tools“. Adobe stellt diese Liste den Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domain hinzufügt, bitten Sie einen Support-Mitarbeiter in Ihrem Unternehmen, sich an die Kundenunterstützung zu wenden.

* `https://chatgpt.com`
* `https://chat.com`
* `https://chat.openai.com`
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

### Soziale Netzwerke

Die folgende Liste verweist auf die von Adobe verwendete Suchtabelle „Soziale Netzwerke“. Adobe stellt diese Liste den Kunden von Adobe Analytics zur Verfügung. Wenn Sie empfehlen möchten, dass Adobe dieser Liste eine Domain hinzufügt, bitten Sie einen Support-Mitarbeiter in Ihrem Unternehmen, sich an die Kundenunterstützung zu wenden.

>[!NOTE]
>
>Diese Liste unterscheidet sich von der standardmäßigen Liste von sozialen Netzwerken in den [Verarbeitungsregeln für Marketing-Kanäle](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-rules.md).

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
