---
title: 'Lync Server 2013: Verwalten von Benutzern in einer hybridbereitstellung'
description: 'Lync Server 2013: Verwalten von Benutzern in einer hybridbereitstellung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393866"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a><span data-ttu-id="152d5-103">Verwalten von Benutzern in einer hybriden lync Server 2013-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="152d5-103">Administering users in a hybrid Lync Server 2013 deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="152d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="152d5-104">

<span> </span></span></span>

<span data-ttu-id="152d5-105">_**Letztes Änderungsdatum des Themas:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="152d5-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="152d5-106">Sie können Benutzereinstellungen und Richtlinien für Benutzer verwalten, die nach lync Online migriert wurden, indem Sie die Benutzer Verwaltungsfeatures verwenden, die im Microsoft 365 Admin Center zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="152d5-106">You can manage user settings and policies for users migrated to Lync Online by using the User Management features available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="152d5-107">Zum Ausführen von Verwaltungsaufgaben müssen Sie sich mit Ihrem Mandantenadministratorkonto anmelden.</span><span class="sxs-lookup"><span data-stu-id="152d5-107">You must sign in by using your tenant administrator account to perform administration tasks.</span></span>

<div>

## <a name="moving-users-back-to-on-premises"></a><span data-ttu-id="152d5-108">Verschieben von Benutzern zurück in den lokalen Standort</span><span class="sxs-lookup"><span data-stu-id="152d5-108">Moving Users Back to On-premises</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="152d5-109">Dieser Abschnitt gilt nur für Benutzer, die für lync lokal erstellt und aktiviert wurden und dann von einer lokalen Bereitstellung zu lync Online verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="152d5-109">This section applies only to users that were created and enabled for Lync on-premises and then moved from an on-premises deployment to Lync Online.</span></span> <span data-ttu-id="152d5-110">Wenn Sie Benutzer verschieben möchten, die in lync online erstellt wurden (und in einer lokalen Bereitstellung nicht immer für lync aktiviert wurden), lesen Sie verschieben <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">von Benutzern aus lync Online in lync lokal in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="152d5-110">If you want to move users that were created in Lync Online (and not ever enabled for Lync in an on-premises deployment) see, <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

  - <span data-ttu-id="152d5-111">Führen Sie die folgenden Cmdlets aus, um einen Benutzer aus lync Online zurück in lync lokal zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="152d5-111">Run the following cmdlets to move a user from Lync Online back to Lync on-premises:</span></span>
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

<span data-ttu-id="152d5-112">Das Format der für den Parameter **HostedMigrationOverrideUrl** angegebenen URL muss die URL zum Pool sein, in dem der gehostete Migrationsdienst ausgeführt wird, und muss folgendes Format haben:</span><span class="sxs-lookup"><span data-stu-id="152d5-112">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format:</span></span>

<span data-ttu-id="152d5-113"> Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc.</span><span class="sxs-lookup"><span data-stu-id="152d5-113">Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span> <span data-ttu-id="152d5-114">Sie können die URL für den gehosteten Migrationsdienst ermitteln, indem Sie die URL für die lync Online-Systemsteuerung für Ihr Microsoft 365-oder Office 365-organisationskonto anzeigen.</span><span class="sxs-lookup"><span data-stu-id="152d5-114">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="152d5-115">**So ermitteln Sie die URL des gehosteten Migrations Diensts für Ihre Microsoft 365-oder Office 365-Organisation**</span><span class="sxs-lookup"><span data-stu-id="152d5-115">**To determine the Hosted Migration Service URL for your Microsoft 365 or Office 365 organization**</span></span>

1.  <span data-ttu-id="152d5-116">Melden Sie sich als Administrator bei Ihrer Organisation an.</span><span class="sxs-lookup"><span data-stu-id="152d5-116">Log in to your organization as an administrator.</span></span>

2.  <span data-ttu-id="152d5-117">Öffnen Sie das **lync Admin Center**.</span><span class="sxs-lookup"><span data-stu-id="152d5-117">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="152d5-118">Wenn das **lync Admin Center** angezeigt wird, wählen Sie die URL in der Adressleiste bis zu **lync.com** aus, und kopieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="152d5-118">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="152d5-119">Eine Beispiel-URL sieht ähnlich wie die folgende aus:</span><span class="sxs-lookup"><span data-stu-id="152d5-119">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="152d5-120">Ersetzen Sie **webdir** in der URL durch **admin**, womit Sie folgendes Ergebnis erhalten:</span><span class="sxs-lookup"><span data-stu-id="152d5-120">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="152d5-121">Fügen Sie dann folgende Zeichenfolge an die URL an: **/HostedMigration/hostedmigrationservice.svc**.</span><span class="sxs-lookup"><span data-stu-id="152d5-121">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="152d5-122">Die daraus resultierende URL, die dem Wert der **HostedMigrationOverrideUrl** entspricht, sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="152d5-122">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

<span data-ttu-id="152d5-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="152d5-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

