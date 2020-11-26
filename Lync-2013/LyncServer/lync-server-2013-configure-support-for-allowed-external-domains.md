---
title: 'Lync Server 2013: Konfigurieren der Unterstützung für zulässige externe Domänen'
description: 'Lync Server 2013: Konfigurieren der Unterstützung für zugelassene externe Domänen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure support for allowed external domains
ms:assetid: 3ee6e175-986d-4c33-b03a-b9f93083dca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425908(v=OCS.15)
ms:contentKeyID: 48183943
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13845638bca8791d43b8644c5dcb30ec73751a5b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433682"
---
# <a name="configure-support-for-allowed-external-domains-in-lync-server-2013"></a><span data-ttu-id="25c55-103">Konfigurieren der Unterstützung für zulässige externe Domänen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25c55-103">Configure support for allowed external domains in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25c55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25c55-104">

<span> </span></span></span>

<span data-ttu-id="25c55-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="25c55-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="25c55-106">Wenn Sie die Unterstützung für Federated-Partner konfiguriert haben, können Sie verwalten, welche bestimmten Domänen mit Ihrer Organisation verbunden werden können.</span><span class="sxs-lookup"><span data-stu-id="25c55-106">If you have configured support for federated partners, you can manage which specific domains can federate with your organization.</span></span> <span data-ttu-id="25c55-107">Sie konfigurieren eine oder mehrere bestimmte externe Domänen als zugelassene Verbunddomänen.</span><span class="sxs-lookup"><span data-stu-id="25c55-107">You configure one or more specific external domains as allowed federated domains.</span></span> <span data-ttu-id="25c55-108">Fügen Sie dazu jede Domäne zur Liste der zulässigen Domänen hinzu.</span><span class="sxs-lookup"><span data-stu-id="25c55-108">To do this, add each domain to the list of allowed domains.</span></span> <span data-ttu-id="25c55-109">Auch wenn die Partner Ermittlung für Ihre Organisation aktiviert ist, gehen Sie wie folgt vor, wenn es sich bei der Domäne um einen Verbundpartner handelt, der möglicherweise mit mehr als 1.000 ihrer Benutzer kommunizieren muss, oder wenn Sie möglicherweise mehr als 20 Nachrichten pro Sekunde senden müssen.</span><span class="sxs-lookup"><span data-stu-id="25c55-109">Even if partner discovery is enabled for your organization, do this if the domain is a federated partner that might need to communicate with more than 1,000 of your users or might need to send more than 20 messages per second.</span></span> <span data-ttu-id="25c55-110">Wenn die Partner Ermittlung für Ihre Organisation nicht aktiviert ist, können nur Benutzer externer Domänen, die Sie der Liste zugelassene Domänen hinzufügen, an Chats und Konferenzen mit Benutzern in Ihrer Organisation teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="25c55-110">If partner discovery is not enabled for your organization, only users of external domains that you add to the allowed domains list can participate in IM and conferencing with users in your organization.</span></span> <span data-ttu-id="25c55-111">Wenn Sie den Zugriff auf eine Verbunddomäne auf einen bestimmten Server einschränken möchten, auf dem der Access-Edgedienst des Verbundpartners ausgeführt wird, können Sie den Domänennamen des Servers angeben, auf dem der Access Edge-Dienst für jede Domäne in der Liste der zulässigen Domänen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25c55-111">If you want to restrict access for a federated domain to a specific server running the Access Edge service of the federated partner, you can specify the domain name of the server running the Access Edge service for each domain in the list of allowed domains.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="25c55-112">In diesem Verfahren wird beschrieben, wie Sie die Unterstützung für bestimmte Domänen konfigurieren, aber die Implementierung der Unterstützung für Verbundbenutzer erfordert auch, dass Sie die Unterstützung für Verbundbenutzer für Ihre Organisation aktivieren und Richtlinien konfigurieren und anwenden, um zu steuern, welche Benutzer mit Verbundbenutzern zusammenarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="25c55-112">This procedure describes how to configure support for specific domains, but implementing support for federated users also requires that you enable support for federated users for your organization, and configure and apply policies to control which users can collaborate with federated users.</span></span> <span data-ttu-id="25c55-113">Details zum Aktivieren der Unterstützung für Verbundbenutzer finden Sie unter <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Aktivieren oder Deaktivieren des Remotebenutzerzugriffs in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="25c55-113">For details about enabling support for federated users, see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span> <span data-ttu-id="25c55-114">Details zum Konfigurieren von Richtlinien für die Steuerung der Föderation finden Sie unter <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Konfigurieren von Richtlinien zum Steuern des Zugriffs von Verbundbenutzern in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="25c55-114">For details about configuring policies to control federation, see <A href="lync-server-2013-configure-policies-to-control-federated-user-access.md">Configure policies to control federated user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-add-an-external-domain-to-the-list-of-allowed-domains"></a><span data-ttu-id="25c55-115">So fügen Sie eine externe Domäne zur Liste der zulässigen Domänen hinzu</span><span class="sxs-lookup"><span data-stu-id="25c55-115">To add an external domain to the list of allowed domains</span></span>

