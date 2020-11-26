---
title: 'Lync Server 2013: Integrieren von lync Server und Outlook Web App 2013'
description: 'Lync Server 2013: Integrieren von lync Server und Outlook Web App 2013'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating Lync Server 2013 and Outlook Web App 2013
ms:assetid: 513d4cc7-aa87-4f68-b99d-d58b63bdf242
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688055(v=OCS.15)
ms:contentKeyID: 49733649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d9c7e91dba22f78325eaddc5b5d7469ccf4cc92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426893"
---
# <a name="integrating-microsoft-lync-server-2013-and-microsoft-outlook-web-app-2013"></a><span data-ttu-id="2bdcf-103">Integrieren von Microsoft lync Server 2013 und Microsoft Outlook Web App 2013</span><span class="sxs-lookup"><span data-stu-id="2bdcf-103">Integrating Microsoft Lync Server 2013 and Microsoft Outlook Web App 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2bdcf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2bdcf-104">

<span> </span></span></span>

<span data-ttu-id="2bdcf-105">_**Letztes Änderungsdatum des Themas:** 2013-02-03_</span><span class="sxs-lookup"><span data-stu-id="2bdcf-105">_**Topic Last Modified:** 2013-02-03_</span></span>

<span data-ttu-id="2bdcf-106">Neben der Integration in Microsoft Outlook 2013 kann Microsoft lync Server 2013 vollständig in Microsoft Outlook Web App 2013 integriert werden. Damit werden unter anderem Instant Messaging und Anwesenheitsinformationen zu Outlook Web App hinzugefügt, und Ihre Unified Contact-Liste kann zwischen Outlook Web App und Microsoft lync 2013 freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-106">In addition to integrating with Microsoft Outlook 2013, Microsoft Lync Server 2013 can be fully integrated with Microsoft Outlook Web App 2013; among other things, this adds instant messaging and presence to Outlook Web App, and enables your unified contact list to be shared between Outlook Web App and Microsoft Lync 2013.</span></span> <span data-ttu-id="2bdcf-107">Um lync Server 2013 und Outlook Web App zu integrieren, müssen Sie zuerst überprüfen, ob die Unified Communications Managed API 4,0-Laufzeit auf dem Microsoft Exchange Server 2013-Back-End-Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-107">In order to integrate Lync Server 2013 and Outlook Web App, you must first verify that the Unified Communications Managed API 4.0 Runtime has been installed in your Microsoft Exchange Server 2013 backend server.</span></span> <span data-ttu-id="2bdcf-108">Sie können dies tun, indem Sie nach dem vorhanden sein des folgenden Registrierungswerts suchen:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-108">You can do this by looking for the existence of the following registry value:</span></span>

<span data-ttu-id="2bdcf-109">HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ MSExchange OWA \\ instantmessaging \\ ImplementationDLLPath</span><span class="sxs-lookup"><span data-stu-id="2bdcf-109">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\MSExchange OWA\\InstantMessaging\\ImplementationDLLPath</span></span>

<span data-ttu-id="2bdcf-110">ImplementationDLLPath sollte auf den Speicherort des Ordners für die Datei „Microsoft.Rtc.Internal.Ucweb.dll“ zeigen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-110">The ImplementationDLLPath should point to the folder location for the file Microsoft.Rtc.Internal.Ucweb.dll.</span></span> <span data-ttu-id="2bdcf-111">Wenn dies nicht der Fall ist, oder wenn der Registrierungswert nicht vorhanden ist, sollten Sie das UCMA-Runtime-Setup-Programm aus dem Microsoft Download Center unter herunterladen und installieren <https://www.microsoft.com/download/details.aspx?id=34992> .</span><span class="sxs-lookup"><span data-stu-id="2bdcf-111">If it does not, or if the registry value does not exist, then you should download and install the UCMA Runtime setup program from the Microsoft Download Center at <https://www.microsoft.com/download/details.aspx?id=34992>.</span></span> <span data-ttu-id="2bdcf-112">Informationen zum Installieren der UCMA Runtime finden Sie auf derselben Webseite.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-112">Information on how to install the UCMA Runtime can be found on that same web page.</span></span>

