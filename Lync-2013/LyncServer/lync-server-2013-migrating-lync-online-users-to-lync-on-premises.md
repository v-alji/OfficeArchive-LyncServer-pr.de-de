---
title: 'Lync Server 2013: Migrieren von lync Online-Benutzern zu lync lokal'
description: 'Lync Server 2013: Migrieren von lync Online-Benutzern zu lync lokal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migrating Lync Online users to Lync on-premises
ms:assetid: 0e29605b-db2d-4cbf-b6a9-15db6b9fdabc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689115(v=OCS.15)
ms:contentKeyID: 62258120
ms.date: 11/13/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 620bc07def8e3c1f6b761c6398b452b4dbcd3b04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445981"
---
# <a name="migrating-lync-online-users-to-lync-on-premises-in-lync-server-2013"></a><span data-ttu-id="f5386-103">Migrieren von lync Online-Benutzern zu lync lokal in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5386-103">Migrating Lync Online users to Lync on-premises in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5386-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5386-104">

<span> </span></span></span>

<span data-ttu-id="f5386-105">_**Letztes Änderungsdatum des Themas:** 2015-11-13_</span><span class="sxs-lookup"><span data-stu-id="f5386-105">_**Topic Last Modified:** 2015-11-13_</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="f5386-106">Diese Schritte sind nur für die Migration von Benutzerkonten erforderlich, die ursprünglich für lync in lync Online aktiviert waren, bevor Sie lync lokal bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="f5386-106">These steps are necessary only for migrating user accounts that were originally enabled for Lync in Lync Online, before you deployed Lync on-premises.</span></span> <span data-ttu-id="f5386-107">Informationen zum Verschieben von Benutzern, die ursprünglich für lync lokal aktiviert wurden und später in lync Online verschoben wurden, finden Sie unter <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Verwalten von Benutzern in einer hybriden lync Server 2013-Bereitstellung</A>.</span><span class="sxs-lookup"><span data-stu-id="f5386-107">To move users who were originally enabled for Lync on-premises, then later moved to Lync Online, see <A href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</A>.</span></span><BR><span data-ttu-id="f5386-108">Darüber hinaus müssen alle Benutzer, die verschoben werden, über Konten im lokalen Active Directory verfügen.</span><span class="sxs-lookup"><span data-stu-id="f5386-108">Additionally, all users being moved must have accounts in the on-premises Active Directory.</span></span>



</div>

<div>

## <a name="migrating-user-accounts-originally-enabled-in-lync-online-to-lync-on-premises"></a><span data-ttu-id="f5386-109">Migrieren von Benutzerkonten, die ursprünglich in lync Online aktiviert sind, lokal in lync</span><span class="sxs-lookup"><span data-stu-id="f5386-109">Migrating User Accounts Originally Enabled in Lync Online to Lync On-Premises</span></span>

1.  <span data-ttu-id="f5386-110">Stellen Sie zunächst sicher, dass Ihre Organisation für Hybrid konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f5386-110">First, make sure that your organization is configured for hybrid.</span></span>
    
      - <span data-ttu-id="f5386-111">Installieren Sie das Azure Active Directory-Synchronisierungs Tool.</span><span class="sxs-lookup"><span data-stu-id="f5386-111">Install the Azure Active Directory Sync Tool.</span></span> <span data-ttu-id="f5386-112">Weitere Informationen finden Sie unter <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f5386-112">For more information, see <https://social.technet.microsoft.com/wiki/contents/articles/19098.howto-install-the-windows-azure-active-directory-sync-tool.aspx>.</span></span>
    
      - <span data-ttu-id="f5386-113">Wenn Sie Ihren Benutzern die Verwendung von einmaligem Anmelden für lync Online ermöglichen möchten, installieren Sie die Active Directory-Verbunddienste <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx> .</span><span class="sxs-lookup"><span data-stu-id="f5386-113">To enable your users to use single sign-on for Lync Online, install Active Directory Federation Services <https://social.technet.microsoft.com/wiki/contents/articles/1011.active-directory-federation-services-ad-fs-overview.aspx>.</span></span>
    
      - <span data-ttu-id="f5386-114">Geben Sie in Ihrer lokalen Bereitstellung in der lync Server-Verwaltungsshell die folgenden Cmdlets ein, um den Hostinganbieter für lync online zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f5386-114">On your on-premises deployment, in Lync Server Management Shell, type the following cmdlets to create the hosting provider for Lync Online:</span></span>
        
           ```PowerShell
           Set-CsAccessEdgeConfiguration -AllowOutsideUsers 1 -AllowFederatedUsers 1 -UseDnsSrvRouting -EnablePartnerDiscovery $true
           ```
        
           ```PowerShell
            New-CsHostingProvider -Identity LyncOnline -ProxyFqdn "sipfed.online.lync.com" -Enabled $true -EnabledSharedAddressSpace $true -HostsOCSUsers $true -VerificationLevel UseSourceVerification -IsLocal $false -AutodiscoverUrl https://webdir.online.lync.com/Autodiscover/AutodiscoverService.svc/root
           ```

