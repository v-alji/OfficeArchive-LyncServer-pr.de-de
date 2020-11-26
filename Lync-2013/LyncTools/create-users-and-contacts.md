---
title: Erstellen von Benutzern und Kontakten
description: Erstellen von Benutzern und Kontakten
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Create Users and Contacts
ms:assetid: 04b24d07-2864-463d-b508-544c2674c4ab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945587(v=OCS.15)
ms:contentKeyID: 51541412
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e45bb1aa737dd8287be15ae72ece2e35a346af1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446523"
---
# <a name="create-users-and-contacts"></a><span data-ttu-id="b0f61-103">Erstellen von Benutzern und Kontakten</span><span class="sxs-lookup"><span data-stu-id="b0f61-103">Create Users and Contacts</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0f61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0f61-104">

<span> </span></span></span>

<span data-ttu-id="b0f61-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="b0f61-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="b0f61-106">Sie müssen das lync Server 2013-Benutzer Bereitstellungs Tool (UserProvisioningTool.exe) verwenden, um Benutzer und Kontakte in Vorbereitung auf Stress-und Leistungs Auslastungstests zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-106">You must use the Lync Server 2013 User Provisioning Tool (UserProvisioningTool.exe) to create users and contacts in preparation for stress and performance load testing.</span></span>

<span data-ttu-id="b0f61-107">Nachfolgend finden Sie eine Liste der Begriffe und Definitionen, die Ihnen bei der Lektüre dieses Themas nützlich sein können.</span><span class="sxs-lookup"><span data-stu-id="b0f61-107">Here is a list of terms and definitions that you might find useful as you read through this topic.</span></span>

  - <span data-ttu-id="b0f61-108">Organisationseinheit – die Organisationseinheit für Active Directory-Domänendienste.</span><span class="sxs-lookup"><span data-stu-id="b0f61-108">Organizational Unit – The Active Directory Domain Services organizational unit (OU).</span></span>

  - <span data-ttu-id="b0f61-109">Federated/Cross-Pool – Benutzer, die für die Kommunikation mit Benutzern aus anderen Instant Messaging-Diensten (im) wie MSN-Netzwerk von Internet Diensten, AOL® und Yahoo- \! ® aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-109">Federated / Cross Pool – Users who will be enabled to communicate with users from other Instant Messaging (IM) services, such as MSN network of Internet services, AOL®, and Yahoo\!®.</span></span>

  - <span data-ttu-id="b0f61-110">Verteilerlisten – die Objekte in den Active Directory-Domänendiensten, die eine Liste der Benutzer von Active Directory-Domänendiensten enthalten, die zum Starten von Kommunikation mit Personengruppen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-110">Distribution Lists – The objects in Active Directory Domain Services that contain a list of Active Directory Domain Services users, used for launching communications with groups of people.</span></span>

  - <span data-ttu-id="b0f61-111">Location Info Service – der lync Server 2013-Dienst, der bei aktivierter und konfigurierter Telefonfunktion das Abrufen des physikalischen Standorts für verbesserte 9-1-1 (E9-1-1)-Dienste ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b0f61-111">Location Info Service – The Lync Server 2013 service that, when enabled and configured per phone, enables retrieval of physical location for Enhanced 9-1-1 (E9-1-1) services.</span></span>

  - <span data-ttu-id="b0f61-112">US-Telefonnummern – die den Benutzern zugewiesenen Telefonnummern, zusätzlich zu dem SIP-URI, der für das Routing von eingehenden und ausgehenden Anrufen sowie für Reverse Number Lookup (RNL) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0f61-112">U.S. Phone Numbers – The phone numbers that are assigned to users, in addition to the SIP URI that is used for routing inbound and outbound calls and reverse number lookup (RNL).</span></span>

<div>

## <a name="create-users-and-contacts-by-using-userprovisioningtoolexe"></a><span data-ttu-id="b0f61-113">Erstellen von Benutzern und Kontakten mithilfe von UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="b0f61-113">Create Users and Contacts by Using UserProvisioningTool.exe</span></span>