<span data-ttu-id="2bdcf-113">**Abwärtskompatibilität**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-113">**Backward Compatibility**</span></span>

<span data-ttu-id="2bdcf-114">Lync Server 2013 kann in die Microsoft Exchange Server 2010-Versionen von Unified Messaging und Outlook Web App integriert werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-114">Lync Server 2013 can be integrated with the Microsoft Exchange Server 2010 versions of both unified messaging and Outlook Web App.</span></span> <span data-ttu-id="2bdcf-115">Weitere Informationen finden Sie im Artikel Bereitstellen von lokalen Exchange um für die Bereitstellung von lync Server 2010-Voicemail [https://technet.microsoft.com/library/gg398768.aspx](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md) .</span><span class="sxs-lookup"><span data-stu-id="2bdcf-115">For more information, see the article Deploying On-Premises Exchange UM to Provide Lync Server 2010 Voice Mail at [https://technet.microsoft.com/library/gg398768.aspx](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md).</span></span> <span data-ttu-id="2bdcf-116">Wenn Sie sich in Exchange 2010 integrieren, verfügen Sie nicht über lync Server-spezifische Features wie den Unified Contact Store und die lync-zu-Exchange-Archivierung.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-116">If you integrate with Exchange 2010 you will not have Lync Server specific features such as the unified contact store and Lync-to-Exchange archiving.</span></span>

<span data-ttu-id="2bdcf-117">Microsoft lync 2013 kann auch in Verbindung mit Exchange 2010 und Outlook 2010 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-117">Microsoft Lync 2013 can also be used in conjunction with Exchange 2010 and Outlook 2010.</span></span> <span data-ttu-id="2bdcf-118">Neue Funktionen wie der Unified Contact Store und Fotos mit hoher Auflösung sind jedoch nicht für lync 2013-Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-118">Once again, however, new functionality such as the unified contact store and high-resolution photos will not be available to Lync 2013 users.</span></span> <span data-ttu-id="2bdcf-119">Diese neuen Funktionen erfordern sowohl lync Server 2013 als auch Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-119">These new capabilities require both Lync Server 2013 and Exchange 2013.</span></span>

<span data-ttu-id="2bdcf-120">**Erstellen eines vertrauenswürdigen Anwendungspools für Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-120">**Creating a Trusted Application Pool for Outlook Web App**</span></span>

<span data-ttu-id="2bdcf-121">Wenn Sie den Microsoft Exchange Unified Messaging-Anruf Router-Dienst und den Microsoft Exchange Unified Messaging-Dienst auf demselben Computer installiert haben, müssen Sie keinen vertrauenswürdigen Anwendungspool für Outlook Web App erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-121">If you have installed the Microsoft Exchange Unified Messaging Call Router service and the Microsoft Exchange Unified Messaging service on the same computer then there is no need to create a trusted application pool for Outlook Web App.</span></span> <span data-ttu-id="2bdcf-122">(Es wird davon ausgegangen, dass der fragliche Server einen SipName um-Wählplan hostet.) Wenn Sie einen einzelnen Computer zum Hosten dieser beiden Dienste verwenden, können Sie zum Abschnitt dieses Dokuments mit dem Titel **Aktivieren von Instant Messaging in Outlook Web App** springen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-122">(This assumes that the server in question is hosting a SipName UM dial plan.) If you are using a single computer to host both of these services then you can skip to the section of this document titled **Enabling Instant Messaging on Outlook Web App**.</span></span>