2.  <span data-ttu-id="f5386-115">Vergewissern Sie sich, dass Sie auf Ihren lokalen Edgeserver über die Zertifikatkette verfügen, die die Verbindung zu lync Online ermöglicht, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5386-115">Confirm that, on your on-premises Edge Servers, you have the certificate chain that enables connection to Lync Online, as shown in the following table.</span></span> <span data-ttu-id="f5386-116">Sie können diese Kette hier herunterladen: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span><span class="sxs-lookup"><span data-stu-id="f5386-116">You can download this chain here: https://support.office.com/article/office-365-certificate-chains-0c03e6b3-e73f-4316-9e2b-bf4091ae96bb</span></span>


    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f5386-117">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="f5386-117">Certificate</span></span></th>
    <th><span data-ttu-id="f5386-118">Zertifikatspeicher</span><span class="sxs-lookup"><span data-stu-id="f5386-118">Certificate Store</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f5386-119">Baltimore CyberTrust Root</span><span class="sxs-lookup"><span data-stu-id="f5386-119">Baltimore CyberTrust Root</span></span></p></td>
    <td><p><span data-ttu-id="f5386-120">Vertrauenswürdige Stammzertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="f5386-120">Trusted Root CA</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f5386-121">Microsoft Internet Authority (Zertifikat einer neuen Zertifizierungsstelle)</span><span class="sxs-lookup"><span data-stu-id="f5386-121">Microsoft Internet Authority (New CA certificate)</span></span></p></td>
    <td><p><span data-ttu-id="f5386-122">Zwischenzertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="f5386-122">Intermediate CA</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f5386-123">MSIT Machine Auth CA2 (neue ausstellende CA2)</span><span class="sxs-lookup"><span data-stu-id="f5386-123">MSIT Machine Auth CA2 (New Issuing CA2)</span></span></p></td>
    <td><p><span data-ttu-id="f5386-124">Zwischenzertifizierungsstelle</span><span class="sxs-lookup"><span data-stu-id="f5386-124">Intermediate CA</span></span></p></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="f5386-125">Aktivieren Sie in Ihrem lokalen Active Directory die betroffenen Benutzerkonten für lync lokal.</span><span class="sxs-lookup"><span data-stu-id="f5386-125">In your on-premises Active Directory, enable the affected user accounts for Lync on-premises.</span></span> <span data-ttu-id="f5386-126">Geben Sie dafür für einen einzelnen Benutzer das folgende Cmdlet ein:</span><span class="sxs-lookup"><span data-stu-id="f5386-126">You can do this for an individual user by typing the following cmdlet:</span></span>
    
        Enable-CsUser
        -Identity "username" 
        -SipAddress "sip: username@contoso.com"
        -HostingProviderProxyFqdn "sipfed.online.lync.com"
    
    <span data-ttu-id="f5386-127">Oder erstellen Sie ein Skript, das Benutzernamen aus einer Datei liest und sie als Eingabe für das Cmdlet „Enable-CsUser“ bereitstellt:</span><span class="sxs-lookup"><span data-stu-id="f5386-127">Or you can create a script that reads user names from a file and provides them as input to the Enable-CsUser cmdlet:</span></span>
    
        Enable-CsUser
        -Identity $Identity 
        -SipAddress $SipAddress 
        -HostingProviderProxyFqdn "sipfed.online.lync.com"

4.  <span data-ttu-id="f5386-128">Führen Sie Dirsync aus, um die lync Online-Benutzer mit den aktualisierten lokalen lync-Benutzern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f5386-128">Run DirSync to sync the Lync Online users with the updated Lync on-premises users.</span></span>