<span data-ttu-id="b0f61-114">Sie müssen das lync Server-Benutzer Bereitstellungs Tool verwenden, um Benutzer und Kontakte für die Auslastungssimulation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-114">You must use the Lync Server User Provisioning Tool to create users and contacts for load simulation.</span></span> <span data-ttu-id="b0f61-115">Das lync Server-Bereitstellungstool für Benutzer wird mit dem lync Server Stress and Performance Tool-Paket installiert.</span><span class="sxs-lookup"><span data-stu-id="b0f61-115">The Lync Server User Provisioning Tool is installed with the Lync Server Stress and Performance Tool package.</span></span> <span data-ttu-id="b0f61-116">Stellen Sie sicher, dass das Paketinstallationsprogramm (CapacityPlanningTool.msi) auf dem Front-End-Server oder dem Standard Edition-Server ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0f61-116">Be sure that the package installer (CapacityPlanningTool.msi) has been run on the Front End Server or the Standard Edition server.</span></span> <span data-ttu-id="b0f61-117">Starten Sie das lync Server-Benutzer Bereitstellungs Tool, indem Sie die Datei UserProvisioningTool.exe (befindet sich unter% InstalledDirectory% LyncStressAndPerfTool \\ LyncStress) auf dem Front-End-Server oder auf dem Standard Edition-Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-117">Start the Lync Server User Provisioning Tool by running the file UserProvisioningTool.exe (located at %InstalledDirectory%LyncStressAndPerfTool\\LyncStress) on the Front End Server or on the Standard Edition server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b0f61-118">Sie müssen als Mitglied der Sicherheitsgruppe "Domänen-Admins" angemeldet sein, um UserProvisioningTool.exe ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="b0f61-118">You must be logged on as a member of the Domain Admins security group in order to run UserProvisioningTool.exe.</span></span> <span data-ttu-id="b0f61-119">Sie müssen in diesem Kontext ausgeführt werden, da UserProvisioningTool.exe neue Active Directory-Domänendienste-Benutzer erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-119">It is necessary to run from this context because UserProvisioningTool.exe will be creating and configuring new Active Directory Domain Services users.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b0f61-120">Wenn Sie eine große Anzahl von Benutzern (10.000 oder mehr) erstellen, führen Sie UserProvisioningTool.exe von einem Highend-Computer aus.</span><span class="sxs-lookup"><span data-stu-id="b0f61-120">When you create a significant number of users (10,000 or more), run UserProvisioningTool.exe from a high-end computer.</span></span> <span data-ttu-id="b0f61-121">Beachten Sie, dass der Domänencontroller auch eine hohe Auslastung aufweisen wird, während die Benutzer erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-121">Note that the domain controller will also experience high load while the users are being created.</span></span>



</div>

<span data-ttu-id="b0f61-122">Wenn das lync Server-Benutzer Bereitstellungs Tool geöffnet wird, klicken Sie auf **Konfiguration** , und wählen Sie **Konfiguration laden** aus.</span><span class="sxs-lookup"><span data-stu-id="b0f61-122">When the Lync Server User Provisioning Tool opens, click **Configuration** and select **Load Configuration**.</span></span> <span data-ttu-id="b0f61-123">Wenn Sie mit der Konfiguration von Benutzern und Kontakten beginnen möchten, laden Sie die im Paket enthaltene Standarddatei SampleData.xml.</span><span class="sxs-lookup"><span data-stu-id="b0f61-123">To begin configuring users and contacts, load the default file that is included in the package, SampleData.xml.</span></span> <span data-ttu-id="b0f61-124">Dadurch werden die Felder mit Beispieldaten vorab gefüllt, die Sie für Ihr System überarbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-124">This will prepopulate the fields with example data that you'll need to revise for your system.</span></span> <span data-ttu-id="b0f61-125">Wenn Sie über eine vorkonfigurierte XML-Datei verfügen, die bereits angepasste Einstellungen enthält, laden Sie stattdessen die Datei.</span><span class="sxs-lookup"><span data-stu-id="b0f61-125">If you have a preconfigured XML file that already contains customized settings, load that file instead.</span></span> <span data-ttu-id="b0f61-126">Füllen Sie die Felder im lync Server-Benutzer Bereitstellungs Tool aus, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0f61-126">Fill in the fields in the Lync Server User Provisioning Tool, as described in the following sections.</span></span>

<span data-ttu-id="b0f61-127">![Registerkarte "Benutzererstellung"](images/JJ945587.80d3c17b-7482-4818-8381-1eff8717d2fe(OCS.15).jpg "Registerkarte "Benutzererstellung"")</span><span class="sxs-lookup"><span data-stu-id="b0f61-127">![User Creation tab.](images/JJ945587.80d3c17b-7482-4818-8381-1eff8717d2fe(OCS.15).jpg "User Creation tab.")</span></span>

