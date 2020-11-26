---
title: 'Lync Server 2013: Verwenden der zweistufigen Authentifizierung mit lync-Client'
description: 'Lync Server 2013: Verwenden der zweistufigen Authentifizierung mit lync-Client.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using two-factor authentication with Lync client
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn338071(v=OCS.15)
ms:contentKeyID: 55115593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbfde1d04d4e641c8fbe4817ffce214df891b565
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438687"
---
# <a name="using-two-factor-authentication-with-lync-client-and-lync-server-2013"></a><span data-ttu-id="a6cda-103">Verwenden der zweistufigen Authentifizierung mit lync-Client und lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6cda-103">Using two-factor authentication with Lync client and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6cda-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6cda-104">

<span> </span></span></span>

<span data-ttu-id="a6cda-105">_**Letztes Änderungsdatum des Themas:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="a6cda-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="a6cda-106">In diesem Thema wurde beschrieben, wie Sie die zweistufige Authentifizierung mit lync 2013-Client nutzen können.</span><span class="sxs-lookup"><span data-stu-id="a6cda-106">This topic described how to take advantage of two-factor authentication with Lync 2013 client.</span></span>

<div>

## <a name="sign-in-to-lync-2013-for-the-first-time"></a><span data-ttu-id="a6cda-107">Erstmaliges Anmelden bei lync 2013</span><span class="sxs-lookup"><span data-stu-id="a6cda-107">Sign in to Lync 2013 for the first time</span></span>

<span data-ttu-id="a6cda-108">Ihre lync-Anmeldeinformationen werden in der Regel automatisch konfiguriert, wenn lync 2013 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a6cda-108">Your Lync sign-in information is usually configured automatically when Lync 2013 is installed.</span></span> <span data-ttu-id="a6cda-109">Wenn Sie lync zum ersten Mal verwenden, müssen Sie den Client möglicherweise manuell starten.</span><span class="sxs-lookup"><span data-stu-id="a6cda-109">But the first time you use Lync, you might have to manually start the client.</span></span>

<span data-ttu-id="a6cda-110">**So können Sie sich zum ersten Mal bei lync anmelden**</span><span class="sxs-lookup"><span data-stu-id="a6cda-110">**To sign in to Lync for the first time**</span></span>

1.  <span data-ttu-id="a6cda-111">Melden Sie sich beim Netzwerk Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="a6cda-111">Log on to your organization’s network.</span></span>

2.  <span data-ttu-id="a6cda-112">Wählen **Start** Sie \> **Alle Programme** starten \> **Microsoft \> lync lync 2013** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-112">Select **Start** \> **All Programs** \> **Microsoft Lync \> Lync 2013**.</span></span>
    
    <span data-ttu-id="a6cda-113">Der Anmeldebildschirm von lync sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a6cda-113">You should see the Lync sign-in screen.</span></span>
    
      - <span data-ttu-id="a6cda-114">Wenn das Feld mit der Anmeldeadresse bereits ausgefüllt ist, überprüfen Sie, ob die angezeigte Adresse richtig ist.</span><span class="sxs-lookup"><span data-stu-id="a6cda-114">If the sign-in address box is already filled in, confirm that the address shown is correct.</span></span>
    
      - <span data-ttu-id="a6cda-115">Wenn dies nicht der Fall ist, oder wenn das Feld leer ist, geben Sie Ihre lync-Anmeldeadresse ein (Dies ist in der Regel identisch mit Ihrer e-Mail-Adresse).</span><span class="sxs-lookup"><span data-stu-id="a6cda-115">If it’s not correct, or if the box is empty, enter your Lync sign-in address (this is usually the same as your email address).</span></span>
    
      - <span data-ttu-id="a6cda-116">Wenn ein leeres Kennwortfeld angezeigt wird, geben Sie Ihr Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="a6cda-116">If an empty password box is displayed, add your password.</span></span>

3.  <span data-ttu-id="a6cda-117">Wählen Sie **Anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-117">Select **Sign-in**.</span></span>

</div>

<div>