1.  <span data-ttu-id="25c55-116">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="25c55-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="25c55-117">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25c55-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="25c55-118">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="25c55-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="25c55-119">Klicken Sie in der linken Navigationsleiste auf **externer Benutzer Zugriff**, und klicken Sie dann auf **Föderationsdomänen**.</span><span class="sxs-lookup"><span data-stu-id="25c55-119">In the left navigation bar, click **External User Access**, and then click **Federated Domains**.</span></span>

4.  <span data-ttu-id="25c55-120">Klicken Sie auf der Seite **Federated Domains** auf **neu** und dann auf **zugelassene Domäne**.</span><span class="sxs-lookup"><span data-stu-id="25c55-120">On the **Federated Domains** page, click **New**, and then click **Allowed domain**.</span></span>

5.  <span data-ttu-id="25c55-121">Führen Sie in **neuen Föderationsdomänen** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="25c55-121">In **New Federated Domains**, do the following:</span></span>
    
      - <span data-ttu-id="25c55-122">Geben Sie in **Domänenname (oder FQDN)** den Namen der Föderationspartner-Domäne ein.</span><span class="sxs-lookup"><span data-stu-id="25c55-122">In **Domain name (or FQDN)**, type the name of the federated partner domain.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="25c55-123">Dieser Name muss eindeutig sein und kann nicht bereits als zulässige Domäne für diesen Server mit dem Access Edge-Dienst vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="25c55-123">This name must be unique and cannot already exist as an allowed domain for this server running the Access Edge service.</span></span> <span data-ttu-id="25c55-124">Der Name darf nicht mehr als 256 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="25c55-124">The name cannot exceed 256 characters in length.</span></span><BR><span data-ttu-id="25c55-125">Bei der Suche nach dem Domänennamen des Partner Partners wird eine Übereinstimmung mit dem Suffix ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25c55-125">The search on the federated partner domain name performs a suffix match.</span></span> <span data-ttu-id="25c55-126">Wenn Sie beispielsweise <STRONG>contoso.com</STRONG>eingeben, gibt die Suche auch die Domäne <STRONG>IT.contoso.com</STRONG>zurück.</span><span class="sxs-lookup"><span data-stu-id="25c55-126">For example, if you type <STRONG>contoso.com</STRONG>, the search will also return the domain <STRONG>it.contoso.com</STRONG>.</span></span><BR><span data-ttu-id="25c55-127">Eine Föderationspartner-Domäne kann nicht gleichzeitig blockiert und zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="25c55-127">A federated partner domain cannot simultaneously be blocked and allowed.</span></span> <span data-ttu-id="25c55-128">Lync Server 2013 verhindert, dass dies geschieht, damit Sie Ihre Listen nicht synchronisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="25c55-128">Lync Server 2013 prevents this from happening so that you do not have to synch up your lists.</span></span>

        
        </div>
    
      - <span data-ttu-id="25c55-129">Wenn Sie den Zugriff auf Diese Verbunddomäne auf Benutzer eines bestimmten Servers einschränken möchten, auf dem der Access Edge-Dienst ausgeführt wird, geben Sie in **Access Edge Service (FQDN)** den FQDN des Servers der Verbunddomäne ein, auf dem der Access Edge-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25c55-129">If you want to restrict access for this federated domain to users of a specific server running the Access Edge service, in **Access Edge service (FQDN)**, type the FQDN of the federated domain’s server running the Access Edge service.</span></span>
    
      - <span data-ttu-id="25c55-130">Wenn Sie zusätzliche Informationen angeben möchten, geben Sie in **Kommentar** Informationen ein, die Sie für andere Systemadministratoren über diese Konfiguration freigeben möchten.</span><span class="sxs-lookup"><span data-stu-id="25c55-130">If you want to provide additional information, in **Comment**, type information that you want to share with other system administrators about this configuration.</span></span>

6.  <span data-ttu-id="25c55-131">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="25c55-131">Click **Commit**.</span></span>

7.  <span data-ttu-id="25c55-132">Wiederholen Sie die Schritte 4 bis 6 für jede Federated-Partner-Domäne, die Sie zulassen möchten.</span><span class="sxs-lookup"><span data-stu-id="25c55-132">Repeat steps 4 through 6 for each federated partner domain that you want to allow.</span></span>

<span data-ttu-id="25c55-133">Zum Aktivieren des Zugriffs auf den Verbundbenutzer müssen Sie auch die Unterstützung für den Verbundbenutzer Zugriff in Ihrer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="25c55-133">To enable federated user access, you must also enable support for federated user access in your organization.</span></span> <span data-ttu-id="25c55-134">Ausführliche Informationen finden Sie unter [Aktivieren oder Deaktivieren des Remotebenutzerzugriffs in lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="25c55-134">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

<span data-ttu-id="25c55-135">Darüber hinaus müssen Sie die Richtlinie für Benutzer konfigurieren und anwenden, die in der Lage sein sollen, mit Verbundbenutzern zusammenzuarbeiten.</span><span class="sxs-lookup"><span data-stu-id="25c55-135">Additionally, you must configure and apply the policy to users that you want to be able to collaborate with federated users.</span></span> <span data-ttu-id="25c55-136">Ausführliche Informationen finden Sie unter [Konfigurieren von Richtlinien zum Steuern des Zugriffs von Verbundbenutzern in lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="25c55-136">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md).</span></span>

<span data-ttu-id="25c55-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25c55-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