<span data-ttu-id="b0f61-128">Führen Sie die folgenden Schritte aus, um Serveroptionen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-128">To configure server options, follow these steps.</span></span>

1.  <span data-ttu-id="b0f61-129">Geben Sie im **Front-End-Pool-FQDN** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Standard Edition-Servers oder-Front-End-Pools ein, in dem Sie die Benutzer hosten möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-129">In **Front End Pool FQDN**, type the fully qualified domain name (FQDN) of the Standard Edition server or Front End pool where you want to host the users.</span></span>

2.  <span data-ttu-id="b0f61-130">Geben Sie unter **Benutzer Name-Präfix** ein Präfix ein, das Sie zum Erstellen von Benutzernamen für Testzwecke verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-130">In **User Name Prefix**, type a prefix that you want to use to build user names for testing purposes.</span></span>

3.  <span data-ttu-id="b0f61-131">Geben Sie im Feld **Kennwort** ein Kennwort ein, das für alle Testbenutzerkonten angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f61-131">In **Password**, specify a password that will be applied for all of the test user accounts.</span></span>

4.  <span data-ttu-id="b0f61-132">Geben Sie in **SIP-Domäne** den Domänennamen ein, der für die SIP-URIs von Testbenutzern verwendet werden soll (Uniform Resource Identifiers).</span><span class="sxs-lookup"><span data-stu-id="b0f61-132">In **SIP Domain**, type the domain name to be used for test users’ SIP URIs (Uniform Resource Identifiers).</span></span>

5.  <span data-ttu-id="b0f61-133">Geben Sie in **Kontodomäne** den Domänennamen Ihrer aktuellen Active Directory-Domänendienst Domäne ein, unter der Sie die Testbenutzer erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-133">In **Account Domain**, type the domain name of your current Active Directory Domain Services domain, under which you want to create the test users.</span></span>

6.  <span data-ttu-id="b0f61-134">Geben Sie in **Organisationseinheit** den Namen der Active Directory-Domänendienste-ou ein, in der Sie die Benutzerobjekte erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-134">In **Organizational Unit**, type the name of the Active Directory Domain Services OU where you want to create the User objects.</span></span> <span data-ttu-id="b0f61-135">Wenn die Organisationseinheit nicht vorhanden ist, wird Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-135">If the OU does not exist, it will be created.</span></span>

7.  <span data-ttu-id="b0f61-136">Geben Sie in **Telefonvorwahl** die dreistellige Vorwahl ein, die für Testbenutzerkonten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0f61-136">In **Phone Area Code**, type the three-digit area code that will be used for test user accounts.</span></span> <span data-ttu-id="b0f61-137">Stellen Sie sicher, dass die Telefonvorwahl keinen Konflikt mit den Ortsnummern anderer Benutzer in den Active Directory-Domänendiensten verursacht.</span><span class="sxs-lookup"><span data-stu-id="b0f61-137">Be sure that phone area code does not conflict with any other users’ area codes in Active Directory Domain Services.</span></span>

8.  <span data-ttu-id="b0f61-138">Aktivieren Sie das Kontrollkästchen **sprachaktiviert** , wenn Sie die Testbenutzer für Enterprise-VoIP aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-138">Select the **Voice Enabled** check box if you want to enable the test users for Enterprise Voice.</span></span>

9.  <span data-ttu-id="b0f61-139">Geben Sie unter **Anzahl der Benutzer** die Gesamtzahl der Testbenutzer an, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-139">In **Number of Users**, specify the total number of test users that you want to create.</span></span>

10. <span data-ttu-id="b0f61-140">Geben Sie im **Start Index** die Anfangsnummer an, die als Suffix für das Benutzernamenpräfix verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0f61-140">In **Start Index**, specify the starting number that will be used as suffix to the user name prefix.</span></span>

<div>

## <a name="create-users-button"></a><span data-ttu-id="b0f61-141">Schaltfläche "Benutzer erstellen"</span><span class="sxs-lookup"><span data-stu-id="b0f61-141">Create Users Button</span></span>