5.  <span data-ttu-id="f5386-129">Aktualisieren Sie einige DNS-Einträge, um den gesamten SIP-Datenverkehr an lync lokal zu leiten:</span><span class="sxs-lookup"><span data-stu-id="f5386-129">Update some DNS records to direct all SIP traffic to Lync on-premises:</span></span>
    
      - <span data-ttu-id="f5386-130">Aktualisieren Sie den Eintrag **lyncdiscover.contoso.com** so, dass er auf den FQDN des lokalen Reverseproxyservers verweist.</span><span class="sxs-lookup"><span data-stu-id="f5386-130">Update the **lyncdiscover.contoso.com** A record to point to the FQDN of the on-premises reverse proxy server.</span></span>
    
      - <span data-ttu-id="f5386-131">Aktualisieren Sie das **_\_ SIP_. \_ TLS.contoso.com** SRV-Eintrag, um die öffentliche IP-oder VIP-Adresse des Access Edge-Diensts von lync lokal zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f5386-131">Update the **_\_sip_.\_tls.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="f5386-132">Aktualisieren Sie das **_\_ sipfederationtls_. \_ TCP.contoso.com** SRV-Eintrag, um die öffentliche IP-oder VIP-Adresse des Access Edge-Diensts von lync lokal zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f5386-132">Update the **_\_sipfederationtls_.\_tcp.contoso.com** SRV record to resolve to the public IP or VIP address of the Access Edge service of Lync on-premises.</span></span>
    
      - <span data-ttu-id="f5386-133">Wenn in Ihrem Unternehmen Split-DNS (manchmal auch als „Split-Brain-DNS“ bezeichnet) verwendet wird, stellen Sie sicher, dass Benutzer, die Namen über die interne DNS-Zone auflösen, an den Front-End-Pool geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f5386-133">If your organization uses split DNS (sometimes called “split-brain DNS”), make sure that users resolving names through the internal DNS zone are directed to the Front End Pool.</span></span>

6.  <span data-ttu-id="f5386-134">Geben `Get-CsUser` Sie das Cmdlet ein, um einige Eigenschaften über die Benutzer zu überprüfen, die Sie verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="f5386-134">Type the `Get-CsUser` cmdlet to check some properties about the users you’ll be moving.</span></span> <span data-ttu-id="f5386-135">Sie möchten sicherstellen, dass die HostingProviderProxyFQDN auf festgelegte `"sipfed.online.lync.com"` und die SIP-Adressen richtig festgesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="f5386-135">You want to make sure that the HostingProviderProxyFQDN is set to `"sipfed.online.lync.com"` and that the SIP addresses are set correctly.</span></span>