<span data-ttu-id="2bdcf-123">Lync Server 2013 kann alle Exchange-Server, die einen SipName um-Wählplan hosten, AutoErmittlung durchführen. Diese Server werden automatisch der Liste der bekannten lync Server-Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-123">Lync Server 2013 can autodiscover any Exchange servers that host a SipName UM dial plan; these servers are automatically added to the Lync Server Known Servers List.</span></span> <span data-ttu-id="2bdcf-124">Es ist nicht erforderlich, einen vertrauenswürdigen Anwendungspool zu erstellen und diese Server der Liste der bekannten Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-124">There is no need to create a trusted application pool and add these servers to the Known Servers List.</span></span> <span data-ttu-id="2bdcf-125">In der Tat führt dies dazu, dass die Integration von Outlook Web App nicht mehr funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-125">In fact, doing so will cause Outlook Web App integration to stop working.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2bdcf-126">Dies ist darauf zurückzuführen, dass die lync Server-Topologie nun über zwei Einträge für denselben Computer verfügt: den automatisch gefundenen Eintrag und den manuell hinzugefügten Eintrag.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-126">This is due to the fact that the Lync Server topology will now have two entries for the same computer: the autodiscovered entry, and the manually-added entry.</span></span> <span data-ttu-id="2bdcf-127">Sie können dieses Problem beheben und die Funktionsfähigkeit von Outlook Web App wiederherstellen, indem Sie mithilfe der Windows PowerShell den vertrauenswürdigen Pool und die Einträge für vertrauenswürdige Anwendungen vom Server entfernen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-127">To fix the problem, and to get Outlook Web App working again, use Windows PowerShell to remove the trusted pool and trusted application entries for the server.</span></span> <span data-ttu-id="2bdcf-128">Weitere Informationen finden Sie in den Hilfethemen zu den Cmdlets <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplicationPool">Remove-CsTrustedApplicationPool</A> und <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplication">Remove-CsTrustedApplication</A>.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-128">See the help topics for the <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplicationPool">Remove-CsTrustedApplicationPool</A> and <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsTrustedApplication">Remove-CsTrustedApplication</A> cmdlets for more information.</span></span>



</div>

<span data-ttu-id="2bdcf-129">Wenn diese beiden Dienste auf separaten Computern ausgeführt werden, müssen Sie, nachdem Sie überprüft haben, dass die 4,0-Runtime der Unified Communications-API installiert ist, einen vertrauenswürdigen lync Server-Anwendungspool und eine vertrauenswürdige Anwendung erstellen, die Outlook Web App zugeordnet ist. Dadurch wird der Server der Liste der bekannten Server hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-129">If these two services are running on separate computers then, after you have verified that the Unified Communications Managed API 4.0 Runtime has been installed, you must create a Lync Server trusted application pool and a trusted application associated with Outlook Web App; that will add the server to the Known Servers List.</span></span> <span data-ttu-id="2bdcf-130">Führen Sie dazu zunächst in der lync Server-Verwaltungsshell einen ähnlichen Befehl wie den folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-130">To do that, first run a command similar to this from within the Lync Server Management Shell:</span></span>

    New-CsTrustedApplicationPool -Identity atl-owa-001.litwareinc.com -Registrar atl-cs-001.litwareinc.com -Site Redmond -RequiresReplication $False

<span data-ttu-id="2bdcf-131">Im vorhergehenden Befehl ist ATL-OWA-001.litwareinc.com der vollqualifizierte Domänenname des Outlook Web App-Pools. Dies muss derselbe Name sein, der in den Feldern "Subject Name" und "Subject Alternative Name (San)" des Zertifikats angezeigt wird, das den Zugriff auf Outlook Web App ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-131">In the preceding command, atl-owa-001.litwareinc.com is the fully qualified domain name of the Outlook Web App pool; this must be the same name that appears in the Subject Name and Subject Alternative Name (SAN) fields of the certificate that provides access to Outlook Web App.</span></span> <span data-ttu-id="2bdcf-132">Ebenso ist ATL-CS-001.litwareinc.com der vollqualifizierte Domänenname des lync Server 2013-Pools, der den neuen vertrauenswürdigen Anwendungspool hosten soll.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-132">Likewise, atl-cs-001.litwareinc.com is the fully qualified domain name of the Lync Server 2013 pool that will host the new trusted application pool.</span></span> <span data-ttu-id="2bdcf-133">Beachten Sie auch, dass die angegebene Website, Redmond, die Website-Nr der lync Server-Website darstellt.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-133">Note, too that the specified site, Redmond, represents the SiteID of the Lync Server site.</span></span> <span data-ttu-id="2bdcf-134">Die Website-Nr ist nicht unbedingt mit dem DisplayName der Website identisch; Sie können SiteIDs für Ihre lync Server-Websites abrufen, indem Sie den folgenden Befehl in der lync Server-Verwaltungsshell ausführen:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-134">The SiteID is not necessarily the same as the site's DisplayName; you can retrieve SiteIDs for your Lync Server sites by running the following command from the Lync Server Management Shell:</span></span>

    Get-CsSite | Select-Object DisplayName, SiteID