## <a name="sign-out-of-lync"></a><span data-ttu-id="a6cda-118">Abmelden bei lync</span><span class="sxs-lookup"><span data-stu-id="a6cda-118">Sign out of Lync</span></span>

<span data-ttu-id="a6cda-119">Wenn Sie mit der Verwendung von lync fertig sind, können Sie die Anzeige schließen, sich von Ihrer Sitzung abmelden oder das Programm beenden, und zwar alle über das Menü "Datei".</span><span class="sxs-lookup"><span data-stu-id="a6cda-119">When you’re finished using Lync, you can close the display, sign out of your session, or exit from the program, all from the File menu.</span></span> <span data-ttu-id="a6cda-120">In der folgenden Tabelle werden die Unterschiede zwischen diesen Optionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="a6cda-120">The following table explains the differences in the options.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6cda-121">Option</span><span class="sxs-lookup"><span data-stu-id="a6cda-121">Option</span></span></th>
<th><span data-ttu-id="a6cda-122">Zweck</span><span class="sxs-lookup"><span data-stu-id="a6cda-122">What it does</span></span></th>
<th><span data-ttu-id="a6cda-123">Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="a6cda-123">How to perform it</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6cda-124">Schließen</span><span class="sxs-lookup"><span data-stu-id="a6cda-124">Close</span></span></p></td>
<td><p><span data-ttu-id="a6cda-125">Schließt die lync-Anzeige, lässt aber die lync-Sitzung, die mit Ihrer Benutzer-ID identifiziert wurde, weiterhin ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a6cda-125">Closes your Lync display but lets the Lync session identified with your user ID continue to run.</span></span> <span data-ttu-id="a6cda-126">Dies hat den Sinn, dass Sie weiterhin Benachrichtigungen erhalten und sich mit anderen austauschen können.</span><span class="sxs-lookup"><span data-stu-id="a6cda-126">This is so you can continue to get notifications and interact with others.</span></span></p>
<p><span data-ttu-id="a6cda-127">Sie können die Anzeige jederzeit wiederherstellen, indem Sie auf das lync-Symbol in der Taskleiste oder im Infobereich am unteren Rand des Bildschirms klicken.</span><span class="sxs-lookup"><span data-stu-id="a6cda-127">You can get the display back at any time by clicking the Lync icon on the taskbar or the notification area at the bottom of your screen.</span></span></p></td>
<td><p><span data-ttu-id="a6cda-128">Führen Sie im lync-Hauptfenster eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a6cda-128">On the Lync main window, do one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="a6cda-129">Wählen Sie die Schaltfläche <strong>Optionen</strong> und dann <strong>Datei</strong> &gt; <strong>Schließen</strong>aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-129">Select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Close</strong>.</span></span></p></li>
<li><p><span data-ttu-id="a6cda-130">Klicken Sie auf die Schaltfläche <strong>Schließen</strong> (X) in der oberen rechten Ecke des Fensters.</span><span class="sxs-lookup"><span data-stu-id="a6cda-130">Click the <strong>Close</strong> button (X) in the upper-right corner of the window.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6cda-131">Abmelden</span><span class="sxs-lookup"><span data-stu-id="a6cda-131">Sign out</span></span></p></td>
<td><p><span data-ttu-id="a6cda-132">Beendet die mit Ihrer Benutzer-ID verknüpfte lync-Sitzung, während lync weiterhin im Hintergrund ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6cda-132">Ends the Lync session associated with your user ID, but Lync continues to run in the background.</span></span> <span data-ttu-id="a6cda-133">Wenn Sie sich abmelden, wird das Abmeldefenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6cda-133">When you sign out, the sign-in window will appear.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="a6cda-p105">Wählen Sie bei der Abmeldung <STRONG>Meine Anmeldeinformationen löschen</STRONG> aus, um den Datensatz mit Ihrer Anmelde-ID und dem Kennwort vom Computer zu entfernen. Dies vereinfacht möglicherweise den Support bei der Behandlung von Anmeldeproblemen. Außerdem trägt es dazu bei, Ihre Anmeldeinformationen zu sichern, da es nicht autorisierten Benutzern so erschwert wird, sich mit Ihren Anmeldeinformationen anzumelden.</span><span class="sxs-lookup"><span data-stu-id="a6cda-p105">Select <STRONG>Delete my sign-in information</STRONG> when you sign out to remove the record of your logon ID and password from the computer. Doing this might make it easier for support people to troubleshoot sign-in issues. It can also help ensure your sign-in information is more secure by making it difficult for unauthorized users to log on with your credentials.</span></span>