7.  <span data-ttu-id="f5386-136">Verschieben Sie lync Online-Benutzer in die lokale lync-app.</span><span class="sxs-lookup"><span data-stu-id="f5386-136">Move Lync Online users to Lync on-premises.</span></span>
    
    <span data-ttu-id="f5386-137">Geben Sie Folgendes ein, um einen einzelnen Benutzer zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="f5386-137">To move a single user, type this:</span></span>
    
       ```PowerShell
       $cred = Get-Credential
       ```
    
       ```PowerShell
       Move-CsUser -Identity <username>@contoso.com -Target "<fe-pool>.contoso.com" -Credential $cred -HostedMigrationOverrideURL <URL>
       ```
    
    <span data-ttu-id="f5386-138">Sie können mehrere Benutzer verschieben, indem Sie das Cmdlet **Get-CsUSer** mit dem Parameter –Filter verwenden, um Benutzer mit einer bestimmten Eigenschaft auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f5386-138">You can move multiple users by using the **Get-CsUSer** cmdlet with the –Filter parameter to select the users with a specific property.</span></span> <span data-ttu-id="f5386-139">So können Sie beispielsweise alle lync Online-Benutzer auswählen, indem Sie für {Hosting Provider – EQ "sipfed.online.lync.om"} filtern.</span><span class="sxs-lookup"><span data-stu-id="f5386-139">For example, you could select all Lync Online users by filtering for {Hosting Provider –eq “sipfed.online.lync.om”}.</span></span> <span data-ttu-id="f5386-140">Sie können dann die zurückgegebenen Benutzer an das Cmdlet **Move-CsUSer** weiterleiten, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5386-140">You can then pipe the returned users to the **Move-CsUSer** cmdlet, as shown below.</span></span>
    
        Get-CsUser -Filter {Hosting Provider -eq "sipfed.online.lync.com"} | Move-CsUser -Target "<fe-pool>.contoso.com" -Credential $creds -HostedMigrationOverrideURL <URL>
    
    <span data-ttu-id="f5386-141">Das Format der für den **HostedMigrationOverrideUrl** -Parameter angegebenen URL muss die URL des Pools sein, in dem der gehostete Migrationsdienst ausgeführt wird, im folgenden Format: *https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc*.</span><span class="sxs-lookup"><span data-stu-id="f5386-141">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format: *Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc*.</span></span>
    
    <span data-ttu-id="f5386-142">Sie können die URL für den gehosteten Migrationsdienst ermitteln, indem Sie die URL für die lync Online-Systemsteuerung für Ihr Microsoft 365-oder Office 365-organisationskonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5386-142">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>
    
    <div>
    
    ## <a name="to-determine-the-hosted-migration-service-url-for-your-organizaton"></a><span data-ttu-id="f5386-143">So ermitteln Sie die URL des gehosteten Migrations Diensts für Ihre organizaton</span><span class="sxs-lookup"><span data-stu-id="f5386-143">To determine the Hosted Migration Service URL for your organizaton</span></span>
    
    1.  <span data-ttu-id="f5386-144">Melden Sie sich bei Ihrer Microsoft 365-oder Office 365-Organisation als Administrator an.</span><span class="sxs-lookup"><span data-stu-id="f5386-144">Log in to your Microsoft 365 or Office 365 organization as an administrator.</span></span>
    
    2.  <span data-ttu-id="f5386-145">Öffnen Sie das **lync Admin Center**.</span><span class="sxs-lookup"><span data-stu-id="f5386-145">Open the **Lync admin center**.</span></span>
    
    3.  <span data-ttu-id="f5386-146">Wenn das **lync Admin Center** angezeigt wird, wählen Sie die URL in der Adressleiste bis zu **lync.com** aus, und kopieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="f5386-146">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="f5386-147">Eine Beispiel-URL sieht ähnlich wie die folgende aus:</span><span class="sxs-lookup"><span data-stu-id="f5386-147">An example URL looks similar to the following:</span></span>
        
        `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`
    
    4.  <span data-ttu-id="f5386-148">Ersetzen Sie **webdir** in der URL durch **admin**, womit Sie folgendes Ergebnis erhalten:</span><span class="sxs-lookup"><span data-stu-id="f5386-148">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
        
        `https://admin0a.online.lync.com`
    
    5.  <span data-ttu-id="f5386-149">Fügen Sie dann folgende Zeichenfolge an die URL an: **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="f5386-149">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
        
        <span data-ttu-id="f5386-150">Die daraus resultierende URL, die dem Wert der **HostedMigrationOverrideUrl** entspricht, sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="f5386-150">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
        
        `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`
    
    </div>
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="f5386-151">Standardmäßig beträgt die maximale Größe für Transaktionsprotokolldateien der rtcxds-Datenbank 16 GB.</span><span class="sxs-lookup"><span data-stu-id="f5386-151">The default maximum size for transaction log files of the rtcxds database is 16 GB.</span></span> <span data-ttu-id="f5386-152">Das ist möglicherweise nicht ausreichend, wenn Sie viele Benutzer auf einmal verschieben, insbesondere wenn das Spiegeln aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5386-152">This might not be big enough if you’re moving a large number of users at once, especially if you have mirroring enabled.</span></span> <span data-ttu-id="f5386-153">Sie können dieses Problem umgehen, indem Sie die Dateigröße erhöhen oder die Protokolldateien regelmäßig sichern.</span><span class="sxs-lookup"><span data-stu-id="f5386-153">To get around this you can increase the file size or back up the log files regularly.</span></span> <span data-ttu-id="f5386-154">Weitere Informationen finden Sie unter <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span><span class="sxs-lookup"><span data-stu-id="f5386-154">For more information, see <A class=uri href="https://support.microsoft.com/kb/2756725">https://support.microsoft.com/kb/2756725</A>.</span></span>

    
    </div>

8.  <span data-ttu-id="f5386-155">Dies ist ein optionaler Schritt.</span><span class="sxs-lookup"><span data-stu-id="f5386-155">This is an optional step.</span></span> <span data-ttu-id="f5386-156">Wenn Sie eine Integration in Exchange 2013 Online benötigen, müssen Sie einen zusätzlichen Hostinganbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5386-156">If you need to integrate with Exchange 2013 Online, you need to use an additional hosting provider.</span></span> <span data-ttu-id="f5386-157">Ausführliche Informationen finden Sie unter [Konfigurieren der lokalen lync Server 2013-Integration in Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="f5386-157">For details, see [Configuring on-premises Lync Server 2013 integration with Exchange Online](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md).</span></span>

