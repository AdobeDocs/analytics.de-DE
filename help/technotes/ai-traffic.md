---
description: Erfahren Sie, wie Sie Berichte über Traffic von KI-Chatbots erstellen
title: Analysieren des Traffics von KI-Chatbots
feature: Metrics, Data Configuration and Collection
exl-id: 0b013b7d-02a2-405d-bdd6-c991f0baac8e
TQID: https://experienceleague.adobe.com/lyzSP-7iZ8Y5XiTG1t7Axsg1f5AJf6BbcZbu7MmkwWU
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: b7156124-d291-4de4-ac0c-ed17d8078449id: b8734a57-d5fb-44a8-8ee1-65225cecaeaeid: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 643
ht-degree: 2%

---

# Analysieren des Traffics von konversativen KI-Tools

Adobe Analytics bietet Tools zur Analyse des KI-Traffics auf Ihrer Website.

Bei der Analyse des KI-Traffics müssen Sie zunächst verstehen, welche Arten von KI-Traffic auftreten können und welche Typen Treffer generieren. Anschließend können Sie den Traffic in Analysis Workspace analysieren.

## KI-Traffic verstehen

### Typen von KI-Traffic verstehen

KI-Traffic auf Ihrer Website kann unter folgenden Umständen auftreten:

* **Während des Vortrainings**: Tritt selten auf, wenn Inhalte von Ihrer Website gekratzt und in die KI-Schulungsdaten aufgenommen werden.

* **Bei der Reaktion auf On-Demand-**: Tritt in dem Moment auf, in dem der Benutzer KI mit einer Frage auffordert und der KI-Chatbot antwortet. Der KI-Chatbot führt eine Web-Suche durch und Inhalte von Ihrer Website werden in die Antwort aufgenommen. (Diese Art von Interaktionen wird manchmal als Retrieval-Augmented Generation (RAG) bezeichnet.)

  Einige KI-Chatbot-Antworten enthalten Links zum Quellmaterial auf Ihrer Site, andere nicht.

* **Beim Ausführen von Agent-Workflows**: Tritt jedes Mal auf, wenn ein KI-Agent Ihre Website besucht, wenn er auf eine Reihe von Web-Seiten in einem Browser klickt, um auf eine Benutzeranfrage zu reagieren. In diesem Fall agiert die KI als Agent für den Benutzer, der die Anfrage gestellt hat.

### Erfahren Sie, wann Treffer für KI-Traffic generiert werden

Ein Treffer wird auf einer Web-Seite generiert, wenn JavaScript auf der Seite ausgeführt wird. Je nach Art des KI-Traffics auf Ihrer Site wird JavaScript möglicherweise ausgeführt oder nicht.

| KI-Traffic-Typ | Erzeugt Treffer | Zu beachten |
|---------|----------|---------|
| **Vorschulung** | Ja | Treffer werden während der Vorschulung generiert, wenn der Inhalt von Ihrer Website in die KI aufgenommen wird. Eine Vorschulung findet jedoch selten statt. Inhalte, die im Vorschulungsmodus einer KI enthalten sind, können in zukünftigen Antworten immer wieder verwendet werden, ohne dass weitere Treffer auf Ihrer Website generiert werden. <p>Mit anderen Worten: Ein einzelner Treffer, der während des Vortrainings einer KI auftritt, kann immer wieder für mehrere On-Demand-Antworten wiederverwendet werden, ohne dass zusätzliche Treffer auf Ihrer Website erzeugt werden.</p><p>Informationen zur Analyse dieses KI-Traffics in Analysis Workspace finden Sie unter [Analysieren von KI-Traffic mithilfe der Bot-Erkennung](#analyze-ai-traffic-using-bot-detection).</p> |
| **On-Demand-Aufforderungen** | Nein | Die KI-Antwort generiert keine Treffer, da die Antwort eine Kombination aus Folgendem verwendet:<ul><li>Vortrainierte Daten <br/>Informationen sind bereits im vortrainierten Wissen der KI enthalten, sodass die KI JavaScript nicht auf Seiten ausführt.</li><li>On-Demand-Websuche <br/>Ruft während der Websuche nur die unformatierte HTML der Webseite ab, sodass die KI JavaScript nicht auf Seiten ausführt.</li></ul> |
| **Materielle Links zu Source in KI-Antworten** | Ja | Treffer werden generiert, wenn ein Benutzer auf den Link zu Quellmaterial klickt, das in der KI-Antwort enthalten ist. Es wird kein Treffer generiert, wenn in der Antwort ein Link enthalten ist und der Benutzer nicht auf den Link geklickt hat. <p>Einige KI-Chatbot-Antworten enthalten Links zum Quellmaterial, andere nicht. </p><p>Informationen zur Analyse dieses KI-Traffic-Typs in Analysis Workspace finden Sie unter [Analysieren von KI-Traffic nach Referrer-Typ](#analyze-ai-traffic-by-referrer-type).</p> |
| **Agent-Workflows** | Ja | Treffer werden auf jeder Seite generiert, wenn der KI-Agent im Namen des Benutzers durch den Workflow klickt. <p>Informationen zur Analyse dieses KI-Traffic-Typs in Analysis Workspace finden Sie unter [Analysieren von KI-Traffic nach Referrer-Typ](#analyze-ai-traffic-by-referrer-type).</p> |

## Analysieren des KI-Traffics in Analysis Workspace

### Analysieren des KI-Traffics nach Referrer-Typ

Sie können die Dimension Referrer-Typ in Analysis Workspace verwenden, um die folgenden Arten von KI-Traffic zu analysieren:

* Materielle Links zu Source in KI-Antworten

* Agent-Workflows

Die Dimension Referrer-Typ enthält das Dimensionselement [Konversationelle KI-Tools](/help/components/dimensions/referrer-type.md#conversational-ai-tools). Dieses Dimensionselement enthält eine vordefinierte Liste von KI-Chatbots.

Weitere Informationen finden Sie unter [Referrer-Typ](/help/components/dimensions/referrer-type.md).

### Analysieren des KI-Traffics mithilfe der Bot-Erkennung

Sie können die Bot-Erkennung in Analysis Workspace verwenden, um den KI-Traffic zu analysieren, der aus der Vorschulung stammt.
