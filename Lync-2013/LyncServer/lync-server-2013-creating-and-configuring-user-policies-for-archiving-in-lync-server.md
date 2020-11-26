---
title: Erstellen und Konfigurieren von Benutzerrichtlinien für die Archivierung in lync Server
description: Erstellen und Konfigurieren von Benutzerrichtlinien für die Archivierung in lync Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating and configuring user policies for Archiving in Lync Server
ms:assetid: 5af0e605-3563-4d6f-a3c6-511d204a3165
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204923(v=OCS.15)
ms:contentKeyID: 48184234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dad260910f01e10c71dbbde67af98ea9a207e33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431540"
---
# <a name="creating-and-configuring-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="ffd53-103">Erstellen und Konfigurieren von Benutzerrichtlinien für die Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffd53-103">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffd53-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffd53-104">

<span> </span></span></span>

<span data-ttu-id="ffd53-105">_**Letztes Änderungsdatum des Themas:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="ffd53-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="ffd53-106">Um die Archivierung für bestimmte Benutzer zu aktivieren oder zu deaktivieren, die sich auf lync Server befinden, müssen Sie zuerst eine Benutzerrichtlinie erstellen und dann die Richtlinie auf einen oder mehrere Benutzer oder Benutzergruppen anwenden.</span><span class="sxs-lookup"><span data-stu-id="ffd53-106">To enable or disable Archiving for specific users homed on Lync Server, you must first create a user policy and then apply the policy to one or more users or user groups.</span></span> <span data-ttu-id="ffd53-107">Ausführliche Informationen zum Anwenden von Benutzerrichtlinien auf bestimmte Benutzer und Benutzergruppen finden Sie unter [Anwenden einer lync Server-Archivierungsrichtlinie auf einen Benutzer in lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ffd53-107">For details about applying user policies to specific users and user groups, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="ffd53-108">Ausführliche Informationen zur Funktionsweise von Archivierungsrichtlinien, einschließlich der Hierarchie für Global-, Website-und Benutzerrichtlinien, finden Sie unter [Funktionsweise der Archivierung in lync Server 2013](lync-server-2013-how-archiving-works.md) in der Planungsdokumentation, in der Bereitstellungsdokumentation oder in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ffd53-108">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, in the Deployment documentation, or in the Operations documentation.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="ffd53-109">Wenn Sie die Microsoft Exchange-Integration für Ihre Bereitstellung aktiviert haben, Steuern Exchange-In-Place Speicherrichtlinien, ob die Archivierung für die Benutzer aktiviert ist, die sich in Exchange 2013 befinden, und die Postfächer In-Place halten.</span><span class="sxs-lookup"><span data-stu-id="ffd53-109">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="ffd53-110">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ffd53-110">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="ffd53-111">Sie sollten alle geeigneten Optionen in den Archivierungs Konfigurationen angeben, bevor Sie die Archivierung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ffd53-111">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="ffd53-112">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configuring-archiving-options.md">Konfigurieren von Archivierungsoptionen in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ffd53-112">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-configure-an-archiving-policy-for-users-homed-on-lync-server"></a><span data-ttu-id="ffd53-113">So konfigurieren Sie eine Archivierungsrichtlinie für Benutzer, die auf lync Server verwaltet werden</span><span class="sxs-lookup"><span data-stu-id="ffd53-113">To configure an archiving policy for users homed on Lync Server</span></span>

1.  <span data-ttu-id="ffd53-114">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsArchivingAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ffd53-114">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ffd53-115">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server 2013-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffd53-115">Open a browser window, and then enter the Admin URL to open the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="ffd53-116">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server 2013-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ffd53-116">For details about the different methods that you can use to start Lync Server 2013 Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ffd53-117">Klicken Sie auf der linken Navigationsleiste auf **Überwachung und Archivierung** und anschließend auf **Archivierungsrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="ffd53-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="ffd53-118">Klicken Sie auf **Neu** und anschließend auf **Benutzerrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="ffd53-118">Click **New**, and then click **User policy**.</span></span>

5.  <span data-ttu-id="ffd53-119">Führen Sie unter **Neue Archivierungsrichtlinie** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="ffd53-119">In **New Archiving Policy**, do the following:</span></span>
    
      - <span data-ttu-id="ffd53-120">Geben Sie im Feld **Name** den Namen der Benutzerrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="ffd53-120">In **Name**, specify the name for the user policy.</span></span>
    
      - <span data-ttu-id="ffd53-121">Machen Sie im Feld **Beschreibung** nähere Angaben zur Art der Benutzerrichtlinie (z. B. Benutzerrichtlinie für die Rechtsabteilung).</span><span class="sxs-lookup"><span data-stu-id="ffd53-121">In **Description**, provide information about what the user policy is (for example, user policy for legal department).</span></span>
    
      - <span data-ttu-id="ffd53-122">Um die Archivierung der internen Kommunikation für die Benutzerrichtlinie zu kontrollieren, aktivieren oder deaktivieren Sie das Kontrollkästchen **Interne Kommunikation archivieren**.</span><span class="sxs-lookup"><span data-stu-id="ffd53-122">To control archiving of internal communications for the user policy, select or clear the **Archive internal communications** check box.</span></span>
    
      - <span data-ttu-id="ffd53-123">Um die Archivierung der externen Kommunikation für die Benutzerrichtlinie zu kontrollieren, aktivieren oder deaktivieren Sie das Kontrollkästchen **Externe Kommunikation archivieren**.</span><span class="sxs-lookup"><span data-stu-id="ffd53-123">To control archiving of external communications for the user policy, select or clear the **Archive external communications** check box.</span></span>

6.  <span data-ttu-id="ffd53-124">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ffd53-124">Click **Commit**.</span></span>

<span data-ttu-id="ffd53-125">Benutzerrichtlinien wirken sich nur auf Benutzer aus, denen eine solche Richtlinie zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ffd53-125">A user policy applies only to users to whom you assign the policy.</span></span> <span data-ttu-id="ffd53-126">Ausführliche Informationen zum Anwenden einer Benutzerrichtlinie auf bestimmte Benutzer finden Sie unter [Anwenden einer lync Server-Archivierungsrichtlinie auf einen Benutzer in lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ffd53-126">For details about applying a user policy to specific users, see [Applying a Lync Server Archiving policy to a user in Lync Server 2013](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md) in the Deployment documentation.</span></span>

<span data-ttu-id="ffd53-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffd53-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