</div></td>
<td><p><span data-ttu-id="a6cda-137">Klicken Sie im Hauptfenster von lync auf die Schaltfläche <strong>Optionen</strong> , und wählen Sie dann <strong>Datei</strong> &gt; <strong>Abmelden aus</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6cda-137">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Sign Out</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6cda-138">Beenden</span><span class="sxs-lookup"><span data-stu-id="a6cda-138">Exit</span></span></p></td>
<td><p><span data-ttu-id="a6cda-139">Beendet die lync-Sitzung und beendet lync auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="a6cda-139">Ends your Lync session and shuts down Lync on your computer.</span></span> <span data-ttu-id="a6cda-140">Wenn Sie lync nach dem Beenden erneut starten möchten, wählen Sie <strong>Start</strong> &gt; <strong>Alle Programme</strong> starten &gt; <strong>Microsoft lync</strong> &gt; <strong>lync 2013</strong>aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-140">After exiting, if you want to restart Lync, select <strong>Start</strong> &gt; <strong>All Programs</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span></span></p></td>
<td><p><span data-ttu-id="a6cda-141">Klicken Sie im Hauptfenster von lync auf die Schaltfläche <strong>Optionen</strong> , und wählen Sie dann <strong>Datei</strong> &gt; <strong>Beenden</strong>aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-141">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Exit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sign-in-to-lync-with-a-smart-card"></a><span data-ttu-id="a6cda-142">Anmelden bei lync mit einer Smartcard</span><span class="sxs-lookup"><span data-stu-id="a6cda-142">Sign in to Lync with a Smart Card</span></span>

<span data-ttu-id="a6cda-143">Einige Organisationen verwenden jetzt einen mehrstufigen Anmeldeprozess mit der Bezeichnung zweistufige Authentifizierung, um die Sicherheit für Ihre lync 2013-Benutzer zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a6cda-143">Some organizations now use a multi-step sign-in process, called two-factor authentication, to increase security for their Lync 2013 users.</span></span> <span data-ttu-id="a6cda-144">Wenn Sie davon ausgehen, dass Sie diese Option verwenden, benötigen Sie eine "Smartcard", um sich bei lync anzumeldet.</span><span class="sxs-lookup"><span data-stu-id="a6cda-144">If you’re expected to use this option, you’ll need a “smart card” to sign in to Lync.</span></span> <span data-ttu-id="a6cda-145">Smartcards sind in zwei Varianten erhältlich:</span><span class="sxs-lookup"><span data-stu-id="a6cda-145">Smart cards come in two varieties, physical and virtual:</span></span>

  - <span data-ttu-id="a6cda-146">**Physisch**   Über die Größe einer Kreditkarte.</span><span class="sxs-lookup"><span data-stu-id="a6cda-146">**Physical**   About the size of a credit card.</span></span> <span data-ttu-id="a6cda-147">Sie setzen sie für die Anmeldung in ein SmartCard-Lesegerät ein.</span><span class="sxs-lookup"><span data-stu-id="a6cda-147">You insert it into a smart card reader when you log in.</span></span>

  - <span data-ttu-id="a6cda-148">**Virtuelles**   Kein physikalisches Objekt, sondern ein elektronischer Bezeichner, der auf einen speziellen Chip auf dem Computer geschrieben wird, der im Wesentlichen die Smartcard auf Ihren Computer aufbaut.</span><span class="sxs-lookup"><span data-stu-id="a6cda-148">**Virtual**   Not a physical object, but an electronic identifier that gets written to a special chip on your computer, which in essence builds the smart card into your computer.</span></span> <span data-ttu-id="a6cda-149">Nur für die Verwendung mit Windows 8-Computern verfügbar, die den TPM-Chip (Trusted Platform Module) enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6cda-149">Available only for use with Windows 8 computers that contain the TPM (Trusted Platform Module) chip.</span></span>