9.  <span data-ttu-id="f5386-p110">Die Benutzer sind jetzt verschoben. Geben Sie das folgende Cmdlet ein, um zu überprüfen, ob ein Benutzer korrekte Werte für die in der folgenden Tabelle gezeigten Attribute hat:</span><span class="sxs-lookup"><span data-stu-id="f5386-p110">The users are now moved. To check that a user has correct values for the attributes shown in the following table, type this cmdlet:</span></span>
    
        Get-CsUser | fl DisplayName,HostingProvider,SipAddress,Enabled
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f5386-160">Active Directory-Attribut</span><span class="sxs-lookup"><span data-stu-id="f5386-160">Active Directory attribute</span></span></th>
    <th><span data-ttu-id="f5386-161">Attributname</span><span class="sxs-lookup"><span data-stu-id="f5386-161">Attribute name</span></span></th>
    <th><span data-ttu-id="f5386-162">Korrekter Wert für lync Online-Benutzer</span><span class="sxs-lookup"><span data-stu-id="f5386-162">Correct value for Lync Online user</span></span></th>
    <th><span data-ttu-id="f5386-163">Der richtige Wert für lync-lokal Benutzer</span><span class="sxs-lookup"><span data-stu-id="f5386-163">Correct value for Lync on–premises users</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="f5386-164">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="f5386-164">msRTCSIP-DeploymentLocator</span></span></p></td>
    <td><p><span data-ttu-id="f5386-165">HostingProvider</span><span class="sxs-lookup"><span data-stu-id="f5386-165">HostingProvider</span></span></p></td>
    <td><p><span data-ttu-id="f5386-166">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="f5386-166">sipfed.online.lync.com</span></span></p></td>
    <td><p><span data-ttu-id="f5386-167">SRV:</span><span class="sxs-lookup"><span data-stu-id="f5386-167">SRV:</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="f5386-168">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="f5386-168">msRTCSIP-PrimaryUserAddress</span></span></p></td>
    <td><p><span data-ttu-id="f5386-169">SIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5386-169">SIPAddress</span></span></p></td>
    <td><p><span data-ttu-id="f5386-170">sip:username@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5386-170">sip:userName@contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="f5386-171">sip:username@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f5386-171">sip:userName@contoso.com</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="f5386-172">Attribut msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="f5386-172">msRTCSIP-UserEnabled</span></span></p></td>
    <td><p><span data-ttu-id="f5386-173">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="f5386-173">Enabled</span></span></p></td>
    <td><p><span data-ttu-id="f5386-174">True</span><span class="sxs-lookup"><span data-stu-id="f5386-174">True</span></span></p></td>
    <td><p><span data-ttu-id="f5386-175">Wahr</span><span class="sxs-lookup"><span data-stu-id="f5386-175">True</span></span></p></td>
    </tr>
    </tbody>
    </table>


10. <span data-ttu-id="f5386-176">Jeder Benutzer, der verschoben wurde, muss sich bei lync abmelden und dann wieder anmelden.</span><span class="sxs-lookup"><span data-stu-id="f5386-176">Each user who has been moved will need to log out of Lync, then log back in.</span></span> <span data-ttu-id="f5386-177">Wenn Sie sich anmelden, sollten Sie ihre Kontaktlisten überprüfen und bei Bedarf Kontakte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f5386-177">When they log in they should verify their contact lists, and add contacts if needed.</span></span>
    
    <span data-ttu-id="f5386-178">Beachten Sie, dass geplante Besprechungen nicht von lync online zu lync lokal migriert werden.</span><span class="sxs-lookup"><span data-stu-id="f5386-178">Note that scheduled meetings are not migrated from Lync Online to Lync on-premises.</span></span> <span data-ttu-id="f5386-179">Benutzer müssen diese Besprechungen erneut planen, nachdem sie verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="f5386-179">Users will need to reschedule these meetings after being moved.</span></span>
    
    <span data-ttu-id="f5386-180">Nachdem die DNS-Einträge aktualisiert wurden und alle Benutzer an Premise weitergeleitet werden, weist das Hostinganbieter-Attribut den lync-Benutzer an, entweder SRV-Einträge zu verwenden oder Sie an den Online Anbieter "sipfed.online.lync.com" zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f5386-180">After the DNS records are updated and all users are directed to On premise, the HostingProvider attribute directs the Lync user to either use SRV records or direct them to the Online provider “sipfed.online.lync.com.”</span></span>

<span data-ttu-id="f5386-181"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5386-181"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

