---
title: Verwenden eines Beispiel-Konnektors zum Archivieren von Twitter-Daten in Office 365 (Vorschau)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Administratoren können einen systemeigenen Connector einrichten, um Twitter-Daten in Office 365 zu importieren. Auf diese Weise können Sie Daten aus Drittanbieter-Datenquellen in Office 365 archivieren, sodass Sie Compliance-Features wie Legal Hold, Inhaltssuche und Aufbewahrungsrichtlinien verwenden können, um die Steuerung der drittanbieterdaten Ihrer Organisation zu verwalten.
ms.openlocfilehash: b53d882a66ba30a0c4c90389253689a9fe1fb457
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155617"
---
# <a name="use-a-sample-connector-to-archive-twitter-data-in-office-365-preview"></a>Verwenden eines Beispiel-Konnektors zum Archivieren von Twitter-Daten in Office 365 (Vorschau)

Das Feature "Sample Connector" zum Archivieren von Twitter-Daten in Office 365 befindet sich in der Vorschau.

Verwenden Sie einen Beispiel-Konnektor im Security & Compliance Center in Office 365, um Daten aus Twitter zu importieren und zu archivieren. Nachdem Sie einen Sample Connector eingerichtet und konfiguriert haben, stellt er eine Verbindung mit dem Twitter-Konto Ihrer Organisation her (planmäßig), konvertiert den Inhalt eines Elements in ein e-Mail-Nachrichtenformat und importiert diese Elemente dann in ein Postfach in Office 365.

Nachdem Sie Twitter-Daten importiert haben, können Sie Office 365 Compliance-Features wie Beweissicherungsverfahren, Inhaltssuche, in-situ-Archivierung, Überwachung, Überwachung und Office 365 Aufbewahrungsrichtlinien auf die im Postfach gespeicherten Daten anwenden. Sie können beispielsweise mithilfe der Inhaltssuche drittanbieterdaten durchsuchen oder Sie einer Depotbank in einem erweiterten eDiscovery-Fall zuordnen. Das Verwenden von Beispiel-Konnektoren zum Importieren und Archivieren von Twitter-Daten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien konform bleibt.

> [!NOTE]
> Derzeit stehen nur die Beispiel-Konnektoren für Twitter-und [Facebook-Geschäfts Seiten](archive-facebook-data-with-sample-connector.md) für die Vorschau zur Verfügung. Weitere Beispiel-Konnektoren werden in Kürze verfügbar sein.


## <a name="prerequisites-for-setting-up-a-connector-for-twitter"></a>Voraussetzungen für das Einrichten eines Connectors für Twitter

Sie müssen die folgenden Voraussetzungen erfüllen, bevor Sie einen Sample Connector im Security & Compliance Center einrichten und konfigurieren können, um Daten aus dem Twitter-Konto Ihrer Organisation zu importieren und zu archivieren. 

- Sie benötigen ein Twitter-Konto für Ihre Organisation; Sie müssen sich bei diesem Konto anmelden, wenn Sie den Connector einrichten.