<span data-ttu-id="b0f61-142">Wenn Sie auf die Schaltfläche Benutzer erstellen klicken, werden alle Eingabeparameter überprüft.</span><span class="sxs-lookup"><span data-stu-id="b0f61-142">When you click on the Create Users button, it will validate all the input parameters.</span></span>

  - <span data-ttu-id="b0f61-143">Wenn es Validierungsfehler gibt, werden Sie aufgefordert, diese Eingabewerte zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-143">If there are any validation errors, it will prompt you to correct those input values.</span></span>

  - <span data-ttu-id="b0f61-144">Wenn alle Eingabewerte richtig sind, wird das Erstellen von Benutzern in den Active Directory-Domänendiensten gestartet.</span><span class="sxs-lookup"><span data-stu-id="b0f61-144">If all the input values are correct, it will start creating users in Active Directory Domain Services.</span></span> <span data-ttu-id="b0f61-145">Am Ende dieses Formulars wird eine Statusleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-145">A progress bar will appear at the bottom of this form.</span></span> <span data-ttu-id="b0f61-146">Wir empfehlen, dass Sie die Anwendung nicht schließen, während die Statusleiste aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="b0f61-146">We recommend that you do not close the application while the progress bar is active.</span></span>

<span data-ttu-id="b0f61-147">Die Benutzererstellung ist ein langsamer Prozess.</span><span class="sxs-lookup"><span data-stu-id="b0f61-147">User Creation is a slow process.</span></span> <span data-ttu-id="b0f61-148">Es kann mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="b0f61-148">It can take several minutes.</span></span> <span data-ttu-id="b0f61-149">Wenn die Anzahl der Benutzer sehr groß ist, kann der Vorgang sogar einige Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="b0f61-149">If the number of users is very large, the process could even take a few hours.</span></span> <span data-ttu-id="b0f61-150">Wenn die Benutzer bereits vorhanden sind, werden Sie mit allen Änderungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b0f61-150">If the users already exist, they are updated with any changes.</span></span> <span data-ttu-id="b0f61-151">Sie können überprüfen, ob die Benutzer erstellt wurden, indem Sie sich als einer der Benutzer im Bereich anmelden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-151">You can validate that the users were created by logging on as one of the users in the range.</span></span> <span data-ttu-id="b0f61-152">Verwenden Sie das Benutzerpräfix, die Benutzernummer und @sipDomain als Benutzernamen (beispielsweise LyncUser10@contoso.net) zusammen mit dem angegebenen Kennwort.</span><span class="sxs-lookup"><span data-stu-id="b0f61-152">Use the user prefix, user number, and @sipDomain as the user name (for example, LyncUser10@contoso.net), along with the specified password.</span></span>

</div>

<div>

## <a name="delete-users-button"></a><span data-ttu-id="b0f61-153">Schaltfläche "Benutzer löschen"</span><span class="sxs-lookup"><span data-stu-id="b0f61-153">Delete Users Button</span></span>

<span data-ttu-id="b0f61-154">Wenn Sie auf die Schaltfläche Benutzer löschen klicken, werden alle Eingabeparameter überprüft.</span><span class="sxs-lookup"><span data-stu-id="b0f61-154">When you click on Delete Users button, it will validate all the input parameters.</span></span>

  - <span data-ttu-id="b0f61-155">Wenn es Validierungsfehler gibt, werden Sie aufgefordert, diese Eingabewerte zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-155">If there are any validation errors, it will prompt you to correct those input values.</span></span>

  - <span data-ttu-id="b0f61-156">Wenn alle Eingabewerte richtig sind, wird das Deaktivieren und Löschen von Benutzern in den Active Directory-Domänendiensten gestartet.</span><span class="sxs-lookup"><span data-stu-id="b0f61-156">If all the input values are correct, it will start disabling and deleting users in Active Directory Domain Services.</span></span> <span data-ttu-id="b0f61-157">Am Ende dieses Formulars wird eine Statusleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-157">A progress bar will appear at the bottom of this form.</span></span> <span data-ttu-id="b0f61-158">Wir empfehlen, dass Sie die Anwendung nicht schließen, während die Statusleiste aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="b0f61-158">We recommend that you do not close the application while the progress bar is active.</span></span>

<div>


