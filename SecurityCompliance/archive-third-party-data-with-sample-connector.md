---
title: Verwenden von Beispiel-Konnektoren zum Archivieren von drittanbieterdaten in Office 365 (Vorschau)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Administratoren können einen systemeigenen Connector einrichten, um drittanbieterdaten aus Datenquellen wie Facebook-Geschäfts Seiten, LinkedIn-Unternehmensseiten und Instant Bloomberg zu importieren. Auf diese Weise können Sie Daten von drittanbieterdaten Quellen in Office 365 archivieren, sodass Sie Compliance-Funktionen wie Legal Hold, Inhaltssuche und Aufbewahrungsrichtlinien verwenden können, um die Steuerung der drittanbieterdaten Ihrer Organisation zu verwalten.
ms.openlocfilehash: bca193753d0a63de867bdb11cfce3918c124f429
ms.sourcegitcommit: 63a10dc5ffa9d709fac437d3fc9e554b1bcd826f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2019
ms.locfileid: "33307952"
---
# <a name="use-sample-connectors-to-archive-third-party-data-in-office-365-preview"></a>Verwenden von Beispiel-Konnektoren zum Archivieren von drittanbieterdaten in Office 365 (Vorschau)

Das Beispiel-Konnektor-Feature zum Archivieren von drittanbieterdaten in Office 365 befindet sich in der Vorschau.

Verwenden Sie einen Beispiel-Konnektor im Security & Compliance Center in Office 365, um Daten aus drittanbieterdaten Quellen wie Facebook, LinkedIn, Twitter und Bloomberg zu importieren und zu archivieren. Nachdem Sie einen Beispiel-Konnektor eingerichtet und konfiguriert haben, stellt er eine Verbindung mit der Drittanbieter-Datenquelle her (geplant), konvertiert den Inhalt eines Elements in ein e-Mail-Nachrichtenformat und importiert diese Elemente dann in ein Postfach in Office 365.

Nachdem drittanbieterdaten importiert wurden, können Sie die Office 365-Compliance-Funktionen wie die Aufbewahrung von Rechtsstreitigkeiten, die Inhaltssuche, die in-situ-Archivierung, Überwachung, Überwachung und Office 365-Speicherrichtlinien auf die drittanbieterdaten anwenden. Wenn beispielsweise ein Postfach für die Aufbewahrung von Rechtsstreitigkeiten oder für die Zuweisung zu einer Beibehaltungsrichtlinie aktiviert wird, werden die drittanbieterdaten beibehalten. Sie können Daten von Drittanbietern mithilfe der Inhaltssuche durchsuchen oder einem depotverwalter in einem erweiterten eDiscovery-Fall zuordnen. Die Verwendung von Beispiel-Konnektoren zum Importieren und Archivieren von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien konform bleibt.

> [!NOTE]
> Derzeit stehen nur die Beispiel-Konnektor für Facebook-Business-Seiten für die Vorschau zur Verfügung. Weitere Beispiel-Konnektoren werden in Kürze verfügbar sein.


## <a name="prerequisites-for-setting-up-a-connector-for-facebook-business-pages"></a>VoraussetZungen für das Einrichten eines Connectors für Facebook-Geschäfts Seiten

Sie müssen die folgenden Voraussetzungen erfüllen, bevor Sie einen Beispiel-Konnektor im Security & Compliance Center einrichten und konfigurieren können, um Daten aus den Facebook-Geschäfts Seiten Ihrer Organisation zu importieren und zu archivieren. 

- Sie benötigen ein Facebook-Konto für die Geschäfts Seiten Ihrer Organisation (Sie müssen sich beim Einrichten des Connectors bei diesem Konto anmelden). Derzeit können Sie nur Daten von Facebook-Geschäfts Seiten archivieren; Sie können keine Daten aus einzelnen Facebook-Profilen archivieren.