<div>

## <a name="enroll-your-smart-card"></a><span data-ttu-id="a6cda-150">Registrieren Ihrer SmartCard</span><span class="sxs-lookup"><span data-stu-id="a6cda-150">Enroll your smart card</span></span>

<span data-ttu-id="a6cda-151">Bevor Sie sich mit einer SmartCard anmelden können, muss die Karte „registriert“ werden – das bedeutet, dass Ihre Benutzeranmeldeinformationen für die Karte kenntlich gemacht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a6cda-151">Before you can sign in with a smart card, the card must be “enrolled”—that is, your user credentials have to be identified with the card.</span></span> <span data-ttu-id="a6cda-152">Dies muss unabhängig davon erfolgen, ob es sich um eine physische oder um eine virtuelle Karte handelt.</span><span class="sxs-lookup"><span data-stu-id="a6cda-152">This is the case whether the card is physical or virtual.</span></span> <span data-ttu-id="a6cda-153">Dieser Vorgang wurde möglicherweise bereits vom lync Server-Administrator durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6cda-153">This process may already been carried out by your Lync Server administrator.</span></span> <span data-ttu-id="a6cda-154">Erkundigen Sie sich bei ihm, wenn Sie nicht sicher sind, ob dieser Vorgang bereits ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a6cda-154">Check with them if you’re not sure whether that has been done.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6cda-155">Da jede virtuelle Smartcard nur dem Gerät zugeordnet ist, auf dem Sie installiert ist, muss für jeden Windows 8-Computer, den Sie verwenden, eine separate Karte registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a6cda-155">Since each virtual smart card is associated only with the device it’s installed on, a separate card will need to be enrolled for each Windows 8 computer you use.</span></span>



</div>

<span data-ttu-id="a6cda-156">**So registrieren Sie Ihre SmartCard**</span><span class="sxs-lookup"><span data-stu-id="a6cda-156">**To manually enroll your smart card**</span></span>

1.  <span data-ttu-id="a6cda-157">Melden Sie sich bei dem Computer an, auf dem Sie lync ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="a6cda-157">Log on to the computer you’ll be running Lync on.</span></span>

2.  <span data-ttu-id="a6cda-158">Navigieren Sie im Internet Explorer zur Registrierungsseite der Zertifizierungsstelle Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="a6cda-158">Using Internet Explorer, browse to your organization’s Certificate Authority Web Enrollment page.</span></span>
    
    <span data-ttu-id="a6cda-159">Bitten Sie Ihren lync Server-Administrator um die Webadresse dieser Ressource, wenn Sie Sie nicht bereits haben.</span><span class="sxs-lookup"><span data-stu-id="a6cda-159">Ask your Lync Server administrator for the web address of this resource if you don’t already have it.</span></span> <span data-ttu-id="a6cda-160">Die URL sieht ungefähr wie folgt aus: https://MyCA.\ [YourCompanyName \] . com/certsrv.</span><span class="sxs-lookup"><span data-stu-id="a6cda-160">The URL will look something like this: https://MyCA.\[yourcompanyname\].com/certsrv.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6cda-161">Wenn Sie Internet Explorer 10 verwenden, müssen Sie diese Website möglicherweise im Kompatibilitätsmodus anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a6cda-161">If you’re using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

3.  <span data-ttu-id="a6cda-162">Wenn Sie aufgefordert werden, sich auf der Zertifizierungsseite anzumelden, melden Sie sich mit Ihrem Domänenkonto (statt als Administrator Ihres Computers) an.</span><span class="sxs-lookup"><span data-stu-id="a6cda-162">When you’re prompted to log on to the certification page, log on using your domain account (rather than as administrator of your computer).</span></span>