<span data-ttu-id="2bdcf-135">Nachdem Sie den vertrauenswürdigen Anwendungspool erstellt haben, konfigurieren Sie mit einem Befehl wie dem folgenden eine Anwendungs-ID sowie einen Port für Outlook Web App:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-135">After creating the trusted application pool, use a command similar to the following to configure an application Identity and a port for Outlook Web App:</span></span>

    New-CsTrustedApplication -ApplicationId OutlookWebApp -TrustedApplicationPoolFqdn atl-owa-001.litwareinc.com  -Port 5199

<span data-ttu-id="2bdcf-p110">Bei der ApplicationID im vorherigen Befehl handelt es sich lediglich um einen Anzeigebezeichner zur Unterscheidung vertrauenswürdiger Anwendungen. Die ApplicationID kann eine beliebige Textzeichenfolge ohne Leerzeichen oder andere unzulässige Zeichen sein. (Es wird empfohlen, nur Buchstaben und Ziffern für eine ApplicationID zu verwenden, um Problemen mit der Gültigkeit vorzubeugen.) Die Angabe des Werts für den Portparameter obliegt dem Administrator: Jeder verfügbare Netzwerkport kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-p110">In the preceding command, the ApplicationID is simply a friendly identifier used to distinguish trusted applications. The ApplicationID can be any text string that does not include blank spaces or other prohibited characters. (To ensure that you create a valid identifier, it is recommended that you use only letters and numbers when specifying an ApplicationId.) The value assigned to the Port parameter is also left to the administrator's discretion: this can be any available network port.</span></span>

<span data-ttu-id="2bdcf-139">Nachdem Sie die vertrauenswürdige Anwendung erstellt haben, müssen Sie den folgenden Befehl ausführen, um die Änderungen an ihrer lync Server-Topologie zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-139">After creating the trusted application you must run the following command to enable the changes to your Lync Server topology:</span></span>

    Enable-CsTopology

<span data-ttu-id="2bdcf-140">Beachten Sie, dass Sie auch Ihren Exchange-Clientzugriffs-und Postfachserver zu allen SIP-URI-Wählplänen hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-140">Note that you must also add your Exchange client access and mailbox server to all of your SIP Uri dial plans.</span></span> <span data-ttu-id="2bdcf-141">Auf diese Weise werden die Server wiederum als vertrauenswürdige SIP-Peers mit der ExUmRouting-Topologie für lync Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-141">In turn, this will configure the servers as trusted SIP peers with the ExUmRouting topology for Lync Server.</span></span>

<span data-ttu-id="2bdcf-142">**Aktivieren von Chatfunktionen in Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-142">**Enabling Instant Messaging on Outlook Web App**</span></span>

<span data-ttu-id="2bdcf-143">Wenn lync Server richtig konfiguriert ist, können Sie mit der Konfiguration von Outlook Web App beginnen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-143">With Lync Server correctly configured you can then begin to configure Outlook Web App.</span></span> <span data-ttu-id="2bdcf-144">Aktivieren Sie dafür zunächst die Chatfunktion in allen virtuellen Verzeichnissen von Outlook Web App auf Ihren Front-End-Servern.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-144">The first step in that process is to enable instant messaging on all your Outlook Web App virtual directories on your front end servers.</span></span> <span data-ttu-id="2bdcf-145">(Auf den Back-End-Servern muss die Chatfunktion in virtuellen Verzeichnissen nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-145">(There is no need to enable instant messaging for the virtual directories on your backend servers.</span></span> <span data-ttu-id="2bdcf-146">In der Tat empfiehlt es sich, keine Chatnachrichten auf ihren Back-End-Servern zu aktivieren.) Sofortnachrichten können auf den Clientzugriffsservern aktiviert werden, indem Sie den folgenden Befehl in der Exchange-Verwaltungsshell ausführen:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-146">In fact, it is recommended that you do not enable instant messaging on your backend servers.) Instant messaging can be enabled on the client access servers by running the following command from within the Exchange Management Shell:</span></span>

    Get-OwaVirtualDirectory | Set-OwaVirtualDirectory -InstantMessagingEnabled $True -InstantMessagingType OCS

