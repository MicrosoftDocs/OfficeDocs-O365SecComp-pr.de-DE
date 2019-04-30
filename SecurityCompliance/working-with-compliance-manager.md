---
title: Arbeiten mit Microsoft Compliance Manager
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: ec01bc8cbf1a1b59353d2f0840baa539e1331ef4
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473114"
---
# <a name="work-with-microsoft-compliance-manager"></a>Arbeiten mit Microsoft Compliance Manager

> [!IMPORTANT]
> Microsoft Compliance Manager ist ein Dashboard und Verwaltungstool, das eine Zusammenfassung Ihrer Datenschutz-und Compliance-Statur sowie Empfehlungen zur Verbesserung des Schutzes und der Compliance von Daten bereitstellt. Die im Compliance-Manager bereitgestellten Kundenaktionen sind Empfehlungen; Es ist Ihre Organisation, die Wirksamkeit dieser Empfehlungen in ihrem jeweiligen regulatorischen Umfeld vor der Implementierung zu bewerten. Empfehlungen im Compliance-Manager sollten nicht als Garantie für die Compliance interpretiert werden.

## <a name="access-compliance-manager"></a>Zugriff auf Compliance-Manager

Sie können über das Service Trust Portal auf den Compliance-Manager zugreifen. Alle Personen mit einem Microsoft-Konto oder mit einem Azure Active Directory-Organisationskonto können auf den Compliance-Manager zugreifen.
  
