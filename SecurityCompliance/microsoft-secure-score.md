---
title: Microsoft-Sicherheitsbewertung
description: Beschreibt Microsoft 365 Secure Score, wie Details berechnet werden und welche Sicherheitsadministratoren davon ausgehen können.
keywords: Sicherheit, Schadsoftware, Microsoft 365, M365, Secure Score, Security Center, Improvement Actions
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: fa76e2edd3f66595a47fb511881f15c07b441c77
ms.sourcegitcommit: 8213c353954b92f5c3979bee4aa049da0fd28a18
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/03/2019
ms.locfileid: "31043246"
---
# <a name="microsoft-secure-score"></a>Microsoft-Sicherheitsbewertung

Mit Microsoft Secure Score im Microsoft 365 Security Center können Sie die Sicherheit Ihrer Organisation erhöhen. Über ein zentrales Dashboard können Sie die Sicherheit für Ihre Microsoft 365-Identitäten, Daten, apps, Geräte und Infrastruktur überwachen und verbessern.

Microsoft Secure Score bietet Ihnen stabile Visualisierungen, Integration mit anderen Microsoft-Produkten, Vergleich ihrer Gäste mit anderen Unternehmen, Filterung nach Kategorie und vieles mehr. Mit dem Tool können Sie Sicherheits Verbesserungs Aktionen innerhalb Ihrer Organisation ausführen und den Verlauf ihrer Bewertung nachverfolgen. Die Bewertung kann auch widerspiegeln, wenn von Drittanbieterlösungen Empfohlene Verbesserungs Aktionen behoben wurden.  

## <a name="how-it-works"></a>Funktionsweise

Sie erhalten Punkte zum Konfigurieren empfohlener Sicherheitsfunktionen, zum Ausführen von sicherheitsbezogenen Aufgaben (beispielsweise zum Anzeigen von Berichten) oder zur Behandlung der Verbesserungs Aktion mit einer Anwendung oder Software eines Drittanbieters. Einige Aktionen werden für die partielle Vervollständigung wie die Aktivierung der mehrstufigen Authentifizierung (Multi-Factor Authentication, MFA) für Ihre Benutzer erzielt. Sicherheit sollte immer mit der Benutzerfreundlichkeit ausgeglichen werden, und nicht jede Empfehlung funktioniert für Ihre Umgebung.

## <a name="required-permissions"></a>Erforderliche Berechtigungen

Zum Anzeigen von Microsoft Secure Score müssen Sie derzeit eine der folgenden Rollen in Azure Active Directory besitzen:

* Globaler Administrator
* Sicherheitsadministrator
* Sicherheits Leser

## <a name="rich-experiences--additional-security-recommendations"></a>Umfassende Erfahrungen & zusätzliche Sicherheitsempfehlungen