<div>


> [!NOTE]  
> <span data-ttu-id="2bdcf-p113">Bei der Installation von Outlook Web App wird die Chatfunktion standardmäßig aktiviert, d. h. die Eigenschaft „InstantMessagingEnabled“ wird auf „True“ festgelegt. Sie müssen dennoch den vorstehenden Befehl ausführen, um den Chattyp auf OCS festzulegen. „InstantMessagingType“ ist standardmäßig auf „None“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-p113">By default, instant messaging is enabled when you install Outlook Web App; that is, the InstantMessagingEnabled property is set to True. However, you must still run the preceding command in order to set the instant messaging type to OCS. By default, InstantMessagingType is set to None.</span></span>



</div>

<span data-ttu-id="2bdcf-150">Als nächstes müssen Sie die folgenden zwei Zeilen zu Outlook Web App Web.config-Datei hinzufügen (diese Datei befindet sich normalerweise im Ordner C: \\ Programmdateien \\ Microsoft \\ Exchange Server \\ V15 \\ ClientAccess \\ OWA).</span><span class="sxs-lookup"><span data-stu-id="2bdcf-150">Next you must add the following two lines to Outlook Web App Web.config file (this file is typically located in the folder C:\\Program Files\\Microsoft\\Exchange Server\\V15\\ClientAccess\\Owa).</span></span> <span data-ttu-id="2bdcf-151">Diese beiden Zeilen sollten unter dem \<AppSettings\> Knoten in der Web.config-Datei hinzugefügt werden, und diese Vorgehensweisesollte nur auf den Back-End-Servern ausgeführt werden, auf denen Outlook Web App installiert wurde:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-151">These two lines should be added under the \<AppSettings\> node in the Web.config file, and this procedure should be carried out only on the backend servers where Outlook Web App has been installed:</span></span>

    <add key="IMCertificateThumbprint" value="EA5A332496CC05DA69B75B66111C0F78A110D22d"/>
    <add key="IMServerName" value="atl-cs-001.litwareinc.com"/>

<span data-ttu-id="2bdcf-152">Im vorhergehenden Beispiel muss der Wert für IMCertificateThumbprint der Fingerabdruck für das Exchange 2013-Zertifikat sein, das auf den Back-End-Servern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-152">In the preceding example, the value for IMCertificateThumbprint must be the thumbprint for the Exchange 2013 certificate that is installed on your backend servers.</span></span> <span data-ttu-id="2bdcf-153">Sie können diese Informationen abrufen, indem Sie den folgenden Befehl in der Exchange-Verwaltungsshell ausführen:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-153">You can retrieve that information by running the following command from the Exchange Management Shell:</span></span>

    Get-ExchangeCertificate

<span data-ttu-id="2bdcf-154">Beachten Sie auch, dass der dem imservername zugewiesene Wert der vollqualifizierte Domänenname des lync Server-Pools ist, in dem Sie den vertrauenswürdigen Anwendungspool für Outlook Web App erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-154">Note, too that the value assigned to IMServerName is the fully qualified domain name of the Lync Server pool where you created the trusted application pool for Outlook Web App.</span></span>

<span data-ttu-id="2bdcf-155">Das Zertifikat, das Sie für Outlook Web App verwenden, muss ein Zertifikat sein, das von lync Server als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-155">The certificate that you use for Outlook Web App must be a certificate that is trusted by Lync Server.</span></span> <span data-ttu-id="2bdcf-156">Eine Möglichkeit, um sicherzustellen, dass das Zertifikat sowohl von lync Server als auch von Exchange als vertrauenswürdig eingestuft wird, besteht darin, die interne Zertifizierungsstelle zum Erstellen eines Zertifikats auf dem Postfachserver zu verwenden, indem Sie sicherstellen, dass der Server-FQDN für den Antragstellernamen verwendet wird und dieser FQDN im Feld Alternativer Zertifikatname angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-156">One way to ensure that the certificate will be trusted by both Lync Server and Exchange is to use your internal certificate authority to create a certificate on the mailbox server, making sure that the server FQDN is used for the subject name and that this FQDN appears in the certificate alternate name field.</span></span> <span data-ttu-id="2bdcf-157">Nachdem das Zertifikat erstellt wurde, kann es in Ihre Back-End-Server importiert werden.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-157">After the certificate has been created it can then be imported to your backend servers.</span></span> <span data-ttu-id="2bdcf-158">Das Ergebnis ist, dass dasselbe Zertifikat für zwei Zwecke verwendet wird: 1) Kommunikation zwischen Exchange Unified Messaging und lync Server; und 2) die Integration von Outlook Web App und lync Server.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-158">The net result is that the same certificate is used for two purposes: 1) communication between Exchange unified messaging and Lync Server; and, 2) the integration between Outlook Web App and Lync Server.</span></span>