> [!NOTE]  
> <OL>
> <LI>
> <P><span data-ttu-id="b0f61-159">Nur US-formatierte Telefonnummern werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-159">Only U.S.-formatted phone numbers are supported.</span></span> <span data-ttu-id="b0f61-160">Telefonnummern werden immer Benutzern zugewiesen, und alle von UserProvisioningTool.exe erstellten Benutzer sind für Enterprise-VoIP aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b0f61-160">Phone numbers are always assigned to users, and all users created by UserProvisioningTool.exe are enabled for Enterprise Voice.</span></span> <span data-ttu-id="b0f61-161">In Szenarien, in denen die Telefonnummer verwendet wird, beispielsweise die automatische Telefonzentrale oder UC-PSTN-Anrufe, verwenden Sie diese Telefonnummer, um Anrufe richtig weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-161">Any scenarios that use the phone number, such as Conferencing Auto Attendant or UC-PSTN calls, use this phone number to properly route calls.</span></span> <span data-ttu-id="b0f61-162">Aus diesem Grund muss jeder Nutzer eine eindeutige Telefonnummer haben.</span><span class="sxs-lookup"><span data-stu-id="b0f61-162">For this reason, every user must have a unique phone number.</span></span> <span data-ttu-id="b0f61-163">Wenn Sie Benutzer zweimal erstellen müssen, schlägt der Befehl fehl, es sei denn, Sie verwenden eine andere Ortsvorwahl, oder wenn die vorherigen Benutzer mithilfe des Cmdlets <STRONG>Disable-CsUser</STRONG> deaktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-163">If you have to create users twice, the command will fail unless you use a different area code, or if the previous users have been disabled by using the <STRONG>Disable-CsUser</STRONG> cmdlet.</span></span></P>
> <LI>
> <P><span data-ttu-id="b0f61-164">Bevor Sie Kontakte erstellen, müssen Sie zuerst die Benutzerreplikation durchführen, die auf der Registerkarte Benutzer ausgeführt wird. Wenn Sie soeben Ihre Benutzer erstellt haben, müssen Sie warten, bis die lync Server-Replikation abgeschlossen ist, und die Benutzerkonten in der Datenbank werden gefüllt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-164">Before you create contacts, you must first complete user replication, performed from the Users tab. If you have just created your users, you must wait until Lync Server replication completes and populates the user accounts in the database.</span></span> <span data-ttu-id="b0f61-165">Wenn die Replizierung der Benutzer noch nicht erfolgt ist, wird ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-165">If the users have not finished replicating, you will see an error.</span></span> <span data-ttu-id="b0f61-166">Sie wissen, wann die Replikation der Benutzer abgeschlossen ist, wenn der lync Server 2013-Front-End-Dienst gestartet wurde, oder dass Sie das Cmdlet " <STRONG>Get-CsUser</STRONG> " für den letzten Benutzer erfolgreich ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="b0f61-166">You will know when users have finished replicating if Lync Server 2013 Front End service has started, or by successfully running the <STRONG>Get-CsUser</STRONG> cmdlet on the last user.</span></span></P></LI></OL>



</div>

</div>

</div>

<div>

## <a name="contacts-creation-tab"></a><span data-ttu-id="b0f61-167">Registerkarte "Kontakte erstellen"</span><span class="sxs-lookup"><span data-stu-id="b0f61-167">Contacts Creation Tab</span></span>

<span data-ttu-id="b0f61-168">Auf der Registerkarte "Kontakte erstellen" können Sie Details zu den Kontakten der Benutzer angeben.</span><span class="sxs-lookup"><span data-stu-id="b0f61-168">The Contacts Creation tab enables you to specify details for users’ contacts.</span></span>

<span data-ttu-id="b0f61-169">![Registerkarte "Kontakte erstellen"](images/JJ945587.7508726e-83e6-4878-8edd-114543d9af24(OCS.15).jpg "Registerkarte "Kontakte erstellen"")</span><span class="sxs-lookup"><span data-stu-id="b0f61-169">![Contacts Creation tab.](images/JJ945587.7508726e-83e6-4878-8edd-114543d9af24(OCS.15).jpg "Contacts Creation tab.")</span></span>

<span data-ttu-id="b0f61-170">Führen Sie die folgenden Schritte aus, um die Kontakte der Benutzer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-170">To configure users’ contacts, follow these steps.</span></span>

1.  <span data-ttu-id="b0f61-171">Geben Sie in durchschnittliche Kontakte pro Benutzer die durchschnittliche Anzahl der Kontakte an, die in Kontaktlisten für die einzelnen Benutzer aufgefüllt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-171">In Average Contacts per User, specify the average number of contacts to populate in contact lists for each of the users.</span></span>