- Ihre Organisation muss über ein gültiges Azure-Abonnement verfügen. Wenn Sie über kein vorhandenes Azure-Abonnement verfügen, können Sie sich für eine der folgenden Optionen registrieren:

    - [Registrieren Sie sich für ein kostenloses 1-Jahres-Azure-Abonnement](https://azure.microsoft.com/free) 

    - [Registrieren für ein Pay-as-you-go Azure-Abonnement](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > Das [﻿Kostenlose Azure Active Directory-Abonnement](use-your-free-azure-ad-subscription-in-office-365.md) , das in Ihrem Office 365-Abonnement enthalten ist, unterstützt die Beispiel-Konnektoren im Security & Compliance Center nicht.

- Ihre Organisation muss einwilligen, dass der Office 365 Import Dienst auf Postfachdaten in Ihrer Organisation zugreifen kann. Um dieser Anforderung zuzustimmen, gehen Sie zu [dieser Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), melden Sie sich mit den Anmeldeinformationen eines Office 365 globalen Administrators an, und nehmen Sie dann die Anforderung an.

- Der Benutzer, der den benutzerdefinierten Connector in der Security & Compliance (in Schritt 7) einrichtet, muss in Exchange Online über die Rolle "Post Fach Import-Export" verfügen. Diese Rolle ist in Exchange Online standardmäßig keiner Rollengruppe zugewiesen. Sie können die Rolle "Post Fach Import exportieren" der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzufügen. Sie können auch eine neue Rollengruppe erstellen, die Rolle "Post Fach Import Export" zuweisen und dann die entsprechenden Benutzer als Mitglieder hinzufügen. Weitere Informationen finden Sie im Abschnitt [Erstellen](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) von Rollengruppen oder [Ändern von Rollengruppen](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) im Artikel "Verwalten von Rollengruppen in Exchange Online".

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a>Schritt 1: Herunterladen des vorab erstellten Connector-App-Pakets von GitHub

Der erste Schritt besteht darin, den Quellcode für die Twitter Sample Connector-APP herunterzuladen, die eine Twitter-API verwendet, um eine Verbindung mit Ihrem Twitter-Konto herzustellen und Daten zu extrahieren, damit Sie Sie in Office 365 importieren können.

1. Wechseln Sie zu [dieser GitHub-Website](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases). 
2. Klicken Sie unter der letzten Version auf die Datei **SampleConnector. zip** .
3. Speichern Sie die ZIP-Datei an einem Speicherort auf Ihrem lokalen Computer. Sie laden diese ZIP-Datei in Schritt 4 in Azure hoch.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Schritt 2: Erstellen einer APP in Azure Active Directory

Der nächste Schritt besteht darin, eine neue app in Azure Active Directory (AAD) zu registrieren. Diese APP entspricht der Webanwendungs Ressource, die Sie in Schritt 4 für den Twitter-Connector implementieren werden. 

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 2: Erstellen einer APP in Azure Active Directory](deploy-twitter-connector.md#step-2-create-an-app-in-azure-active-directory).

Bei Abschluss dieses Schritts (indem Sie die schrittweisen Anleitungen ausführen) speichern Sie die folgenden Informationen in einer Textdatei. Die Werte für diese werden in späteren Schritten im Bereitstellungsprozess verwendet.

- Aad-Anwendungs-ID
- Aad-Anwendungs Geheimnis
- Aad-Anwendungs-URI
- Mandanten-ID

## <a name="step-3-create-an-azure-storage-account"></a>Schritt 3: Erstellen eines Azure-speicherkontos

Der Twitter-Konnektor, den Sie für Ihre Organisation bereitstellen, lädt die Elemente von Twitter an den Azure-Speicherort hoch, den Sie in diesem Schritt erstellen. Nachdem Sie einen benutzerdefinierten Connector im Security & Compliance Center (in Schritt 7) erstellt haben, kopiert der Office 365-Import Dienst die Twitter-Daten aus dem Azure-Speicherort in ein Postfach in Office 365. Wie zuvor im Abschnitt [voraus](#prerequisites-for-setting-up-a-connector-for-twitter) setzungen erläutert, benötigen Sie ein gültiges Azure-Abonnement, um ein Azure-Speicherkonto zu erstellen.

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 3: Erstellen eines Azure-speicherkontos](deploy-twitter-connector.md#step-3-create-an-azure-storage-account).

Während des Abschlusses dieses Schritts (mit den schrittweisen Anweisungen) speichern Sie den generierten Verbindungszeichenfolgen-URI. Sie verwenden diese Zeichenfolge beim Erstellen einer webapp-Ressource in Azure in Schritt 4.

## <a name="step-4-create-a-web-app-resource-in-azure"></a>Schritt 4: Erstellen einer webapp-Ressource in Azure

Der nächste Schritt besteht darin, eine Webanwendungs Ressource in Azure für den Twitter-Connector zu erstellen. 

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 4: Erstellen einer neuen webapp-Ressource in Azure](deploy-twitter-connector.md#step-4-create-a-new-web-app-resource-in-azure).

Während des Abschlusses dieses Schritts (mit den schrittweisen Anweisungen) geben Sie die folgenden Informationen (die Sie nach Abschluss der vorherigen Schritte in eine Textdatei kopiert haben) beim Erstellen der Ressource für die Webanwendung an.

- APISecretKey – Sie werden diesen Schlüssel während des Abschlusses dieses Schritts erstellen; Sie wird in Schritt 7 verwendet.
- StorageAccountConnectionString – der Verbindungszeichenfolgen-URI, den Sie nach dem Erstellen des Azure-speicherkontos in Schritt 3 kopiert haben.
- Mandantenkennung – die Mandanten-ID Ihrer Office 365 Organisation, die Sie nach dem Erstellen der Twitter Connector-app in Azure Active Directory in Schritt 2 kopiert haben.

Darüber hinaus laden Sie die SampleConnector. zip-Datei (die Sie in Schritt 1 heruntergeladen haben) in diesem Schritt hoch, um den Quellcode für die Twitter Connector-App bereitzustellen.

Nachdem Sie diesen Schritt abgeschlossen haben, müssen Sie die Azure-App-Dienst-URL kopieren https://twitterconnector.azurewebsites.net)(beispielsweise. Sie müssen dies verwenden, um Schritt 5, Schritt 6 und Schritt 7 abzuschließen.

## <a name="step-5-create-developer-app-on-twitter"></a>Schritt 5: Erstellen der Entwickler-App auf Twitter

Der nächste Schritt besteht darin, eine Entwickler-App auf Twitter zu erstellen und zu konfigurieren. Der benutzerdefinierte Connector, den Sie in Schritt 7 erstellen, verwendet die Twitter-APP für die Interaktion mit der Twitter-API, um Daten aus dem Twitter-Konto Ihrer Organisation zu erhalten.

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 5: Erstellen der Twitter-APP](deploy-twitter-connector.md#step-5-create-the-twitter-app).

Bei Abschluss dieses Schritts (indem Sie die schrittweisen Anleitungen ausführen) speichern Sie die folgenden Informationen in einer Textdatei. Die Werte für diese werden verwendet, um die Twitter Connector-app in Schritt 6 zu konfigurieren.

- Twitter-Anwendungs-ID
- Twitter Application Secret (API-geheimer Schlüssel)
- Twitter-Clienttoken
- Geheimer Twitter-Client-Token

## <a name="step-6-configure-the-twitter-connector-app"></a>Schritt 6: Konfigurieren der Twitter Connector-App

Im nächsten Schritt fügen Sie der Twitter Connector-App Konfigurationseinstellungen hinzu, die Sie beim Erstellen der Azure-Webanwendung-Ressource in Schritt 4 hochgeladen haben. Gehen Sie dazu auf die Startseite Ihrer Connector-APP, und konfigurieren Sie Sie.

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 6: Konfigurieren der Connector-Webanwendung](deploy-twitter-connector.md#step-6-configure-the-connector-web-app).

Während des Abschlusses dieses Schritts (indem Sie die schrittweisen Anweisungen befolgen) geben Sie die folgenden Informationen an (die Sie nach Abschluss der vorherigen Schritte in eine Textdatei kopiert haben):

- Twitter Application ID (abgerufen in Schritt 5)
- Geheimer Twitter-Anwendungsschlüssel (in Schritt 5 abgerufen)
- Twitter-Clienttoken (in Schritt 5 abgerufen)
- Geheimer Twitter-Client-Tokenschlüssel (in Schritt 5 abgerufen)
- Azure Active Directory Application ID (die Aad-Anwendungs-ID, die in Schritt 2 abgerufen wurde)
- Azure Active Directory Application Secret (der in Schritt 2 abgerufene Aad-Anwendungsschlüssel)
- Azure Active Directory Application URI (der in Schritt 2 abgerufene Aad-Anwendungs-URI, beispielsweisehttps://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>Schritt 7: Einrichten eines benutzerdefinierten Connectors im Security & Compliance Center

Der letzte Schritt besteht darin, den benutzerdefinierten Connector im Security & Compliance Center einzurichten, mit dem Daten aus dem Twitter-Konto Ihrer Organisation in ein angegebenes Postfach in Office 365 importiert werden. Nachdem Sie diesen Schritt erfolgreich abgeschlossen haben, startet der Office 365 Import-Dienst den Prozess des Importierens von Daten aus Twitter in Office 365. 

Eine Schritt-für-Schritt-Anleitung finden Sie unter [Schritt 7: Einrichten eines benutzerdefinierten Connectors im Security and Compliance Center](deploy-twitter-connector.md#step-7-set-up-a-custom-connector-in-the-security-and-compliance-center). 

Während des Abschlusses dieses Schritts (indem Sie die schrittweisen Anweisungen befolgen) geben Sie die folgenden Informationen an (die Sie nach Abschluss der Schritte in eine Textdatei kopiert haben).

- Azure-App-Dienst-URL (abgerufen in Schritt 4; zum Beispielhttps://twitterconnector.azurewebsites.net)
- APISecretKey (das Sie in Schritt 4 erstellt haben)