<span data-ttu-id="2bdcf-159">Nachdem Sie die Web.config-Datei aktualisiert haben, sollten Sie den folgenden Befehl auf dem Exchange-Back-End-Server ausführen, um den Outlook Web App-Pool wieder zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-159">After you have updated the Web.config file you should then run the following command on the Exchange backend server in order to recycle the Outlook Web App pool:</span></span>

    C:\Windows\System32\Inetsrv\Appcmd.exe recycle apppool /apppool.name:"MSExchangeOWAAppPool"

<span data-ttu-id="2bdcf-160">Wenn der Wiederverwendungsvorgang erfolgreich ausgeführt wird, wird in der Exchange-Verwaltungsshell die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-160">If the recycle operation succeeds you will see the following message in the Exchange Management Shell:</span></span>

    "MSExchangeOWAAppPool" successfully recycled

<span data-ttu-id="2bdcf-161">**Konfigurieren von Outlook Web App-Postfachrichtlinien**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-161">**Configuring Outlook Web App Mailbox Policies**</span></span>

<span data-ttu-id="2bdcf-p117">Nun können Sie mit dem folgenden Befehl die Sofortnachrichtenfunktion in den entsprechenden Postfachrichtlinien von Outlook Web App konfigurieren. Beispielsweise aktiviert der folgende Befehl die Sofortnachrichtenfunktion in der Standardrichtlinie, wenn er auf einem Ihrer Postfachserver ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-p117">At this point you can use the following command to configure instant messaging on the appropriate Outlook Web App mailbox policy (or policies). For example, this command, run on one of your mailbox servers, enables instant messaging on the Default policy:</span></span>

    Set-OwaMailboxPolicy -Identity "Default" -InstantMessagingEnabled $True -InstantMessagingType "OCS"

<span data-ttu-id="2bdcf-164">Und mit dem folgenden Befehl wird die Sofortnachrichtenfunktion für alle Outlook Web App-Postfachrichtlinien aktiviert:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-164">And this command enables instant messaging for all your Outlook Web App mailbox policies:</span></span>

    Get-OwaMailboxPolicy | Set-OwaMailboxPolicy -InstantMessagingEnabled $True -InstantMessagingType "OCS"

<span data-ttu-id="2bdcf-165">Nachdem die Postfachrichtlinie aktiviert wurde, verfügen alle Benutzer, die von dieser Richtlinie verwaltet werden, über eine vollständige Integration zwischen lync Server und Outlook Web App, vorausgesetzt, dass:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-165">After the mailbox policy has been enabled then all users managed by that policy will have full integration between Lync Server and Outlook Web App, provided that:</span></span>

  - <span data-ttu-id="2bdcf-166">Der Benutzer verfügt über ein Postfach in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-166">The user has a mailbox on Exchange 2013.</span></span>

  - <span data-ttu-id="2bdcf-167">Der Benutzer wurde für lync Server 2013 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-167">The user has been enabled for Lync Server 2013.</span></span>

  - <span data-ttu-id="2bdcf-168">Der Benutzer verfügt über eine gültige SIP-Proxyadresse.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-168">The user has a valid SIP proxy address.</span></span>

<span data-ttu-id="2bdcf-169">**Deaktivieren der Chatfunktion in Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-169">**Disabling Instant Messaging in Outlook Web App**</span></span>