1. Wechseln Sie zu [https://servicetrust.microsoft.com](https://servicetrust.microsoft.com/).

2. Melden Sie sich mit Ihrem Microsoft-Dienstkonto an. Hierbei handelt es sich um Ihr Office 365-, Microsoft 365-oder Azure Active Directory-Benutzerkonto (Azure AD).

3. Wählen Sie im Dienst Vertrauensstellungs Portal **Compliance-Manager**aus. Dies ist die Preview-Version von Compliance-Manager. **Compliance-Manager (Classic)** ist der Link zur vorherigen Version von Compliance-Manager.

4. Wenn der GeheimhaltungsVertrag angezeigt wird, lesen Sie ihn, und wählen Sie **zustimmen** aus, um den Vorgang fortzusetzen. Sie müssen ein einziges Mal zustimmen, und dann wird das Compliance-Manager-Dashboard angezeigt.

Um Ihnen den Einstieg zu erleichtern, wird standardmäßig eine ISO/IEC 27001:2103-Bewertung für Office 365 für Ihre Organisation angezeigt.

## <a name="administration"></a>Verwaltung

Es gibt bestimmte Verwaltungsfunktionen, die nur dem mandantenadministrator zur Verfügung stehen und nur sichtbar sind, wenn Sie mit einem globalen Administratorkonto angemeldet sind. Bis der Administrator den Benutzern jedoch Compliance-Manager-Rollen zuweist, sind die Daten im Compliance-Manager für alle Benutzer in Ihrer Organisation sichtbar. Es wird empfohlen, die rollenbasierte Zugriffssteuerung zu implementieren, um zu bestimmen, wer auf Aktionen im Compliance-Manager zugreifen und diese ausführen kann.
  
### <a name="assigning-compliance-manager-roles-to-users"></a>Zuweisen von Compliance-Manager-Rollen zu Benutzern

Jede Compliance-Manager-Rolle hat geringfügig unterschiedliche Berechtigungen. Sie können die jeder Rolle zugewiesenen Berechtigungen anzeigen, die Benutzer, die in welchen Rollen sind, sowie Benutzer aus dieser Rolle über das Dienst Vertrauensstellungs Portal hinzufügen oder entfernen. Wählen Sie das Menüelement **Admin** aus, und wählen Sie die anzuzeigenden **Einstellungen** aus.
  
![STP-Verwaltungsmenü: ausgewählte Einstellungen](media/65a82b1b-d462-452f-988b-7e4263bd638e.png)
  
Hinzufügen oder Entfernen von Benutzern aus Compliance-Manager-Rollen
  
1. Wechseln Sie zu [https://servicetrust.microsoft.com](https://servicetrust.microsoft.com).

2. Melden Sie sich mit Ihrem globalen Azure Active Directory-Administratorkonto an.

3. Wählen Sie auf der oberen Menüleiste des Dienst Vertrauensstellungs Portals **Administrator** aus, und wählen Sie dann **Einstellungen**aus.

4. Wählen Sie in der Dropdownliste **Rolle auswählen** die Rolle aus, die Sie verwalten möchten.

5. Jeder Rolle hinzugefügte Benutzer werden auf der Seite **Rolle auswählen** aufgeführt.

6. Wählen Sie **Hinzufügen**aus, um dieser Rolle Benutzer hinzuzufügen. Wählen Sie im Dialogfeld **Benutzer hinzufügen** die Option Benutzer aus. Sie können durch die Liste der verfügbaren Benutzer Scrollen oder mit der Eingabe des Benutzernamens beginnen, um die Liste basierend auf Ihrem Suchbegriff zu filtern. Wählen Sie den Benutzer aus, der dieses Konto zur Liste Hinzufügen von **Benutzern** hinzufügt, die dieser Rolle bereitgestellt wurde. Wenn Sie mehrere Benutzer gleichzeitig hinzufügen möchten, beginnen Sie mit der Eingabe eines Benutzernamens, um die Liste zu filtern, und wählen Sie dann den Benutzer aus, der der Liste hinzugefügt werden soll. Wählen Sie **Speichern** aus, um die ausgewählte Rolle für diese Benutzer festzustellen. 

    ![Compliance-Manager – Benutzer hinzufügen](media/compliance-manager-add-users.png)
  
7. Um Benutzer aus dieser Rolle zu entfernen, wählen Sie die Benutzer aus, und wählen Sie **Löschen**aus.

    ![Compliance-Manager – Benutzer löschen](media/compliance-manager-delete-users.png)

## <a name="groups"></a>Gruppen

Gruppen ermöglichen es Ihnen, Assessments logisch zu organisieren und gemeinsame Informationen und Workflowaufgaben Zwischenbewertungen mit den gleichen oder verwandten vom Kunden verwalteten Steuerelementen gemeinsam zu nutzen. Sie können Bewertungen nach Jahr, Standard, Dienst, Team, Abteilung oder Agenturen innerhalb Ihrer Organisation gruppieren, um Kunden verwaltete Aktionen zu minimieren:
  
- **FFIEC ist Assessments 2019**
  - Office 365 + FFIEC ist
  - InTune + FFIEC ist
- **Datenschutzbewertungen**
  - Office 365 + ISO 27001:2013
  - Office 365 + ISO 27018:2014

Wenn Sie eine neue Bewertung erstellen, müssen Sie eine neue Gruppe für die Bewertung erstellen oder Sie einer vorhandenen Gruppe zuweisen. Gruppen können nicht als eigenständige Entitäten erstellt werden. Es wird empfohlen, *vor* dem Hinzufügen neuer Bewertungen eine Gruppierungs Strategie für Ihre Organisation zu bestimmen. Standardmäßig ist eine Gruppe mit dem Namen "Default Group" für Ihre anfänglichen Bewertungen verfügbar. Gruppen haben keine Sicherheitseigenschaften. Alle Berechtigungen sind mit Bewertungen verknüpft.

Wenn Sie mit Gruppen arbeiten, denken Sie daran:
  
- Zugehörige bewertungssteuerelemente in verschiedenen Bewertungen innerhalb derselben Gruppe werden automatisch aktualisiert, wenn Sie abgeschlossen sind.
- Neue Gruppen können Informationen aus einer vorhandenen Gruppe kopieren, wenn Sie eine neue Bewertung erstellen. Alle Informationen, die den Implementierungs Details und dem Testplan und der Verwaltungs Antwortfelder von vom Kunden verwalteten Steuerelementen aus Bewertungen in der Gruppe hinzugefügt werden, die Sie aus kopieren, werden in die gleichen (oder verknüpften) vom Kunden verwalteten Steuerelemente in der neuen Bewertung. Wenn Sie einer vorhandenen Gruppe eine neue Bewertung hinzufügen, werden allgemeine Informationen aus Bewertungen in dieser Gruppe in die neue Bewertung kopiert.
- Gruppennamen (auch als *Gruppen-IDs*bezeichnet) müssen innerhalb Ihrer Organisation eindeutig sein.
- Gruppen können Bewertungen für die gleiche Zertifizierung/Regulierung enthalten, aber jede Gruppe kann nur eine Bewertung für einen bestimmten Cloud-Dienst/Zertifizierungs Paar enthalten. Eine Gruppe kann beispielsweise nicht zwei Bewertungen für Office 365 und NIST CSF enthalten. Eine Gruppe kann mehrere Bewertungen für den gleichen Cloud-Dienst nur dann enthalten, wenn die entsprechende Zertifizierung/Regulierung für jeden unterschiedlich ist.
- Sobald eine Bewertung zu einer Bewertungsgruppe hinzugefügt wurde, kann die Gruppierung nicht geändert werden. Sie können die Bewertungsgruppe umbenennen, die den Namen der Bewertungs Gruppierung für alle Bewertungen ändert, die dieser Gruppe zugeordnet sind. Sie können eine Bewertung und eine neue Bewertungsgruppe erstellen und Informationen aus einer vorhandenen Bewertung kopieren, wodurch ein Duplikat dieser Bewertung in einer anderen Bewertungsgruppe erstellt wird.
- Archivierung bei der Bewertung wird die Beziehung zwischen dieser Bewertung und der Gruppe unterbrochen. Alle weiteren Aktualisierungen für andere zugehörige Bewertungen werden in der archivierten Bewertung nicht mehr berücksichtigt.

## <a name="tenant-management"></a>MandantenVerwaltung

Compliance-Manager (Preview) enthält eine neue Schnittstelle zum Verwalten neuer Datenelemente, die als **Mandantenverwaltung**bezeichnet werden. Diese Schnittstelle ermöglicht es Ihnen, Mandantenweite Einstellungen zu verwalten:

- **Dimensionen:** Anzeigen, hinzufügen und Anpassen von Metadaten für Vorlagen, BEWERTUNGEN und Aktionselemente, mit denen Sie benutzerdefinierte Pivots für Filter erstellen können.
- **Besitzer:** Geben Sie einen Besitzer für jedes Aktionselement an.
- **Kundenaktionen:** Verwalten der vollständigen Liste der im Compliance-Manager (Preview) enthaltenen Aktionselemente und aktivieren/deaktivieren der Secure Score-Überwachung für mit Secure Score integrierte Aktionen.

Wählen Sie **mandantEnverwaltung** aus, um die Verwaltungsoberfläche zu öffnen, und führen Sie die folgenden Schritte aus, um **Dimensionen**, **Besitzer**und **Kundenaktionen**zu verwalten.

### <a name="dimensions"></a>Maße

Dimensionen sind Metadaten, die Informationen zu einer Vorlage, einer Bewertung oder einem Aktionselement bereitstellen. Dimensionen verwenden das Konzept von Schlüsseln und Werten, wobei der DimensionsSchlüssel eine Eigenschaft darstellt und der DimensionsWert gültige Werte für die Eigenschaft darstellt. Beispielsweise gibt es im Compliance-Manager drei Arten von Aktionen. Sie werden durch einen DimensionsSchlüssel vom **Typ der Aktion** und Dimensionswerte der **Dokumentation**, des **Betriebs**und der **Technik**definiert. Sie können vorhandene Dimensionen ändern oder eigene Bemaßungen hinzufügen. Das Hinzufügen von Dimensionen ist häufig erforderlich, wenn benutzerdefinierte Vorlagen importieren.

#### <a name="add-a-dimension"></a>Hinzufügen einer Dimension

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Dimensionen**aus.
2. Wählen Sie **+ Dimension hinzufügen**aus.
3. Geben Sie im Feld **Schlüssel** einen eindeutigen Namen ein.
4. Aktivieren Sie optional mehrere Werte, die gleichzeitig für den gleichen Schlüssel verwendet werden sollen, und schieben Sie die Umschaltfläche für die Option **Mehrfachauswahl für Bemaßungen** auf ein.
5. Wählen Sie **+ Hinzufügen** aus, um einen Wert hinzuzufügen, indem Sie einen eindeutigen Namen angeben und auf das Symbol Speichern klicken.
6. Wiederholen Sie Schritt 5 für jeden Wert, den Sie hinzufügen möchten.
7. Klicken Sie auf **Speichern** , um die neue Dimension zu speichern.

#### <a name="edit-a-dimension"></a>Bearbeiten einer Dimension

Sie können einen DimensionsSchlüssel umbenennen, aber Sie können die Werte für benutzerdefinierte Dimensionen ändern.

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Dimensionen**aus.
2. Suchen Sie die zu bearbeitende Dimension, wählen Sie die Auslassungszeichen (...) aus, und wählen Sie **Bearbeiten**aus.
3. Wählen Sie **+ Hinzufügen** aus, um einen Wert hinzuzufügen, indem Sie einen eindeutigen Namen angeben und auf das Symbol Speichern klicken, oder wählen Sie den Wert aus, den Sie bearbeiten oder löschen möchten, und wählen Sie **Entfernen** oder **Bearbeiten**aus.
4. Wählen Sie **Speichern** aus, wenn Sie die Änderungen vorgenommen haben.

#### <a name="delete-a-dimension"></a>Löschen einer Dimension

Sie können benutzerdefinierte Bemaßungen bei Bedarf löschen.

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Dimensionen**aus.
2. Suchen Sie die zu löschende Dimension, wählen Sie die Auslassungszeichen (...) aus, und wählen Sie **Löschen**aus.
3. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **Löschen**aus.

### <a name="owners"></a>Besitzer

Besitzer werden verwendet, um den Verantwortlichen für jedes Steuerelement zu identifizieren. Alle integrierten Steuerelemente gehören Microsoft, von Kunden oder von beiden. Sie können benutzerdefinierte Werte für Besitzer erstellen, die verwendet werden können, um genauere Zuständigkeiten innerhalb Ihrer Organisation anzugeben. Sie können beispielsweise Besitzer erstellen, die bestimmte Gruppen, Teams oder Geschäftseinheiten innerhalb Ihrer Organisation darstellen.

#### <a name="add-an-owner"></a>Hinzufügen eines Besitzers

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Besitzer**aus.
2. Wählen Sie **+ Besitzer hinzufügen**aus.
3. Geben Sie einen Namen und eine Beschreibung für den Besitzer an, und wählen Sie **Speichern**aus. Die Beschreibung wird in der Spalte Besitzer angezeigt.

#### <a name="edit-an-owner"></a>Bearbeiten eines Besitzers

Ein Besitzername kann nicht bearbeitet werden, aber Sie können die Beschreibung ändern, die in der Spalte Besitzer angezeigt wird.

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Besitzer**aus.
2. Suchen Sie den zu bearbeitenden Besitzer, wählen Sie die Ellipsen (...) aus, und wählen Sie **Bearbeiten**aus.
3. Ändern Sie die Beschreibung nach Bedarf, und wählen Sie **Speichern**aus.

#### <a name="delete-an-owner"></a>Löschen eines Besitzers

1. Öffnen Sie **Mandantenverwaltung** , und wählen Sie **Besitzer**aus.
2. Suchen Sie den zu löschenden Besitzer, wählen Sie die Ellipsen (...) neben diesem aus, und wählen Sie **Löschen**aus.
3. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **Löschen**aus.

### <a name="customer-actions"></a>Kundenaktionen

Im Bereich Kundenaktionen werden alle Kundenaktionen für alle Vorlagen und Bewertungen im Compliance-Manager (Preview) angezeigt.

![Compliance-Manager – Benutzer hinzufügen](media/compliance-manager-customer-actions.png)

Auf einen Blick können Sie den Titel, den Besitzer, die Kategorie, die Durchsetzung und das Ergebnis einer Aktion sehen und feststellen, ob Sie mit Secure Score integriert ist. Sie können eine Aktion erweitern und **Weitere Informationen** auswählen, um die Beschreibung der Aktion zu lesen und auf Links in der Beschreibung zuzugreifen. Sie können diese Schnittstelle auch verwenden, um die Secure Score-Integration pro Aktion zu aktivieren und zu deaktivieren und benutzerdefinierte Aktionen hinzuzufügen. Aktionen, die über eine Secure Score-Integrationsfunktion verfügen, haben ein Auslassungszeichen (...).

#### <a name="enable-or-disable-secure-score-integration"></a>Aktivieren oder Deaktivieren der Integration sicherer Bewertungen

1. Wählen Sie die Auslassungspunkte (...) für die Aktion aus, die Sie ändern möchten, und wählen Sie **Bearbeiten**aus.
2. Aktivieren oder Deaktivieren der Option für das kontinuierliche Update für sichere Ergebnisse auf ein-oder ausschalten, um die kontinuierliche Überwachung über sicheres Ergebnis zu ermöglichen oder abzuschalten.
3. Klicken Sie auf **Speichern**.

#### <a name="add-a-customer-action"></a>Hinzufügen einer Kunden Aktion

1. Wählen Sie **+ Kunden Aktion hinzufügen**aus.
2. Geben Sie im Feld **Title** einen eindeutigen Titel für die Aktion ein.
3. Geben Sie im Feld **Maximale Konformitätsbewertung** eine Konformitätsbewertung für die Aktion an (Dies kann eine beliebige zahl von 1-99 sein).
4. Verwenden Sie **** die Dropdownliste Aktionstyp, um den Typ der hinzuzufügenden Aktion anzugeben. Wenn der Aktionstyp nicht vorhanden ist, können Sie ihn hinzufügen, indem Sie den Wert zum Dimensionsschlüssel Aktionstyp hinzufügen.
5. Verwenden Sie die Dropdown-Liste **Dimensionen** , um Bemaßungs Schlüssel und-Werte für die Aktion anzugeben oder hinzuzufügen.
6. Verwenden Sie das Dropdown-Menü **Besitzer** , um den Besitzer für Aktion anzugeben.
7. Wählen **+** Sie diese Option aus, um eine Beschreibung und einen Beschreibungstitel für die Aktion hinzuzufügen.
8. Wählen Sie das **X** aus, um das Blatt Beschreibung zu beenden.
9. Wählen Sie **Speichern** aus, um die Kunden Aktion zu speichern.

#### <a name="edit-a-customer-action"></a>Bearbeiten einer Kunden Aktion

1. Wählen Sie die Auslassungspunkte (...) für die Aktion aus, die Sie ändern möchten, und wählen Sie **Bearbeiten**aus.
2. Bearbeiten Sie die Aktion wie gewünscht, und wählen Sie **Speichern**aus.

#### <a name="delete-a-customer-action"></a>Löschen einer Kunden Aktion

1. Wählen Sie die Auslassungspunkte (...) für die Aktion aus, die Sie ändern möchten, und wählen Sie **Löschen**aus.
2. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **Löschen**aus.

## <a name="assessments"></a>Bewertungen

### <a name="add-an-assessment"></a>Hinzufügen einer Bewertung
  
1. Wählen Sie im Dashboard Assessments die Option **+ Assessment hinzufügen**aus.

2. Wenn das Blatt geöffnet wird, geben Sie die folgenden Informationen ein:

    - **Title (erforderlich):** Geben Sie einen Titel für Ihre Bewertung ein.
    - **Wählen Sie eine Vorlage aus (erforderlich):** Auswählen einer Standard-oder benutzerdefinierten Vorlage
    - **Wählen Sie eine Gruppe aus, oder fügen Sie eine neue Gruppe hinzu (erforderlich):** Wählen Sie eine vorhandene Gruppe aus, oder wählen Sie eine neue Gruppe hinzufügen aus, und geben Sie einen eindeutigen Gruppennamen an.
    - Möchten **Sie die Daten aus einer vorhandenen Gruppe kopieren? (optional):** schalten Sie das Steuerelement ein, um Gruppen Kopien zu aktivieren, und klicken Sie dann auf:
        - **Wählen Sie eine Gruppe aus (optional):** Wenn die Gruppen Kopie aktiviert ist, wählen Sie die Gruppe aus, aus der kopiert werden soll.
            - **Implementierungs Details (optional):** Wählen Sie diese Option aus, um Implementierungsdetails in die neue Gruppe zu kopieren
            - **Testplan & zusätzliche Informationen (optional):** Wählen Sie diese Option aus, um Testplan und zusätzliche Informationen in die neue Gruppe zu kopieren.
            - **Dokumente (optional):** Wählen Sie diese Option aus, um Dokumente in die neue Gruppe zu kopieren.

3. Wählen Sie **Speichern** aus, um die Bewertung zu erstellen.

 Die neue Bewertung wird im Assessment-Dashboard angezeigt und zeigt die folgenden Informationen an:

- Der Titel der Bewertung.
- Die Dimensionen der Bewertung, einschließlich Zertifizierung, Umgebung und Produkt, die auf die Bewertung angewendet wurden.
- Das Erstellungsdatum und das Datum der letzten Änderung.
- Die Beurteilungs Bewertung wird als Prozentsatz angezeigt.
- FortSchrittsindikatoren, die die Anzahl der bewerteten Microsoft-verwalteten und kundenbezogenen Steuerelemente anzeigen.

### <a name="copying-information-from-existing-assessments"></a>Kopieren von Informationen aus vorhandenen Bewertungen

Wenn Sie eine Bewertung erstellen, haben Sie die Möglichkeit, Informationen aus einer vorhandenen Gruppe zu kopieren. Auf diese Weise können Sie die in die kopierte Bewertung eingegebenen Informationen auf dieselben Steuerelemente in der neuen Bewertung anwenden. Wenn Sie beispielsweise über eine Gruppe für alle FFIEC-bezogenen Bewertungen in Ihrer Organisation verfügen, können Sie die folgenden Informationen aus vorhandenen Bewertungen kopieren:

- Implementierungs Details
- Testplan & zusätzliche Informationen
- Dokumente

#### <a name="copy-information-from-an-existing-assessment-to-a-new-assessment"></a>Kopieren von Informationen aus einer vorhandenen Bewertung in eine neue Bewertung
  
1. Wählen Sie im Assessment-Dashboard die Option **+ Add Assessment**aus.
    
2. Füllen Sie im Fenster **Bewertung hinzufügen** die folgenden Informationen aus:

    - **Title (erforderlich):** Geben Sie einen Titel für Ihre Bewertung ein.
    - **Wählen Sie eine Vorlage aus (erforderlich):** Wählen Sie eine Standard-oder benutzerdefinierte Vorlage aus.
    - **Wählen Sie eine Gruppe aus, oder fügen Sie eine neue Gruppe hinzu (erforderlich):** Wählen Sie **neue Gruppe hinzufügen** aus, und geben Sie einen eindeutigen Gruppennamen an.
    - Möchten **Sie die Daten aus einer vorhandenen Gruppe kopieren? (optional):** Umschalten des Steuerelements auf ein, um Gruppen Kopien zu aktivieren, und dann:- **Wählen Sie eine Gruppe aus (optional):** wenn Gruppen Kopie aktiviert ist, wählen Sie die Gruppe aus, aus der kopiert werden soll.
            - **Implementierungs Details (optional):** Wählen Sie diese Option aus, um Implementierungsdetails in die neue Gruppe zu kopieren.
            - **Testplan & zusätzliche Informationen (optional):** Wählen Sie diese Option aus, um Testplan und zusätzliche Informationen in die neue Gruppe zu kopieren.
            - **Dokumente (optional):** Wählen Sie diese Option aus, um Dokumente in die neue Gruppe zu kopieren.

3. Wählen Sie **Speichern** aus, um die Bewertung zu erstellen.

### <a name="viewing-assessments"></a>Anzeigen von Bewertungen

#### <a name="view-an-assessment"></a>Anzeigen einer Bewertung
  
1. Wählen Sie im Dashboard Assessments den Namen der Bewertung aus, um ihn zu öffnen, und zeigen Sie die Informationen zu Aktionselementen und Steuerelementen an.

Nachfolgend finden Sie ein Beispiel für die Bewertung für Office 365 und ISO 27001. Die erste Ansicht zeigt die Ansicht neue Aktionselemente im Compliance-Manager (Preview).

![Ansicht "Compliance-Manager-Aktionselemente"](media/compliance-manager-action-items.png)

Die Aktionen werden in alphabetischer Reihenfolge aufgeführt, und jeder Aktion wird eine Bewertung und ein Besitzer zugewiesen. Wählen Sie den Link **Weitere** Informationen aus, um die Details der einzelnen Aktionen zu lesen. 

![Ansicht "Compliance-Manager-Aktionselemente"](media/compliance-manager-actions-read-more.png)

Wählen Sie den Link **überprüfen** aus, um die Aktion zu verwalten, zuzuweisen, zu implementieren und zu testen. Nachfolgend finden Sie eine Beispielaktion.

![Compliance-Manager-Aktionsansicht](media/compliance-manager-action.png)

In früheren Versionen von Compliance-Manager wurde der Workflow zum Implementieren von Anforderungen auf der Steuerungsebene ausgeführt. Ein Compliance Officer würde jemand ein Steuerelement zuweisen, um das Steuerelement zu implementieren. Es gab zwei Nachteile:

- Steuerelementen waren häufig mehrere Aktionen zugeordnet, und der Benutzer, dem ein Steuerelement zugewiesen wurde, ist möglicherweise nicht die richtige Person, um alle Aktionen abzuschließen, die zum Implementieren des Steuerelements erforderlich waren.
- Das Kombinieren separater Aufgaben in einer einzigen Aktion verhinderte die Erfassung der Signale und der Telemetrie, die verwendet werden, um Änderungen der Mandanten Konfiguration im Compliance-Manager (Preview) automatisch aufzuzeichnen.

Im Compliance-Manager (Preview) wurde der Workflowprozess von der Steuerungsebene auf die Aktionsebene verschoben. Beim Überprüfen einer Aktion können die folgenden Felder zum Verwalten des Aktions Workflows verwendet werden:

- **Benutzer zuweisen:** Wählen Sie dieses Feld aus, um den Benutzer auszuwählen oder einzugeben, dem diese Aktion zugewiesen werden soll. Sie können in der Liste einen Bildlauf durchführen oder einen Namen eingeben, um Sie zu finden, und wählen Sie Sie aus.
- **Dokumente verwalten:** Sie können den Nachweis der Implementierung in Form von Office-Dokumenten, Bilddateien und Screenshots, PowerShell-Ausgabe in CSV oder TXT und PDFs hochladen.
- **Implementierungs Status:** Wird verwendet, um den aktuellen Implementierungsstatus der Aktion anzugeben. Mögliche Werte sind nicht implementiert, implementiert, alternative Implementierung, geplant, und nicht im Bereich.
- **Implementierungsdatum:** Das Datum, an dem die Aktion ausgeführt wurde.
- **Test Ergebnis:** Wird verwendet, um die Ergebnisse der Implementierungs Überprüfung anzugeben. Mögliche Werte werden nicht bewertet, übergeben, fehlgeschlagen-geRinges Risiko, FehlgeSchlagenes-mittleres Risiko, fehlgeschlagen-hohes Risiko und nicht im Umfang.
- **Test Datum:** Das Datum, an dem die Validierung stattgefunden hat.
- **Hinweise zur Implementierung:** Geben Sie die Implementierungsdetails für Ihre Organisation zusammen mit allen Notizen ein, die Sie hinzufügen möchten.
- **Testplan:** Geben Sie die Test Plan Details für diese Aktion zusammen mit allen Notizen ein, die Sie hinzufügen möchten.
- **Weitere Informationen:** Geben Sie zusätzliche Informationen zu dieser Aktion oder deren Implementierung in Ihrer Organisation zusammen mit allen Notizen ein, die Sie hinzufügen möchten.

Compliance-Manager (Preview) enthält auch das steuerelementbasierte Pivot in früheren Versionen. Klicken Sie auf das **Steuerelement-Info** -Dashboard, um es anzuzeigen. Sie können Informationen zu Steuerelementen auf der Ebene der Bewertung und der Vorlage anzeigen. Nachfolgend finden Sie ein Beispiel für das Steuerelement-Info-Dashboard für Bewertungen.

![Kompatibilitäts-Manager-Steuerelement-Info Ansicht](media/compliance-manager-controls-info.png)

Für Bewertungen wird das Steuerelement Info-Dashboard angezeigt:

- Eine **Gruppen** Dropdownliste, um auszuwählen, welche Gruppe angezeigt werden soll (wenn mehrere Gruppen verwendet werden).
- Ein **Bewertung** -Dropdown, um auszuwählen, welche Bewertung angezeigt werden soll.
- Metadaten zur ausgewählten Bewertung, einschließlich:
    - Eine Statusanzeige für **bewertete Steuer** Elemente mit der Anzahl der bewerteten Steuerelemente für die Gesamtzahl der Steuerelemente.
    - Der aktuelle **Kompatibilitäts Faktor** für die Bewertung, als Prozentsatz angezeigt.
    - Details zu der **Zertifizierung** und dem **Produkt** , die bei der Bewertung verwendet werden.
    - Der aktuelle **Status** und das Datum der letzten **Änderung** für die Bewertung.
- Eine Liste der **in-Scope-Dienste** für die Bewertung.
- Details der Steuerelemente, gruppiert nach Steuerelement Familie, mit Links zu Kundenaktionen und Microsoft-Implementierungsdetails:
    - **Ihre Aktionen** zeigt die Kundenaktionen an, die Sie ausführen können, um einige oder alle Anforderungen des Steuerelements zu erfüllen. Vielen Steuerelementen sind mehrere Aktionen zugeordnet, und alle einem Steuerelement zugeordneten Aktionen werden hier angezeigt. Die Aktionen hier haben dieselbe Benutzeroberfläche wie im Dashboard Aktionen.
    - **Microsoft-Aktionen** zeigt die Liste der Steuerelemente aus dem internen Microsoft-Framework an, die für das ausgewählte Zertifizierungs Steuerelement gelten. Wählen Sie für jedes interne Steuerelement **implementiert** aus, um die Implementierungs-und testDetails von Microsoft sowie das Testergebnis und das Test Datum anzuzeigen (siehe unten).

![Compliance-Manager – Microsoft-Aktionsansicht](media/compliance-manager-microsoft-action.png)

### <a name="export-an-assessment"></a>Exportieren einer Bewertung

Sie können eine Bewertung in eine Excel-Datei für die Compliance-Verantwortlichen in Ihrer Organisation oder für externe Auditoren und Regulierer exportieren. Der Bericht ist eine Momentaufnahme der Bewertung als Datum und Uhrzeit der Erstellung des Berichts. Der Bericht enthält die Details für alle von Microsoft und vom Kunden verwalteten Steuerelemente für die Bewertung, die Steuerung des Implementierungsstatus, die Steuerung des Test Datums und der Testergebnisse sowie Links zu hochgeladenen Beweisdokumenten. Sie sollten den Beurteilungsbericht vor der Archivierung einer Bewertung exportieren, da Archivierte Bewertungen keine Links zu hochgeladenen Dokumenten aufbewahren.
  
### <a name="export-an-assessment-report"></a>Exportieren eines Bewertungsberichts
  
1. Wählen Sie im Compliance-Manager-Dashboard die Registerkarte **Steuerelemente-Info** aus.
2. Wählen Sie die **Gruppe** und **Bewertung** in den Dropdownmenüs für die Bewertung aus, die Sie exportieren möchten.
3. Klicken Sie auf die Schaltfläche **exportieren** .

Der Beurteilungsbericht wird als Excel-Datei in ihrer Browsersitzung heruntergeladen. Der Dateiname für die Excel-Datei ist standardmäßig der Titel der Bewertung.

### <a name="archive-a-template-or-an-assessment"></a>Archivieren einer Vorlage oder einer Bewertung

Wenn Sie eine Vorlage oder Bewertung abgeschlossen haben und Sie nicht mehr zu Compliance-Zwecken benötigen, können Sie Sie archivieren. Wenn eine Vorlage oder eine Bewertung archiviert wird, wird Sie aus der Standardansicht entfernt, und Sie müssen das Kontrollkästchen archiviert anzeigen aktivieren, um Sie anzuzeigen.

![Compliance-Manager – Microsoft-Aktionsansicht](media/compliance-manager-archive-assessment-view.png)
  
> [!IMPORTANT]
> Archivierte Bewertungen behalten Ihre Links zu hochgeladenen Beweisdokumenten nicht bei. Es wird dringend empfohlen, dass Sie die Bewertung vor der Archivierung exportieren, um Links zu den Beweisdokumenten im Bericht beizubehalten.
  
#### <a name="archive-a-template"></a>Archivieren einer Vorlage

1. Öffnen Sie das Dashboard **Vorlagen** .
2. Suchen Sie die zu archivierende Vorlage, und wählen Sie das Symbol Archiv aus.
3. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **Archiv**aus.

#### <a name="archive-an-assessment"></a>Archivieren einer Bewertung

1. Öffnen Sie das Dashboard **Bewertungen** .
2. Wählen Sie die **Gruppe** aus der Dropdownliste aus, die die zu archivierende Bewertung enthält.
3. Suchen Sie die zu archivierende Bewertung, und wählen Sie das Symbol Archiv aus.
4. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **Archiv**aus.

#### <a name="view-archived-assessments"></a>Anzeigen archivierter Bewertungen
  
1. Öffnen Sie **** die Registerkarte Assessments-Dashboard, und aktivieren Sie das Kontrollkästchen **Archivierte anzeigen** .
2. Die archivierten Bewertungen werden im Abschnitt **Archivierte Bewertungen** angezeigt.
3. Wählen Sie den zu öffnenden Bewertungs Namen aus, und zeigen Sie den Test an.

#### <a name="activate-an-archived-assessment"></a>Aktivieren einer archivierten Bewertung

1. Klicken Sie auf der Registerkarte **Bewertungen** auf das Kontrollkästchen **archiviert anzeigen** .
2. Die archivierten Bewertungen werden im Abschnitt **Archivierte Bewertungen** angezeigt.
3. Suchen Sie nach der Bewertung, die Sie aktivieren möchten, und wählen Sie das Symbol aktivieren aus.
4. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **aktivieren**aus.

## <a name="controls-and-actions"></a>Steuerelemente und Aktionen

Steuerelemente und Aktionen sind die primären Daten Pivots, die im Compliance-Manager (Preview) verwendet werden. Die Steuerelement-Pivot, die in früheren Versionen von Compliance-Manager vorhanden war, wurde verbessert, um die Microsoft-und Kunden Steuerelemente in den gleichen Steuerelementfamilien anzuzeigen. Diese konsolidierte Ansicht erleichtert das Anzeigen des vollständigen Modells für gemeinsame Aufgaben pro Steuerelement. Die Aktion Pivot ist neu im Compliance-Manager (Preview) und soll eine optimierte Übersicht über alle von Microsoft empfohlenen Aktionen bieten.

### <a name="controls"></a>Steuerelemente

Steuerelemente können im Steuerelement-Info-Dashboard angezeigt werden. Steuerelemente stellen die Anforderungen aus einem Standard, einer Zertifizierung, einer Regulierung oder einem Framework dar. Um diese Anforderungen über mehrere Standards, Verordnungen usw. abzubilden und diese mit Aktionen zu verknüpfen, wird alles so behandelt, als ob es sich um ein Steuerelement handelt. Wie bei einem Steuerelement Framework wurden beispielsweise Vorschriften wie HIPAA nach Abschnitt aufgeschlüsselt, und die HIPAA-Steuerelemente im Compliance-Manager verwenden dasselbe Nummernschema wie die folgenden Abschnitte:

![Compliance-Manager – Details zu Microsoft-Steuerelementen](media/compliance-manager-control-details.png)

Es gibt drei Arten von Steuerelementen. Zwei werden von Microsoft in den integrierten Vorlagen bereitgestellt, und die dritte wird von Kunden in benutzerdefinierten Vorlagen erstellt und verwaltet. Die drei Typen sind:

1. Von **Microsoft verwaltete Steuerelemente (mm):** Dies sind Steuerelemente, für die nur Microsoft verantwortlich ist. Sie werden in den in-Box-Vorlagen angezeigt und werden dem Compliance-Manager von Microsoft hinzugefügt.
2. Vom **Kunden verwaltete Steuerelemente (cm):** Dies sind Steuerelemente, für die nur Kunden verantwortlich sind. Sie werden in den in-Box-Vorlagen angezeigt und werden dem Compliance-Manager von Microsoft oder Kunden hinzugefügt. Der Kunde kann auch von Microsoft bereitgestellte vom Kunden verwaltete Steuerelemente bearbeiten oder deaktivieren.
3. **FreiGegebene Steuerelemente (SM):** hierbei handelt es sich um Steuerelemente, bei denen Microsoft und der Kunde Verantwortung übernehmen. Diese werden in den in-Box-Vorlagen angezeigt und werden dem Compliance-Manager von Microsoft hinzugefügt.

### <a name="actions-items"></a>Aktionselemente

Aktionselemente sind die empfohlenen Aufgaben für die Implementierung der Anforderungen einer Norm oder Regelung oder zum Testen, überprüfen und Dokumentieren der Implementierungsanforderungen Ihrer Organisation. Aktionen sind einem oder mehreren Steuerelementen zugeordnet. Jedem Steuerelement ist eine oder mehrere Aktionen zugeordnet, und jede Aktion kann einem oder mehreren Steuerelementen zugeordnet werden. Aktionen sind Teil des Haupt Workflows im Compliance-Manager (Preview), da es sich um Objekte handelt, die von Ihrer Organisation zugewiesen, verfolgt und validiert werden.

#### <a name="assign-action-items"></a>Aktionselemente zuweisen
  
1. Wählen Sie im Dashboard **Aktionselemente** die **Gruppe** aus, die die Bewertung (en) enthält, deren Aktion Sie zuweisen möchten.
2. Wählen Sie in der Dropdownliste **Bewertung** die Bewertung aus, deren Aktion Sie zuweisen möchten, oder wählen Sie **alle** aus der Dropdownliste aus, um alle verfügbaren Aktionen anzuzeigen.
3. Suchen Sie die Aktion, die Sie zuweisen möchten, und wählen Sie in der Spalte **Besitzer** den Link für **Überprüfung**, **implementiert** oder **Testen**aus.
4. Wählen Sie das Feld **Benutzer zuweisen** aus, und eine Liste der Benutzer in Ihrer Organisation wird angezeigt. Scrollen Sie in der Liste, wählen Sie Benutzer aus, oder Filtern Sie die Liste, um einen Benutzer auszuwählen, indem Sie den Namen des Benutzers eingeben.
5. Geben Sie im Feld ImplementierungsHinweise alle Notizen ein, die Sie dem zugewiesenen Benutzer übermitteln möchten.
6. Wählen Sie **Speichern** aus, um die Aktion zuzuweisen.

#### <a name="reassign-action-items"></a>Erneutes Zuweisen von Aktionselementen

Mit dieser Funktion kann eine Organisation aktive oder ausstehende Abhängigkeiten für das Benutzerkonto entfernen, indem eine Aktion einem neuen Benutzer zugewiesen wird.

1. Wählen Sie im Dashboard **Aktionselemente** die **Gruppe** mit den Bewertungen aus, deren Aktion Sie erneut zuweisen möchten.
2. Wählen Sie in der Dropdownliste **Bewertung** die Bewertung aus, deren Aktion Sie erneut zuweisen möchten, oder wählen Sie **alle** aus der Dropdownliste aus, um alle verfügbaren Aktionen anzuzeigen.
3. Suchen Sie die Aktion, die Sie erneut zuweisen möchten, und wählen Sie in der Spalte **Besitzer** den Link für **Überprüfung**, **implementiert**oder **Testen**aus.
4. Löschen Sie den vorhandenen Benutzer aus dem Feld **Benutzer zuweisen** , und wählen Sie einen anderen Benutzer aus der Liste der Benutzer aus, oder Filtern Sie die Liste, um einen Benutzer auszuwählen, indem Sie den Namen des Benutzers eingeben.
5. Geben Sie im Feld ImplementierungsHinweise alle Notizen ein, die Sie dem Benutzer übermitteln möchten.
6. Wählen Sie **Speichern** aus, um die Aktion erneut zuzuweisen.

## <a name="templates"></a>Vorlagen

Eine Vorlage ist das Basisobjekt im Compliance-Manager (Preview), das einem Produkt und einer Zertifizierung (beispielsweise Standard, Regulation, Control Framework usw.) zugeordnet ist. Vorlagen können im Dashboard Vorlagen angezeigt und hinzugefügt werden.

![Compliance-Manager – Microsoft-Vorlagen Dashboard](media/compliance-manager-template-dashboard.png)
 
Im Dashboard werden die einzelnen Vorlagen sowie die Zertifizierung und das Produkt angezeigt, die mit der Vorlage verknüpft sind, das Datum, an dem die Vorlage erstellt und zuletzt geändert wurde, die Anzahl der Kunden-und Microsoft-verwalteten Steuerelemente, die maximale KonformitätsBewertung für die Vorlage und den Status der Vorlage (beispielsweise genehmigt, ausStehende Genehmigung, importiert).

Den integrierten Vorlagen ist jeweils eine integrierte Bewertung zugeordnet, aber Sie können zusätzliche Bewertungen basierend auf integrierten Vorlagen erstellen, und Sie können eigene Vorlagen importieren und benutzerdefinierte Bewertungen basierend auf diesen erstellen.

### <a name="create-a-template"></a>Erstellen einer Vorlage

Sie können eine Vorlage erstellen, indem Sie eine vorhandene Vorlage kopieren oder eine benutzerdefinierte Vorlage importieren. Es gibt ein bestimmtes Format und Schema, das für Vorlagendaten verwendet werden muss, oder es wird nicht in Compliance-Manager importiert. Eine Datei mit dem korrekten Schema und den Beispieldaten kann hier heruntergeladen werden.
Jede benutzerdefinierte Vorlage sollte sich in einer separaten Excel-Arbeitsmappe (im. xls-oder XLSX-Format) befinden, die fünf Registerkarten enthält:

1. Vorlagen Bewertung
2. ControlFamily
3. Aktionen
4. Besitz
5. Maße

Das in jeder Registerkarte verwendete Schema wird nachfolgend beschrieben.

#### <a name="template-assessment-tab"></a>Registerkarte "Bewertung"

Diese Registerkarte hat eine einzelne Spalte:

- **inScopeServices**: durch trennzeichengetrennte Liste der Produkte oder Dienste, die sich im Bereich der Vorlage befinden.

#### <a name="controlfamily-tab"></a>Registerkarte "ControlFamily"

Diese Registerkarte enthält Spalten, die die Steuerelemente definieren, die den auf der Registerkarte Aktionen aufgeführten Aktionen zugeordnet sind, und enthält Details wie Steuerelementname, Familie, Titel und Beschreibung.  Die Spalten für diese Registerkarte, die innerhalb von Excel in der unten aufgeführten Reihenfolge sortiert werden müssen, sind: 

- **ControlName:** Steuerelementname aus Zertifizierung/Standard/Regulierung usw.
- **controlFamily:** Steuerelement Familie aus Zertifizierung/Standard, Regulierung usw.
- **controlTitle:** Steuerelement Titel aus Zertifizierung/Standard/Regulierung usw.
- **controlDescription:** Steuerelementbeschreibung aus Zertifizierung/Standard/Regulierung usw.
- **controlVersion:** Optionale Steuerelement Versionsinfo.  Beispiel: für NIST 800-53 ist der aktuelle Wert Rev 4, daher ist die controlVersion 4.  Für CSA CCM ist es 3.0.1.
- **isDisabled:** Verwenden Sie TRUE oder FALSE, um anzugeben, ob das Steuerelement deaktiviert wurde.
- **ControlType:** Verwenden Sie CM, um anzugeben, dass es sich um vom Kunden verwaltete Steuerelemente handelt.
- **controlComplianceScore:** Summe der Punktzahl aller Aktionen, die dem Steuerelement zugewiesen sind.
- **controlActionTitle:** Double Semi-Colon-Delimited Liste aller actionTitles für dieses Steuerelement, wie auf der Registerkarte "Aktionen" aufgelistet. 

#### <a name="actions-tab"></a>Registerkarte "Aktionen"

Diese Registerkarte enthält Spalten, die einzelne Aktionen definieren, und enthält Details wie Aktionstitel, Besitz und Dimensionen. Die Spalten für diese Registerkarte, die innerhalb von Excel in der unten aufgeführten Reihenfolge sortiert werden müssen, sind: 

- **actionTitle:** Der Titel der Aktion. Jeder Titel muss eindeutig sein, und es wird empfohlen, Pascal Case zu verwenden.
- **actionRelatedODVs:** Doppelte durch Semikolons getrennte Liste von actionTitles, die übergeordnete Elemente des in der actionTitle-Spalte aufgeführten Kinds sind. In einer übergeordneten/untergeordneten Beziehung stellt das übergeordnete Element das hohe Wasserzeichen dar. Wenn Sie also eine übergeordnete Aktion abgeschlossen haben, schließen Sie auch alle untergeordneten Aktionen ab. Beispielsweise, wenn Sie ähnliche Anforderungen haben, aber unterschiedliche Standardwerte wie Kennwortlänge, wobei eine Norm/Verordnung mindestens 15 Zeichen erfordert und eine andere mindestens 12 oder 10. 15 wäre das übergeordnete Element in diesem Beispiel, und wenn Sie mindestens 15 Zeichen konfigurieren, erfüllen Sie auch die Aktionen, die 12 oder 10 Zeichen in anderen Bewertungen empfehlen.

    > [!NOTE]
    > Die actionRelatedODVs-Spalte ist eine erforderliche Spalte für das Schema; Das Feature (zugehörige Aktionen) ist jedoch im Compliance-Manager (Preview) nicht verfügbar.  Sie wird in einer späteren Version hinzugefügt.

- **actionDimensionValues:** Doppelte durch Semikolons getrennte Liste der anwendbaren Dimensionen aus der Registerkarte Dimensionen unter Verwendung des folgenden Formats:

    ```
    Dimension Key::Dimension Value;;Dimension Key::Dimension Value.
    ```
    
    Beispiel:

    ```
    Product::Office 365;;Certification::NIST CSF
    ```

    Alle Dimensionen, die in einer benutzerdefinierten Vorlage verwendet werden, müssen auf der Registerkarte Dimensionen der Importdatei angezeigt werden, auch wenn Sie bereits im Dimensions-Dashboard aufgeführt sind. Wenn Sie neue Bemaßungs Schlüssel oder-Werte hinzufügen, müssen Sie diese zuerst dem Dimensions-Dashboard hinzufügen.
- **actionScore:** Numerischer Wert für jede Aktion, die das Ergebnis für diese Aktion darstellt. Es wird empfohlen, das von den integrierten Bewertungen verwendete Bewertungsmodell zu befolgen, das auf dem Zweck und der Erzwingung der einzelnen Aktionen basiert.
- **actionOwnership:** Doppelte durch Semikolons getrennte Liste der Besitzer. Alle aufgeführten Besitzer müssen auf der Registerkarte Ownership enthalten sein.
- **actionDescription:** Text jeder Aktion, die eindeutig sein muss. Dieses Feld unterstützt Abschriften Sprache wie unten beschrieben.

#### <a name="ownership-tab"></a>Registerkarte "Ownership"

Diese Registerkarte enthält Spalten, die Besitzer für jede Aktion definieren.  Die Spalten für diese Registerkarte, die innerhalb von Excel in der unten aufgeführten Reihenfolge sortiert werden müssen, sind:

- **ownershipname:** Eindeutiger Name des Besitzers/Verantwortlichen.
- **ownershipDescription:** Beschreibung des Besitzers/Verantwortlichen.

#### <a name="dimensions-tab"></a>Registerkarte "Dimensionen"

Diese Registerkarte enthält Spalten, die die Dimensionen definieren, die einer Aktion zugeordnet werden können.  Die Spalten für diese Registerkarte, die innerhalb von Excel in der unten aufgeführten Reihenfolge sortiert werden müssen, sind:

- **dimensionKey:** Liste der Schlüssel, die für Dimensionen verwendet werden. Beispielsweise Produkt, Zertifizierung usw.
- **dimensionvalue:** Eindeutiger Wert für jeden Dimensionsschlüssel. Beispielsweise Office 365, InTune, Azure, Custom Product usw.
- **allowMultiSelect:** Verwenden Sie TRUE oder FALSE, um anzugeben, dass mehrere Dimensionswerte für einen einzelnen Dimensionsschlüssel ausgewählt werden können.

#### <a name="using-markdown-language-in-description-fields"></a>Verwenden von Abschriften Sprache in BeschreibungsFeldern

Vorlagen und Bewertungen unterstützen die Verwendung der Abschriften Sprache für einige Textelemente und Formatierungen.  Es gibt drei Formatierungselemente der Abschriften Sprache, die im Compliance-Manager verwendet werden:

- AufZählungsZeichen und nummerierte Listen
- Hyperlinks
- Fettdruck

AufZählungsZeichen werden als Sternchen anstelle von Word-oder Excel-Aufzählungszeichen dargestellt. Beispiel:

```
* Item A
* Item B
* Item C
```

Zahlen werden als Zahlen dargestellt, jedoch mit Leerzeichen für Einzug (drei Leerzeichen pro Ebene) und nur Zahlen, die für alle Unterebenen verwendet werden (beispielsweise keine Buchstaben).  Beispiel:
   1. Element A
   2. Element B
      1. Unterelement A
      2. Unterelement B
   3. Element C
   4. Element D
      1. Unterelement A
      2. Unterelement B
   5. Element E

Hyperlinks werden erstellt, indem Klammern um den Hyperlinktext und den Hyperlink selbst in Klammern unmittelbar neben der schließenden Klammer platziert werden.  Beispiel:

```
Click [here](https://www.microsoft.com) to go to Microsoft’s home page.
```
Dieser Text wird wie folgt gerendert: Klicken Sie [hier](https://www.microsoft.com) , um zur startSeite von Microsoft zu gelangen.
Wie im obigen Beispiel dargestellt, rendert der Compliance-Manager keine URLs mit Unterstreichung.

Fettdruck ist nur zwei Sternchen auf jeder Seite des Texts, die fett formatiert werden sollen.  Beispiel:

```
**This text will render in bold**
```
**Dieser Text wird fett formatiert.**

### <a name="create-a-template"></a>Erstellen einer Vorlage

Sie können eine Vorlage erstellen, indem Sie eine vorhandene Vorlage kopieren oder Vorlagendaten aus Excel importieren. Beim Importieren von Daten aus Excel erfordert die Vorlage zwei verschiedene Compliance-Manager-Administratoren, um die Daten zu veröffentlichen (eine für die Veröffentlichung und eine zur Genehmigung).

#### <a name="create-a-template-by-copying-an-existing-template"></a>Erstellen einer Vorlage durch Kopieren einer vorhandenen Vorlage

1. Öffnen Sie das Dashboard **Vorlagen** , und wählen Sie **+ Vorlage hinzufügen**aus.
2. Geben Sie im Feld **Vorlagenname eingeben** einen eindeutigen Namen für die Vorlage ein.
3. Aktivieren Sie das Kontrollkästchen **aus einer vorhandenen Vorlage kopieren** , und wählen Sie die Vorlage aus der Dropdownliste aus, die Sie kopieren möchten.
4. Fügen Sie optional zusätzliche Dimensionen hinzu.
5. Wählen Sie **Add to Dashboard**aus.

#### <a name="create-a-template-by-importing-data"></a>Erstellen einer Vorlage durch Importieren von Daten

1. Öffnen Sie das Dashboard **Vorlagen** , und wählen Sie **+ Vorlage hinzufügen**aus.
2. Geben Sie im Feld **Vorlagenname eingeben** einen eindeutigen Namen für die Vorlage ein.
3. Fügen Sie eine oder mehrere Dimensionen hinzu. Auch wenn die von Ihnen verwendeten Dimensionen bereits im Dimensions-Dashboard aufgeführt sind, müssen Sie weiterhin in der Importdatei aufgeführt werden.
4. Wählen Sie **Durchsuchen** aus, um zum Speicherort der Importdatei zu navigieren, wählen Sie Sie aus, und wählen Sie **Öffnen**aus.
5. Die Importdatei wird validiert und gibt die Anzahl von Steuerelementen und Steuerelementfamilien an, die erkannt wurden. Wenn Fehler vorliegen, wird ein Link zu einer geänderten Version der Importdatei bereitgestellt, die Fehlerdetails enthält. Alle Fehler müssen aufgelöst werden, bevor die Daten importiert werden.
6. Nachdem die Datenvalidierung erfolgreich durchlaufen wurde, wählen Sie **Add to Dashboard**aus.
7. Die importierte Vorlage wird im Dashboard **Vorlagen** angezeigt und hat den Status **importiert**. Wählen Sie die Ellipsen (...) aus, und wählen Sie **veröffentlichen** aus, um die Vorlage zu veröffentlichen. Wenn die Bestätigungsmeldung angezeigt wird, wählen Sie **veröffentlichen**aus. Der Vorlagenstatus wird in **AusstehenDe Genehmigung**geändert.
8. Ein anderer Benutzer mit der Rolle Compliance-Manager-Administrator muss die Vorlage im Dashboard Vorlagen genehmigen. Sie müssen die Ellipsen (...) auswählen und die **** Option Genehmigen auswählen. Wenn die Bestätigungsmeldung angezeigt wird ****, wählen Sie genehmigen aus. Die Vorlage kann nun verwendet werden.

### <a name="customize-a-template"></a>Anpassen einer Vorlage

Vorlagen können durch zusätzliche benutzerdefinierte Steuerelemente angepasst werden. Alle benutzerdefinierten Steuerelemente gelten als vom Kunden verwaltete Steuerelemente.

#### <a name="add-a-custom-control-to-a-template"></a>Hinzufügen eines benutzerdefinierten Steuerelements zu einer Vorlage

1. Öffnen Sie die **Vorlage** , die Sie ändern möchten.
2. Wählen Sie + benutzerdefiniertes Steuerelement **Hinzufügen** aus.
3. Wählen Sie eine **Steuerelement Familie** aus der Dropdownliste aus, oder geben Sie eine neue Steuerelement Familie ein, wenn Sie nicht vorhanden ist.
4. Geben Sie im Feld **Steuerelement-ID** einen eindeutigen Namen oder eine eindeutige ID für das Steuerelement ein.
5. Geben Sie den Steuerelement Titel im Feld **Title** an.
6. Geben Sie die Anforderungen und andere Informationen für das Steuerelement im Feld **Beschreibung** an.
7. Wählen Sie **Kunden Aktion zuweisen** aus.
8. Suchen Sie die Aktion (en), die Sie dem Steuerelement zuweisen möchten:
    - Verwenden Sie **Filter nach Dimension** , um Dimensionen zu verwenden, die den Aktionen zugeordnet sind, um Sie zu suchen und aufzulisten.
    - Verwenden Sie den **Filter nach Besitzer** , um die Besitzer zu verwenden, die den Aktionen zugewiesen sind, um Sie zu suchen und aufzulisten.
    - Wählen Sie **** einen Aktionstyp aus der Dropdownliste aus, um Aktionen nach Typ aufzulisten.
    - Geben Sie den Titel der zu suchenden Aktion ein, und Listen Sie Sie auf.
9. Anhand der Kriterien in Schritt 8 wird eine Liste der **ÜbereinstimmenDen Aktionen** angezeigt. Wählen Sie die erste Aktion aus, die Sie dem Steuerelement zuweisen möchten.
10. Die Details der Aktion werden angezeigt. Wählen Sie die zu verwendende **Beschreibung** aus, und wählen Sie **Fertig**aus.
11. Wiederholen Sie die Schritte 9 und 10 für jede zusätzliche Aktion, die Sie zuweisen möchten.
12. Wenn alle entsprechenden Aktionen ausgewählt wurden, wählen Sie **zuweisen**aus.
13. Klicken Sie auf **Speichern** , um das neue Steuerelement zu speichern.

### <a name="export-a-template-to-json"></a>Exportieren einer Vorlage in JSON

Compliance-Manager (Preview) unterstützt auch das Exportieren von Vorlagen in JavaScript Object Notation (JSON)-Format. Auf diese Weise können Sie Compliance-Manager-Daten mit anderen Systemen, die JSON unterstützen, austauschen.

## <a name="reports"></a>Berichte

Sie können eine Bewertung in eine Excel-Datei für die Compliance-Verantwortlichen in Ihrer Organisation oder für externe Auditoren und Regulierer exportieren. Der Bericht ist eine Momentaufnahme der Bewertung zum Zeitpunkt des Exports. Der Bericht enthält die Details für Microsoft-und vom Kunden verwaltete Steuerelemente für die Bewertung, die Steuerung des Implementierungsstatus, das Kontrolldatum, Testergebnisse und Links zu hochgeladenen Beweisdokumenten. Sie sollten Bewertungen exportieren, bevor Sie Sie archivieren, da Archivierte Bewertungen keine Links zu hochgeladenen Dokumenten aufbewahren.

### <a name="export-an-assessment"></a>Exportieren einer Bewertung

1. Wählen Sie im Compliance-Manager-Dashboard die Registerkarte **Steuerelemente-Info** aus.
2. Wählen Sie die Gruppe und Bewertung in den Dropdownmenüs für die Bewertung aus, die Sie exportieren möchten.
3. Wählen Sie exportieren aus. Der Assessment-Export wird als Excel-Datei heruntergeladen.

![Compliance-Manager-Bewertung – Excel-Bericht](media/compliance-manager-assessment-report.png)

## <a name="permissions"></a>Berechtigungen

In der folgenden Tabelle werden die einzelnen Kompatibilitäts-Manager-Berechtigungen und deren Funktionsweise beschrieben. Die Tabelle gibt außerdem die Rolle an, die jeder Berechtigung zugewiesen ist.

||**Compliance Manager Reader**|**Compliance Manager Contributor**|**Compliance Manager Assessor**|**Compliance Manager Administrator**|**Portal Admin**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|**Daten lesen:** Benutzer können Daten lesen, aber nicht bearbeiten (mit Ausnahme von Vorlagendaten und MandantenVerwaltung).  <br> | X | X | X | X  | X |
|**Bearbeiten von Daten:** Benutzer können alle Felder, mit Ausnahme der Felder Testergebnis und Test Datum (mit Ausnahme von Vorlagendaten und MandantenVerwaltung) bearbeiten.  <br> || X | X  | X | X |
|**Bearbeiten von Testergebnissen:** Benutzer können die Felder Testergebnis und Test Datum bearbeiten.  <br> ||| X | X | X |
|**Verwalten von Bewertungen:** Benutzer können Bewertungen erstellen, archivieren und löschen.  <br> |||| X | X |
|**Verwalten von Masterdaten:** Benutzer können Vorlagendaten und Mandanten Verwaltungsdaten anzeigen, bearbeiten und löschen.  <br> |||| X | X |
|**Verwalten von Benutzern:** Benutzer können anderen Benutzern in Ihrer Organisation die Rollen Leser, mitWirkende, Assessor und Administrator hinzufügen. Nur Benutzer, die die Rolle des globalen Administrators in Ihrer Organisation haben, können Benutzer aus der Rolle des Portal Administrators hinzufügen oder daraus entfernen.  <br> ||||| X |

### <a name="guest-access"></a>Gastzugriff
  
Nachdem der Zugriff auf den Compliance-Manager konfiguriert wurde, ist jeder Benutzer, der über keine bereitgestellte Rolle **** verfügt, standardmäßig in der Gastzugriffs Rolle (Dies ist auch die Erfahrung von Konten, die nicht in der Organisation bereitgestellt werden). Gastzugriffs Benutzer haben nicht vollständigen Zugriff auf alle Compliance-Manager-Funktionen. Sie können keine Daten zur Konformitätsbewertung der Organisation anzeigen, können aber Compliance-Manager verwenden, um die Berichte zur Konformitätsbewertung von Microsoft und Dienst Vertrauens Dokumente anzuzeigen.