2.  <span data-ttu-id="b0f61-172">Aktivieren Sie das Kontrollkästchen behoben, wenn Sie eine gleiche Anzahl von Kontakten für jeden Benutzer erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-172">Select the Fixed check box if you want to create an equal number of contacts for every user.</span></span> <span data-ttu-id="b0f61-173">Wenn Sie die Anzahl der für Benutzer erstellten Kontakte variieren möchten, deaktivieren Sie das Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-173">If you want to vary the number of contacts created for users, clear the check box.</span></span>

3.  <span data-ttu-id="b0f61-174">Geben Sie in durchschnittliche Kontaktgruppen pro Benutzer die Anzahl der Kontaktgruppen pro Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="b0f61-174">In Average Contact Groups per User, specify the number of contact groups per user.</span></span> <span data-ttu-id="b0f61-175">Diese Nummer muss kleiner als durchschnittliche Kontakte pro Nutzer sein.</span><span class="sxs-lookup"><span data-stu-id="b0f61-175">This number must be smaller than Average Contacts per User.</span></span>

4.  <span data-ttu-id="b0f61-176">Geben Sie in Prozent der Föderations-/quer Pool Kontakte eine Zahl zwischen 0 und 100 an.</span><span class="sxs-lookup"><span data-stu-id="b0f61-176">In Federated / Cross Pool Contacts Percentage, specify a number between 0 and 100.</span></span> <span data-ttu-id="b0f61-177">Dieser Prozentsatz der Kontakte wird mit den Verbundbenutzern erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-177">This percentage of contacts will be created with the federated users.</span></span>

5.  <span data-ttu-id="b0f61-178">Geben Sie im Verbund/Pool-Benutzerpräfix den Benutzernamen für Verbundbenutzer an, der den Kontaktlisten lokaler Benutzer hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f61-178">In Federated / Cross Pool User Prefix, specify the username for federated users that will be added to the contact lists of local users.</span></span>

6.  <span data-ttu-id="b0f61-179">Geben Sie in der SIP-Domäne des Federated/Cross Pool-Benutzers den SIP-Domänennamen der Föderationsbenutzer ein.</span><span class="sxs-lookup"><span data-stu-id="b0f61-179">In Federated / Cross Pool User SIP Domain, specify the SIP Domain Name of the federated users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b0f61-180">Bei der Erstellung von Kontakten sollte keiner der Benutzer angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="b0f61-180">None of the users should be signed in when creating contacts.</span></span>

    
    </div>

7.  <span data-ttu-id="b0f61-181">Überprüfen Sie auf der Registerkarte Benutzererstellung, ob die Parameter richtig sind.</span><span class="sxs-lookup"><span data-stu-id="b0f61-181">In User Creation tab, verify that the parameters are correct.</span></span> <span data-ttu-id="b0f61-182">Der Bereich der Benutzer, für die Kontakte erstellt werden, wird auf der Registerkarte Benutzererstellung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-182">The range of users for which contacts will be created is obtained from the User Creation tab.</span></span>

8.  <span data-ttu-id="b0f61-183">Klicken Sie auf Kontakte erstellen, um mit der Erstellung des Kontakts zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-183">Click Create Contacts to begin the contact creation.</span></span> <span data-ttu-id="b0f61-184">Dieser Vorgang kann mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="b0f61-184">This process can take several minutes.</span></span> <span data-ttu-id="b0f61-185">Nach Abschluss des Vorgangs wird ein Dialogfeld mit der Meldung "Vorgang wurde erfolgreich abgeschlossen" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0f61-185">After it completes, a dialog box will appear with the message, "Operation Completed Successfully."</span></span> <span data-ttu-id="b0f61-186">Sie können die Kontakte, die Sie erstellt haben, überprüfen, indem Sie sich als Benutzer anmelden, der über die Registerkarte Benutzererstellung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0f61-186">You can validate the contacts that were created by logging on as a user that was created from the User Creation tab.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b0f61-187">Nachdem die Kontakte erstellt wurden, startet dieses Tool alle Front-End-Server im Ziel Pool neu.</span><span class="sxs-lookup"><span data-stu-id="b0f61-187">After the contacts are created, this tool will restart all the Front End Servers in the target pool.</span></span> <span data-ttu-id="b0f61-188">Je nachdem, wie viele Kontakte von diesem Vorgang erstellt wurden, dauert es möglicherweise länger (bis zu zwei Stunden), bis die Front-End-Server gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-188">It may take longer (up to 2 hours) for the Front End Servers to start, depending on how many contacts were created by this operation.</span></span>

    
    </div>

</div>

<div>