<span data-ttu-id="2bdcf-170">Wie bereits erwähnt ist die Chatfunktion in Outlook Web App standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-170">As noted previously, instant messaging is enabled by default in Outlook Web App.</span></span> <span data-ttu-id="2bdcf-171">Wenn Sie Outlook Web App nicht in lync Server integrieren, werden Benutzern bei jeder Anmeldung bei Outlook Web App leere anwesenheitssymbole und eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-171">That means that, if you do not integrate Outlook Web App with Lync Server, users will see blank presence icons and an error message each time they log on to Outlook Web App.</span></span> <span data-ttu-id="2bdcf-172">Um dieses Problem zu vermeiden, verwenden Sie den folgenden Befehl der Exchange-Verwaltungsshell, um Chatnachrichten in Outlook Web App zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="2bdcf-172">To prevent this problem, use the following Exchange Management Shell command to disable instant messaging in Outlook web App:</span></span>

    Get-OwaVirtualDirectory | Set-OwaVirtualDirectory -InstantMessagingEnabled $False

<span data-ttu-id="2bdcf-173">**Überprüfen der Integration in Outlook Web App**</span><span class="sxs-lookup"><span data-stu-id="2bdcf-173">**Verifying Integration With Outlook Web App**</span></span>

<span data-ttu-id="2bdcf-174">Um die Integration der Chat- und Anwesenheitsfunktion in Outlook Web App zu überprüfen, melden Sie sich bei Outlook Web App 2013 an.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-174">To verify that instant messaging and presence have been integrated with Outlook Web App, sign on to Outlook Web App 2013.</span></span> <span data-ttu-id="2bdcf-175">Oben rechts im Bildschirm ist Ihr Exchange-Anzeigename zu sehen.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-175">In the upper right-hand corner of the screen, you will see your Exchange display name.</span></span> <span data-ttu-id="2bdcf-176">Wenn neben Ihrem Namen ein Anwesenheitssymbol angezeigt wird (beispielsweise ein grünes Symbol, das angibt, dass Ihr aktueller Status verfügbar ist), der angibt, dass Sie lync Server und Outlook Web App erfolgreich integriert haben.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-176">If there is a presence icon next to your name (for example, a green icon indicating that your current status is Available) that indicates that you have successfully integrated Lync Server and Outlook Web App.</span></span>

<span data-ttu-id="2bdcf-177">Überprüfen Sie nach der ersten Anmeldung an Outlook Web App, ob ein Ereignis mit der ID 112 (und der Quelle „MSExchange OWA“) in das Ereignisprotokoll auf dem Postfachserver geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-177">After the initial sign-on to Outlook Web App, check to see if an event with the Event ID 112 (and the source MSExchange OWA) has been written to the event log on the mailbox server.</span></span> <span data-ttu-id="2bdcf-178">Das Ereignis zeigt an, dass der Instant Messaging Endpoint Manager erfolgreich initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-178">This event indicates that the Instant Messaging Endpoint Manager was successfully initialized.</span></span> <span data-ttu-id="2bdcf-179">Wenn Instant Messaging nicht zu funktionieren scheint, suchen Sie auf dem Postfachserver nach Protokolldateien in dem Ordner C: \\ Programmdateien \\ Microsoft \\ Exchange Server \\ V15 Protokollierung von \\ \\ OWA- \\ instantmessaging.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-179">If instant messaging does not appear to be working then, on the mailbox server, look for log files in the folder C:\\Program Files\\Microsoft\\Exchange server\\V15\\Logging\\OWA\\InstantMessaging.</span></span> <span data-ttu-id="2bdcf-180">Wenn der Ordner „Logging“ oder der Ordner „InstantMessaging“ nicht vorhanden ist, deutet dies darauf hin, dass die Integration fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-180">If either the Logging or the InstantMessaging folders do not exist that indicates that integration has failed.</span></span> <span data-ttu-id="2bdcf-181">In diesem Fall können Sie die SIPStack-Ablaufverfolgung auf lync Server (alle Ebenen und alle Flags) verwenden, um zu versuchen, zu ermitteln, warum die Integration fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2bdcf-181">In that case, you can use SIPStack tracing on Lync Server (All Levels and All Flags) to try and determine why integration failed.</span></span>

<span data-ttu-id="2bdcf-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2bdcf-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