4.  <span data-ttu-id="a6cda-163">Wählen Sie auf der Begrüßungsseite die Option **Zertifikat anfordern** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-163">On the website Welcome Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="a6cda-164">Wählen Sie **Erweiterte Anforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-164">Select **Advanced Request**.</span></span>

6.  <span data-ttu-id="a6cda-165">Wählen Sie **Eine Anforderung an diese Zertifizierungsstelle erstellen und einreichen** und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-165">Select **Create and submit a request to this CA**, then click **Next**.</span></span>

7.  <span data-ttu-id="a6cda-166">Jetzt wird eine Seite mit dem Titel SmartCard-Registrierungsstelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a6cda-166">Now you’ll see a page called Smart Card Enrollment Station.</span></span> <span data-ttu-id="a6cda-167">Genehmigen Sie die Anfrage, das ActiveX-Steuerelement zu installieren, und füllen Sie dann das Formular für die erweiterte Zertifikatanforderung wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="a6cda-167">Approve the request to install the ActiveX control, and then complete the Advanced Certificate Request form as follows:</span></span>
    
    1.  <span data-ttu-id="a6cda-168">Wählen Sie in der Dropdownliste **Zertifikatvorlage** den Eintrag **SmartCard-Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-168">Select **Smartcard user** from the **Certificate Template** dropdown list.</span></span>
    
    2.  <span data-ttu-id="a6cda-169">Wählen Sie **Neuen Schlüsselsatz erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-169">Select **Create new key set**.</span></span>
    
    3.  <span data-ttu-id="a6cda-170">Suchen Sie die Herstellerinformationen auf dem Etikett Ihrer SmartCard und wählen Sie dann den betreffenden Hersteller in der **CSP**-Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="a6cda-170">Find the manufacturer information on the label of your smart card and select that manufacturer from the **CSP** dropdown list.</span></span>
    
    4.  <span data-ttu-id="a6cda-171">Wählen Sie **CSP** als Anforderungsformat aus, wenn dies noch nicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6cda-171">Select **CSP** as the Request Format, if it’s not already selected.</span></span>
    
    5.  <span data-ttu-id="a6cda-172">Wählen Sie in der Hashalgorithmus-Dropdownliste den Eintrag **sha1** aus, wenn er noch nicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a6cda-172">Select **sha1** from the Hash Algorithm dropdown list, if it’s not already selected.</span></span>
    
    6.  <span data-ttu-id="a6cda-173">Geben Sie Ihrem Zertifikat einen Namen, den Sie sich merken können und klicken Sie dann auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-173">Give your certificate a name you’ll recognize, and click **Submit**.</span></span>

8.  <span data-ttu-id="a6cda-174">Legen Sie jetzt Ihre leere SmartCard in das an die Registrierungsstelle angeschlossene SmartCard-Lesegerät und klicken Sie auf **Registrieren**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-174">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

9.  <span data-ttu-id="a6cda-175">Wenn Sie dazu aufgefordert werden, geben Sie Ihre PIN (Personal Identification Number) ein und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-175">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6cda-176">Wenn der für Sie zuständige Mitarbeiter des technischen Supports Ihnen keine besondere PIN für die Registrierung Ihrer SmartCard gegeben hat, verwenden Sie die Standard-PIN für SmartCards, nämlich 12345678.</span><span class="sxs-lookup"><span data-stu-id="a6cda-176">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

10. <span data-ttu-id="a6cda-177">Aktivieren Sie die Option, die den Benutzer (Sie) zwingt, die PIN bei der ersten Verwendung der SmartCard zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6cda-177">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

11. <span data-ttu-id="a6cda-178">Legen Sie jetzt Ihre leere SmartCard in das an die Registrierungsstelle angeschlossene SmartCard-Lesegerät und klicken Sie auf **Registrieren**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-178">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

12. <span data-ttu-id="a6cda-179">Wenn Sie dazu aufgefordert werden, geben Sie Ihre PIN (Personal Identification Number) ein und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-179">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6cda-180">Wenn der für Sie zuständige Mitarbeiter des technischen Supports Ihnen keine besondere PIN für die Registrierung Ihrer SmartCard gegeben hat, verwenden Sie die Standard-PIN für SmartCards, nämlich 12345678.</span><span class="sxs-lookup"><span data-stu-id="a6cda-180">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

