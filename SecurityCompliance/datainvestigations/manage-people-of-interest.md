---
title: Verwalten von Personen, die Interesse an Daten Untersuchungen haben (Vorschau)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d06dde60ae75cfea1bf1d79f445b613d20a76363
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257673"
---
# <a name="manage-people-of-interest-in-data-investigations-preview"></a>Verwalten von Personen, die Interesse an Daten Untersuchungen haben (Vorschau)

Daten Untersuchungen beziehen sich häufig auf Personen von Interesse. In der Regel handelt es sich um Personen, die die verlegten, vertraulichen oder bösartigen Daten besitzen, die Sie untersuchen oder zur Korrektur suchen. In **Daten Untersuchungen (Preview)** können Sie Sie hinzufügen, um Ihre Datenquellen zu ermitteln, die Sie bei der Suche verwenden, oder um zusätzliche Informationen wie Kontakt, Speicherort und Aktivitätsprotokolle anzuzeigen. 


## <a name="add-people-of-interest"></a>Hinzufügen von Personen von Interesse

Auf der Registerkarte **Personen von Interesse** können Sie interessante Personen hinzufügen und Ihre Datenquellen wie Exchange-Postfächer oder OneDrive for Business-Website ermitteln, die Sie zum Bereich der Suche verwenden können. Wenn Personen von Interesse sind, sind Suchvorgänge leistungsfähiger und präziser, da das Tool alle nicht indizierten Daten wie Bilder oder nicht unterstützte Dateitypen erneut verarbeitet. Sie können auch Ihre Kontaktinformationen, Standortinformationen und Aktivitätsprotokolle anzeigen, die Sie zum Initiieren der Kommunikation oder zur weiteren Untersuchung ihrer Aktivitäten verwenden können. 

Hinzufügen von Personen, die für eine Untersuchung von Interesse sind:

1. Gehen Sie auf der Seite **Daten Untersuchungen (Preview)** zu ihrer Untersuchung.
 
2. Nachdem Sie eine Untersuchung ausgewählt haben, wechseln Sie zur Registerkarte **Personen von Interesse** , und klicken Sie auf **+ interessante Personen hinzufügen**. 
 
3. Wählen Sie Personen aus, die Sie der Untersuchung hinzufügen möchten. Sie können zunächst eingeben, um die Benutzer aus Azure Active Directory Ihrer Organisation zu suchen und auszuwählen.
 
4. Nachdem Sie die Liste der Personen mit Interesse abgeschlossen haben, klicken Sie auf **weiter** , um Ihre Datenquellen zuzuordnen. 

5. Optional Wählen Sie für jede Person **Exchange** aus, um das primäre Exchange-Postfach der Person hinzuzufügen, und **OneDrive** , um die primäre OneDrive für Business-Website der Person hinzuzufügen.

6. Optional Klicken Sie auf **weiter** , um zusätzliche Datenquellen hinzuzufügen, die Sie Ihren Interessen Personen zuordnen möchten.

7. Optional Wählen Sie **Aktualisieren** aus, um einer Person inhaltsspeicherorte wie Postfächer, Websites und Teams zuzuweisen. 

8. Optional Im Flyout:
   
    -  **Exchange-Postfächer** – klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** . Um weitere Postfächer hinzuzufügen, verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen. Sie können auch Postfächer hinzufügen, die zum Speichern einer Office 365-Gruppe oder einer Microsoft Team-Information verwendet werden. Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.

        > [!NOTE]
        > Wenn Sie auf Benutzer, Gruppen oder Teams zum Angeben von Postfächern klicken, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein.
     
     - **SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um zusätzliche SharePoint-und OneDrive für Business-Websites anzugeben, die Sie einer Person hinzufügen wwant. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen. Geben Sie die URL für jede Website ein, die Sie zuweisen möchten. Klicken Sie auf **auswählen**und dann auf **Fertig**.
     - **Microsoft Teams** – klicken Sie auf **Teams auswählen** , und klicken Sie dann erneut auf **Teams auswählen** , um eine Liste der Microsoft-Team Gruppen anzuzeigen, von denen die Person heute Mitglied ist. Wählen Sie die Teams aus, die Sie der Person hinzufügen möchten. Nach der Auswahl identifiziert das System automatisch & wählen Sie die zugeordnete SharePoint-Website und das Gruppenpostfach aus, die diesem Microsoft-Team zugeordnet sind. Klicken Sie auf **auswählen**und dann auf **Fertig**.
        
      > [!NOTE]
      > Um zusätzliche Microsoft Teams hinzuzufügen, müssen Sie das Postfach und die SharePoint-Website, wie oben dargestellt, separat hinzufügen.

Nachdem Sie die Zuordnung von Datenquellen zu Personen mit Interesse abgeschlossen haben, können Sie die Zusammenfassung aller soeben hinzugefügten Postfächer, Websites und Teams anzeigen. Wenn Sie weitere Datenquellen zu Personen von Interesse und Umfang Ihrer Suche nach Personen von Interesse zuordnen, wird die Zuordnung von Dokumenten zu Personen von Interesse während der gesamten Untersuchung beibehalten, wodurch es einfacher ist, Nachweise zu organisieren oder einen Bericht von Personen von Interesse zu generieren. . 

## <a name="view-additional-people-of-interest-information"></a>Anzeigen zusätzlicher Informationen zu Personen mit Interesse

Klicken Sie auf **der** Registerkarte Interessenten auf eine Person, die Sie adeed. In einem Flyout sehen Sie Folgendes:

- Kontaktinformationen

  - **Anzeigename**: der Name des Perons, der im Adressbuch angezeigt wird. Dies ist normalerweise die Kombination aus Vornamen, mittlerem Anfangs-und Nachname.
  - **Mail/SMTP**: die SMTP-Adresse der Person, beispielsweise Jeff@contoso.onmicrosoft.com.  
  - **Title**: Job Title.
  - **Abteilung**: der Name der Abteilung, in der die Person arbeitet.
  - **Manager**: der Vorgesetzte der Person. Der Vorgesetzte erhält eine Eskalations Kommunikation für diese Person.
  
- Standortinformationen

  - **Ort**: die Stadt, in der sich die Person befindet.
  - **Status**: der Bundesstaat oder Kanton, in dem sich die Person befindet.
  - **Land/Region**: das Land/die Region, in der sich die Person befindet; zum Beispiel "US" oder "UK".
  - **Office**: der Bürostandort der Person.

- Verarbeitungsstatus

  - **Indizierungsstatus**: Status der Deep-Indizierung der Datenquellen
  - **IndexIng Last updated Time**: timestamp of when the Deep Indexed Job zuletzt ausgelöst wurde.
  - **Datenquellen**: zeigt die Anzahl von Postfächern, Websites und Teams an, die der Person zugeordnet sind.

- Index aktualisieren
    - Sie können die Datenquellen dieser Person erneut indizieren. 

- Aktivität anzeigen 

    - Sie können die Aktivitätsprotokolle der Benutzer anzeigen und durchsuchen. Weitere Informationen finden Sie unter [Anzeigen von](view-people-of-interest-activity.md) Interessenten Aktivitäten. 
