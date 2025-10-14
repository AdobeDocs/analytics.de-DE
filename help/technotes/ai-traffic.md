---
description: Erfahren Sie, wie Sie Berichte über Traffic von KI-Chatbots erstellen
title: Analysieren des Traffics von KI-Chatbots
feature: Metrics, Data Configuration and Collection
source-git-commit: d16214865a037efe41b9f95682758daa577a12ed
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

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