13. <span data-ttu-id="a6cda-181">Aktivieren Sie die Option, die den Benutzer (Sie) zwingt, die PIN bei der ersten Verwendung der SmartCard zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a6cda-181">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

14. <span data-ttu-id="a6cda-182">Klicken Sie auf **OK**, um zu bestätigen, dass das angezeigte Zertifikat Ihre Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a6cda-182">Click **OK** to confirm that the certificate displayed has your information on it.</span></span>

15. <span data-ttu-id="a6cda-183">Sobald der Hinweis angezeigt wird, dass das Zertifikat ausgestellt wurde, klicken Sie auf **Dieses Zertifikat installieren**, um den Registrierungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a6cda-183">Once you see the notice that the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>

</div>

<div>

## <a name="sign-in-to-lync-with-your-smart-card-credentials"></a><span data-ttu-id="a6cda-184">Melden Sie sich mit ihren Smartcard-Anmeldeinformationen bei lync an.</span><span class="sxs-lookup"><span data-stu-id="a6cda-184">Sign in to Lync with your smart card credentials</span></span>

<span data-ttu-id="a6cda-185">Bevor Sie Ihre Smartcard zum ersten Mal verwenden, sollten Sie auf der lync-Anmeldeseite auf **Meine Anmeldeinformationen löschen** klicken.</span><span class="sxs-lookup"><span data-stu-id="a6cda-185">Before you use your smart card for the first time, it’s recommended that you click **Delete my sign-in info** on the Lync sign-in page.</span></span> <span data-ttu-id="a6cda-186">Dadurch werden alle eventuell auf dem Computer gespeicherten Anmeldeinformationen gelöscht und eine mögliche Fehlerquelle ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="a6cda-186">Doing this clears any sign-in credentials stored on your computer, and eliminates a possible source of error.</span></span>

<span data-ttu-id="a6cda-187">**So melden Sie sich mit ihren Smartcard-Anmeldeinformationen bei lync an**</span><span class="sxs-lookup"><span data-stu-id="a6cda-187">**To sign in to Lync with your smart card credentials**</span></span>

1.  <span data-ttu-id="a6cda-188">Starten Sie den lync-Client.</span><span class="sxs-lookup"><span data-stu-id="a6cda-188">Start the Lync client.</span></span>

2.  <span data-ttu-id="a6cda-189">Geben Sie auf dem Anmeldebildschirm Ihren Benutzerkontonamen für die Anmeldung im Feld **Anmeldeadresse** ein und klicken Sie dann auf **Anmelden**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-189">On the Sign in screen, type your sign in user account name in the **Sign-in address** box, and then click **Sign In**.</span></span>

3.  <span data-ttu-id="a6cda-190">Wenn Sie eine virtuelle SmartCard verwenden, überspringen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="a6cda-190">If you are using a virtual smart card, skip this step.</span></span>
    
    <span data-ttu-id="a6cda-191">Wenn Sie eine physische SmartCard verwenden, legen Sie die SmartCard in Ihr SmartCard-Lesegerät ein, wenn Sie dazu aufgefordert werden, und klicken dann auf **OK**, wenn die Karte erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="a6cda-191">If you are using a physical smart card, insert the smart card into your smart card reader and prompted to do so, and then click **OK** when the card is detected.</span></span>

4.  <span data-ttu-id="a6cda-192">Geben Sie die PIN-Nummer für Ihre SmartCard ein und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6cda-192">Type in the PIN number you for your smart card and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6cda-193">Wenn Ihnen keine SmartCard-PIN von Ihrem Supportmitarbeiter zugewiesen wurde, verwenden Sie den Standardwert, nämlich 12345678.</span><span class="sxs-lookup"><span data-stu-id="a6cda-193">If you were not assigned a smart card PIN number by your support person, use the default value, which is 12345678.</span></span>

    
    <span data-ttu-id="a6cda-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6cda-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