## <a name="distribution-list"></a><span data-ttu-id="b0f61-189">Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="b0f61-189">Distribution List</span></span>

<span data-ttu-id="b0f61-190">Eines der Features des lync Server 2013-Tools für Stress und Leistung besteht darin, das Erweiterungsfeature Verteilerliste (DL) in lync 2013 zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-190">One of the features of the Lync Server 2013 Stress and Performance Tool is to simulate the distribution list (DL) expansion feature in Lync 2013.</span></span> <span data-ttu-id="b0f61-191">Wenn Sie die DL-Erweiterung in UserProvisioningTool nicht aktivieren möchten, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-191">If you are not going to enable DL expansion in UserProvisioningTool, you can skip this step.</span></span>

<span data-ttu-id="b0f61-192">![Registerkarte "Erstellung der Verteilerliste"](images/JJ945587.0a1d681b-2aea-4724-90d8-efa8a526f600(OCS.15).jpg "Registerkarte "Erstellung der Verteilerliste"")</span><span class="sxs-lookup"><span data-stu-id="b0f61-192">![Distribution List Creation tab.](images/JJ945587.0a1d681b-2aea-4724-90d8-efa8a526f600(OCS.15).jpg "Distribution List Creation tab.")</span></span>

<span data-ttu-id="b0f61-193">Auf der Registerkarte "Verteilerliste" können Sie DLS erstellen, die vom Tool "Spannung und Leistung" für das Erweiterungsfeature "Verteilerliste" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-193">The Distribution List tab enables you to create DLs that the Stress and Performance Tool will use for Distribution List Expansion feature.</span></span> <span data-ttu-id="b0f61-194">Vor dem Erstellen von DLS muss lync Server 2013 bereits installiert sein.</span><span class="sxs-lookup"><span data-stu-id="b0f61-194">Prior to creating DLs, Lync Server 2013 must already be installed.</span></span> <span data-ttu-id="b0f61-195">Sie müssen lync Server 2013 ForestPrep ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="b0f61-195">You must have run Lync Server 2013 ForestPrep.</span></span> <span data-ttu-id="b0f61-196">Andernfalls sind die DL-Attribute im Active Directory-Domänendienste-Schema nicht vorhanden, und das Tool kann keine DLS erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-196">Otherwise, the DL attributes do not exist in the Active Directory Domain Services schema and the tool will not be able to create DLs.</span></span>

<span data-ttu-id="b0f61-197">Führen Sie die folgenden Schritte aus, um Verteilerlisten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-197">To configure distribution lists, follow these steps.</span></span>

1.  <span data-ttu-id="b0f61-198">Geben Sie in Anzahl der Verteilerlisten die Gesamtzahl der DLS an, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="b0f61-198">In Number of Distribution Lists, specify the total number of DLs that you want to create.</span></span> <span data-ttu-id="b0f61-199">(Wir empfehlen, dass Sie mit der doppelten Anzahl von Benutzern beginnen).</span><span class="sxs-lookup"><span data-stu-id="b0f61-199">(We recommend that you start with twice the number of users).</span></span> <span data-ttu-id="b0f61-200">Sie werden von 0 bis n-1 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="b0f61-200">They are numbered from 0 to n-1.</span></span>

2.  <span data-ttu-id="b0f61-201">Geben Sie Unterverteiler Listen Präfix das Präfix an, das die DLS aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="b0f61-201">In Distribution List Prefix, specify the prefix that the DLs will have.</span></span> <span data-ttu-id="b0f61-202">Wenn Sie beispielsweise 100-DLS und ein Präfix von testDL angeben, werden die Verteilerlisten mit dem Namen testDL0, testDL1 usw. durch testDL99.</span><span class="sxs-lookup"><span data-stu-id="b0f61-202">For example if you specify 100 DLs and a prefix of testDL, the DLs will be named testDL0, testDL1, and so on, through testDL99.</span></span>

3.  <span data-ttu-id="b0f61-203">Geben Sie in minimale Mitglieder in einer Vert.-Liste die Mindestanzahl der Benutzer an, die in jeder Verteilerliste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-203">In Minimum Members in a Dist. List, specify the minimum number of users to add in each Distribution List.</span></span>

4.  <span data-ttu-id="b0f61-204">Geben Sie in maximale Anzahl von Mitgliedern in einer Vert.-Liste die maximale Anzahl der Benutzer an, die in jeder Verteilerliste hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0f61-204">In Maximum Members in a Dist. List, specify the maximum number of users to add in each Distribution List.</span></span>