In Microsoft Secure Score haben wir Empfehlungen aus Azure AD, InTune und Cloud App Security hinzugefügt, mit Empfehlungen von Azure Security Center und Windows Defender ATP in Kürze. Außerdem haben wir noch mehr Office 365-Sicherheitsempfehlungen hinzugefügt. Mit zusätzlichen Einblicken und mehr Einblick in eine breitere Palette von Microsoft-Produkten und-Diensten können Sie sich sicher sein, dass Sie bis zum Management über die Sicherheitsintegrität Ihrer Organisation berichten. Sie können Ihre Punktzahl auch mithilfe der [Microsoft Graph-API](https://docs.microsoft.com/graph/api/resources/securescores?view=graph-rest-beta)abrufen.

Um Ihnen die benötigten Informationen schneller zur Verfügung zu stellen, werden Microsoft-Empfehlungen in Gruppen organisiert:

* Identity (Schutzstatus ihrer Azure AD-Konten und-Rollen)
* Daten (Schutzstatus Ihrer Office 365-Dokumente)
* Gerät (Schutzstatus Ihrer Geräte; Windows Defender ATP Improvement-Aktionen in Kürze verfügbar
* App (Schutzstatus Ihrer e-Mails und Cloud-Apps)
* Infrastruktur (Schutzstatus ihrer Azure-Ressourcen; demnächst verfügbar)

Auf der Microsoft Secure Score-Übersichtsseite können Sie sehen, wie Punkte zwischen diesen Gruppen aufgeteilt werden und welche Punkte verfügbar sind. Auf der Übersichtsseite finden Sie auch eine umfassende Übersicht über die Gesamtpunktzahl, den historischen Trend ihres sicheren Ergebnisses mit Benchmark-Vergleichen und priorisierte Verbesserungsmaßnahmen, die ergriffen werden können, um Ihre Punktzahl zu verbessern. Mithilfe dieser Daten können Sie große Unterschiede in der Sicherheitsposition eingehen.  

![M365-](./media/secure-score/homepage-original.png)
Homepage*Abbildung 1: Microsoft Secure Score Overview Page*

## <a name="take-action-to-improve-your-score"></a>Maßnahmen ergreifen, um Ihre Punktzahl zu verbessern

Auf der Registerkarte Verbesserungs Aktionen werden alle Sicherheitsempfehlungen für Ihren Mandanten zusammen mit dem Status (abgeschlossen, nicht abgeschlossen, durch Drittanbieter aufgelöst und ignoriert) aufgelistet. Sie können alle Steuerelemente suchen, Filtern und gruppieren.  Die Rangfolge basiert auf der Bewertung von Sicherheitswert und dem zu vervollständigenden Aufwand von Microsoft.

Aktionen, die als [nicht erzielt] gekennzeichnet sind, werden nicht von Microsoft Secure Score nachverfolgt. Sie können weiterhin Maßnahmen ergreifen, Sie werden jedoch nicht Ihre Bewertung beeinträchtigen. Wenn eine Aktion in der Zukunft von Microsoft Secure Score nachverfolgt wird und Sie Sie bereits abgeschlossen haben, spiegelt Ihre Secure Score automatisch die Änderung wider.

Wenn Sie auf eine Verbesserungs Aktion klicken, wird ein ausfliegen angezeigt. Um die Aktion abzuschließen, haben Sie einige Möglichkeiten:

1. Wählen Sie **Ansichtseinstellungen** , um den Konfigurationsbildschirm zu wechseln, und nehmen Sie die Änderung vor. Sie erhalten dann die Punkte, die die Aktion Wert ist, sichtbar am oberen Rand des Fly-Out. Es kann bis zu 24 Stunden dauern, bis Punkte aktualisiert werden.

2. Wählen Sie **über Drittanbieter auflösen** aus, da die Verbesserungs Aktion bereits durch eine Drittanbieteranwendung oder-Software adressiert wurde. Sie erhalten die Punkte, die die Aktion Wert ist, damit Ihr sicheres Ergebnis Ihre allgemeine Sicherheitsposition besser widerspiegelt. Wenn ein Drittanbieter das Steuerelement nicht mehr abdeckt, können Sie die Verbesserungs Aktion als nicht abgeschlossen kennzeichnen. Beachten Sie, dass Microsoft keine Sichtbarkeit darüber hat, ob die Punkte Anforderungen erfüllt sind, wenn die Verbesserungs Aktion als aufgelöst über Drittanbieter gekennzeichnet ist.

3. Wählen Sie **ignorieren** aus, da Sie sich entschieden haben, das Risiko zu übernehmen und die Verbesserungs Aktion nicht zu verabschieden. Nachdem Sie eine Verbesserungs Aktion ignoriert haben, wird die Gesamtanzahl der sicheren Punkte verringert. Sie können diese Aktion im Verlauf anzeigen oder jederzeit rückgängig machen.

4. Wählen Sie **Überarbeiten** aus, da für die Verbesserungs Aktion ein Teil Ihrer Umgebung regelmäßig überprüft werden muss, um Punkte zu erhalten und beizubehalten. Beispielsweise sollten die Regeln für die Post Fach Weiterleitung wöchentlich überprüft werden, um sicherzustellen, dass die Daten nicht in Ihrem Netzwerk extrahiert werden. Sie müssen keine Änderungen vornehmen, aber es muss eine Aktion ausgeführt werden. Wenn Sie die Regeln regelmäßig überarbeiten, erhalten Sie die Punkte. Wenn dies nicht der Fall ist, wird die Punktzahl reduziert.

![M365-Homepage](./media/secure-score/secure-score1x450.png) ![M365-Homepage](./media/secure-score/secure-score2x450.png)

*Abbildungen 2 & 3: Verbesserungs Aktions Flyouts*

## <a name="monitor-improvements-over-time"></a>Verbesserungen überwachen

Auf der Registerkarte **Verlauf** können Sie einen Graphen des Ergebnisses Ihrer Organisation anzeigen. Diese Ansicht enthält den globalen Durchschnitt, Branchendurchschnitt und ähnliche Anzahl von Arbeitsplätzen sowie alle Aktionen, die im ausgewählten Zeitbereich vorgenommen wurden. Sie können auch einen Datumsbereich anpassen und nach Kategorie filtern.

Die Bewertung wird einmal pro Tag berechnet (um 1:00 Uhr PST). Wenn Sie eine Änderung an einer gemessenen Aktion vornehmen, wird die Partitur automatisch am nächsten Tag aktualisiert. Beachten Sie, dass in einigen anderen Portalen Teile des Microsoft Secure Score (wie Windows Defender Security Center) angezeigt werden. Wenn Sie eine Verbesserungs Aktion ausführen und die Punktzahl in diesen Portalen erhöht wird, kann es bis zu 24 Stunden dauern, bis die aktualisierte Bewertung im Microsoft 365 Security Center angezeigt wird.  

## <a name="risk-awareness"></a>Risikobewusstsein

Microsoft Secure Score ist eine numerische Zusammenfassung Ihrer Sicherheitslage basierend auf Systemkonfigurationen, Benutzerverhalten und anderen sicherheitsbezogenen Messungen. Es ist kein absolutes Maß dafür, wie wahrscheinlich Ihr System oder Ihre Daten verletzt werden. Vielmehr stellt Sie dar, in welchem Umfang Sie Sicherheitskontrollen in Ihrer Microsoft-Umgebung eingeführt haben, die das Risiko von Verstößen kompensieren können. Kein Onlinedienst ist vollständig gegen Sicherheitsverstöße geschützt, und Secure Score sollte nicht als Garantie gegen Sicherheitsverletzungen interpretiert werden.

## <a name="we-want-to-hear-from-you"></a>Wir möchten von Ihnen hören

Wenn Sie Probleme haben, lassen Sie es uns bitte wissen, indem Sie in der [Security, Privacy _AMP_ Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) Community veröffentlichen. Wir überwachen die Community und helfen Ihnen.