- Ihre Organisation muss über ein gültiges Azure-Abonnement verfügen. Wenn Sie nicht über ein vorhandenes Azure-Abonnement verfügen, können Sie sich für eine der folgenden Optionen registrieren:

    - [Registrieren Sie sich für ein kostenloses 1-Jahres-Azure-Abonnement.](https://azure.microsoft.com/free) 

    - [Registrieren Sie sich für ein kostenpflichtiges Azure-Abonnement.](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > Das [﻿Kostenlose Azure Active Directory-Abonnement](use-your-free-azure-ad-subscription-in-office-365.md) , das in ihrem Office 365-Abonnement enthalten ist, unterstützt die Beispiel-Konnektoren im Security _AMP_ Compliance Center nicht.

- Ihre Organisation muss einwilligen, dass der Office 365-Import Dienst auf Postfachdaten in Ihrer Organisation zugreifen kann. Um dieser Anforderung zuzustimmen, wechseln Sie zu [dieser Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), melden Sie sich mit den Anmeldeinformationen eines globalen Office 365-Administrators an, und akzeptieren Sie die Anforderung.

- Der Benutzer, der den benutzerdefinierten Connector in der Security &-Konformität (in Schritt 7) einrichtet, muss der Post Fach Import-Export Rolle in Exchange Online zugewiesen sein. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. Sie können die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" in Exchange Online hinzufügen. Sie können auch eine neue Rollengruppe erstellen, die Rolle Post Fach Import-Export zuweisen und dann die entsprechenden Benutzer als Mitglieder hinzufügen. Weitere Informationen finden Sie unter [Erstellen](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) von Rollengruppen oder [Rollengruppen ändern](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) im Artikel "Verwalten von Rollengruppen in Exchange Online".

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a>Schritt 1: Herunterladen des vordefinierten Connector-App-Pakets von GitHub

Der erste Schritt besteht darin, den Quellcode für die vorinstallierte Facebook-Connector-APP herunterzuladen, die eine Facebook-API zum Herstellen einer Verbindung mit ihren Facebook-Geschäfts Seiten und zum Extrahieren von Facebook-Daten verwendet, damit Sie Sie in Office 365 importieren können.

1. Wechseln Sie zu [dieser GitHub-Website](https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases). 
2. Klicken Sie unter der aktuellen Version auf die Datei **SampleConnector. zip** .
3. Speichern Sie die ZIP-Datei an einem Speicherort auf dem lokalen Computer. Diese ZIP-Datei wird in Schritt 4 in Azure hochgeladen.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Schritt 2: Erstellen einer APP in Azure Active Directory

Der nächste Schritt besteht darin, eine neue app in Azure Active Directory (AAD) zu registrieren. Diese APP entspricht der Web-App-Ressource, die Sie in Schritt 4 für den Facebook-Connector implementieren. 

Schrittweise Anleitungen finden Sie unter [Erstellen einer APP in Azure Active Directory](deploy-facebook-connector.md#step-2-create-an-app-in-azure-active-directory).

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen), speichern Sie die folgenden Informationen in einer Textdatei. Die Werte für diese werden in späteren Schritten des Bereitstellungsprozesses verwendet.

- AAD-Anwendungs-ID
- AAD-Anwendungsschlüssel
- AAD-Anwendungs-URI
- Mandanten-ID

## <a name="step-3-create-an-azure-storage-account"></a>Schritt 3: Erstellen eines Azure-speicherkontos

Der Facebook-Connector, den Sie für Ihre Organisation bereitstellen, lädt die Elemente aus ihren Facebook-Geschäfts Seiten an den Azure-Speicherort hoch, den Sie in diesem Schritt erstellen. Nachdem Sie einen benutzerdefinierten Connector im Security & Compliance Center (in Schritt 7) erstellt haben, kopiert der Office 365-Import Dienst die Facebook-Daten vom Azure-Speicherort in ein Postfach in Office 365. Wie zuvor im Abschnitt [erforderliche Komponenten](#prerequisites-for-setting-up-a-connector-for-facebook-business-pages) erläutert, benötigen Sie ein gültiges Azure-Abonnement, um ein Azure-Speicherkonto zu erstellen.

Schrittweise Anleitungen finden Sie unter [Erstellen eines Azure-speicherkontos](deploy-facebook-connector.md#step-3-create-an-azure-storage-account).

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen) speichern Sie die Verbindungszeichenfolgen-URI, die generiert wird. Sie verwenden diese Zeichenfolge beim Erstellen einer Web-App-Ressource in Azure in Schritt 4.

## <a name="step-4-create-a-web-app-resource-in-azure"></a>Schritt 4: Erstellen einer Web-App-Ressource in Azure

Der nächste Schritt besteht darin, eine Web-App-Ressource in Azure für den Facebook-Connector zu erstellen. 

Schrittweise Anleitungen finden Sie unter [Create a New Web App Resource in Azure](deploy-facebook-connector.md#step-4-create-a-new-web-app-resource-in-azure).

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen), geben Sie die folgenden Informationen (die Sie nach dem Ausführen der vorherigen Schritte in eine Textdatei kopiert haben) beim Erstellen der Web App-Ressource an.

- APISecretKey – Sie erstellen diesen Schlüssel während des Abschlusses dieses Schritts; Sie wird in Schritt 7 verwendet.
- StorageAccountConnectionString – der Verbindungszeichenfolgen-URI, den Sie nach dem Erstellen des Azure-speicherkontos in Schritt 3 kopiert haben.
- mandantenKENNUNG – die Mandanten-ID Ihrer Office 365-Organisation, die Sie nach der Erstellung der Facebook-Connector-app in Azure Active Directory in Schritt 2 kopiert haben.

Darüber hinaus laden Sie die SampleConnector. zip-Datei (die Sie in Schritt 1 heruntergeladen haben) in diesem Schritt hoch, um den Quellcode für die Facebook Connector-App bereitzustellen.

Nachdem Sie diesen Schritt abgeschlossen haben, müssen Sie die APP-Dienst-URL kopieren ( https://fbconnector.azurewebsites.net)beispielsweise. Sie müssen dies zum Abschließen von Schritt 5, Schritt 6 und Schritt 7 verwenden.

## <a name="step-5-register-the-web-app-on-facebook"></a>Schritt 5: Registrieren der Web-App auf Facebook

Im nächsten Schritt erstellen und konfigurieren Sie eine neue APP auf Facebook. Der benutzerdefinierte Connector, den Sie in Schritt 7 erstellen, verwendet die Facebook-Web-App für die Interaktion mit der Facebook-API, um Daten aus den Facebook-Geschäfts Seiten Ihrer Organisation abzurufen.

Schrittweise Anleitungen finden Sie unter [Registrieren der Facebook-App](deploy-facebook-connector.md#step-5-register-the-facebook-app).

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen), speichern Sie die folgenden Informationen in einer Textdatei. Die Werte für diese werden zum Konfigurieren der Facebook-Connector-app in Schritt 6 verwendet.

- Facebook-Anwendungs-ID
- Geheime Facebook-Anwendung
- Facebook-webhooks überprüfen Token

## <a name="step-6-configure-the-facebook-connector-app"></a>Schritt 6: Konfigurieren der Facebook-Connector-App

Der nächste Schritt besteht darin, Konfigurationseinstellungen zur Facebook Connector-App hinzuzufügen, die Sie beim Erstellen der Azure Web App-Ressource in Schritt 4 hochgeladen haben. Gehen Sie dazu zur Homepage Ihrer Connector-APP, und konfigurieren Sie Sie.

Schrittweise Anleitungen finden Sie unter [Schritt 6: Konfigurieren der Connector-Web-App](deploy-facebook-connector.md#step-6-configure-the-connector-web-app).

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen), geben Sie die folgenden Informationen an (die Sie nach dem Ausführen der vorherigen Schritte in eine Textdatei kopiert haben):

- Facebook-Anwendungs-ID (abgerufen in Schritt 5)
- Geheimnis der Facebook-Anwendung (erhalten in Schritt 5)
- Facebook-webhooks überprüfen Token (erhalten in Schritt 5)
- Azure Active Directory-Anwendungs-ID (die in Schritt 2 abgerufene AAD-Anwendungs-ID)
- Azure Active Directory-Anwendungsschlüssel (der in Schritt 2 abgerufene AAD-Anwendungsschlüssel)
- Azure Active Directory-Anwendungs-URI (der in Schritt 2 abgerufene AAD-Anwendungs-URI, beispielsweisehttps://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>Schritt 7: Einrichten eines benutzerdefinierten Connectors im Security & Compliance Center

Der letzte Schritt besteht darin, den benutzerdefinierten Connector im Security & Compliance Center einzurichten, der Daten aus ihren Facebook-Geschäfts Seiten in ein angegebenes Postfach in Office 365 importiert. Nachdem Sie diesen Schritt erfolgreich abgeschlossen haben, beginnt der Office 365-Import Dienst mit dem Importieren von Daten aus ihren Facebook-Geschäfts Seiten in Office 365. 

Schrittweise Anleitungen finden Sie unter [Einrichten eines benutzerdefinierten Connectors im Security _AMP_ Compliance Center](deploy-facebook-connector.md#step-7-set-up-a-custom-connector-in-the-security--compliance-center). 

Während des Abschlusses dieses Schritts (indem Sie die Schritt-für-Schritt-Anweisungen befolgen), geben Sie die folgenden Informationen an (die Sie nach dem Ausführen der Schritte in eine Textdatei kopiert haben).

- Azure-App-Dienst-URL (in Schritt 4; Beispiel:https://fbconnector.azurewebsites.net)
- APISecretKey (die Sie in Schritt 4 erstellt haben)