<div>

## <a name="create-distribution-lists-button"></a><span data-ttu-id="b0f61-205">Schaltfläche "Verteilerlisten erstellen"</span><span class="sxs-lookup"><span data-stu-id="b0f61-205">Create Distribution Lists Button</span></span>

<span data-ttu-id="b0f61-206">Wenn Sie auf die Schaltfläche Verteilerlisten erstellen klicken, fragt das Tool die Active Directory-Domänendienste ab, um festzustellen, ob Verteilerlisten, die dem Präfix und den Nummern entsprechen, bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b0f61-206">When you click the Create Distribution Lists button, the tool queries Active Directory Domain Services to see if distribution lists matching the prefix and numbers already exist.</span></span> <span data-ttu-id="b0f61-207">Das Tool erstellt nur diejenigen, die noch nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b0f61-207">The tool will create only the ones that do not already exist.</span></span> <span data-ttu-id="b0f61-208">Beim Hinzufügen von Mitgliedern zu diesen neu erstellten Verteilerlisten werden die Benutzer aus dem Bereich ausgewählt, der auf der Registerkarte Benutzererstellung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b0f61-208">When adding members to these newly created Distribution Lists, it will pick the users from the range specified on the User Creation tab.</span></span>

</div>

</div>

<div>

## <a name="location-info-service-config-tab"></a><span data-ttu-id="b0f61-209">Registerkarte "Standortinformationen für Dienstkonfiguration"</span><span class="sxs-lookup"><span data-stu-id="b0f61-209">Location Info Service Config Tab</span></span>

<span data-ttu-id="b0f61-210">Eines der Features des lync Server 2013-Tools Stress und Leistung besteht darin, Dummy-Konfigurationsdateien für den standortinformationsdienst zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b0f61-210">One of the features of the Lync Server 2013 Stress and Performance Tool is to generate dummy configuration files for the Location Information Service.</span></span> <span data-ttu-id="b0f61-211">Der standortinformationsdienst hat in der Regel keine bedeutenden Auswirkungen auf die Leistung der Server.</span><span class="sxs-lookup"><span data-stu-id="b0f61-211">The Location Information Service typically does not have any significant performance impact on the servers.</span></span>

<span data-ttu-id="b0f61-212">![Registerkarte "Standortinformationen für Dienstkonfiguration"](images/JJ945587.52ea4e9e-d50a-4dc9-982b-31ee5ace4578(OCS.15).jpg "Registerkarte "Standortinformationen für Dienstkonfiguration"")</span><span class="sxs-lookup"><span data-stu-id="b0f61-212">![Location Info Service Config tab.](images/JJ945587.52ea4e9e-d50a-4dc9-982b-31ee5ace4578(OCS.15).jpg "Location Info Service Config tab.")</span></span>

<span data-ttu-id="b0f61-213">Wenn Sie dieses Feature testen möchten, können Sie die im Formular genannten Werte ausfüllen und dann auf die Schaltfläche "LIS-Konfigurationsdateien generieren" klicken.</span><span class="sxs-lookup"><span data-stu-id="b0f61-213">If you choose to test this feature, you can fill in the values mentioned in the form and then click the Generate LIS Config Files button.</span></span> <span data-ttu-id="b0f61-214">Sie generiert CSV-Dateien, die als LIS \_ -Subnet.csv, LIS- \_Switches.csv, LIS- \_Ports.csv und Lis-WAP.csv bezeichnet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="b0f61-214">It will generate CSV files called LIS\_Subnet.csv, LIS\_Switches.csv, LIS\_Ports.csv, and LIS\_WAP.csv.</span></span> <span data-ttu-id="b0f61-215">Sie können diese CSV-Dateien dann in die LIS-Datenbank importieren, indem Sie das Cmdlet " **CsLisSubnet** ", das Cmdlet "Satz- **CsLisSwitch** ", das Cmdlet " **Satz-CsLisPort** " und das Cmdlet "Satz **-CsWirelessAccessPoint** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0f61-215">You can then import these CSV files into LIS database by using the **Set-CsLisSubnet** cmdlet, the **Set-CsLisSwitch** cmdlet, the **Set-CsLisPort** cmdlet, and the **Set-CsWirelessAccessPoint** cmdlet, respectively.</span></span>

<span data-ttu-id="b0f61-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0f61-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

