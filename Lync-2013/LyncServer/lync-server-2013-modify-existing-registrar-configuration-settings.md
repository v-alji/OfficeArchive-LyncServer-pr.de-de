---
title: 'Lync Server 2013: Ändern vorhandener Registrierungs Konfigurationseinstellungen'
description: 'Lync Server 2013: Ändern vorhandener Registrierungs Konfigurationseinstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify existing Registrar configuration settings
ms:assetid: a8931511-3e66-49ed-a3ec-03bcd61ce1f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182566(v=OCS.15)
ms:contentKeyID: 48185095
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a4a58a73ec67a320a9d9ee9a29b8e0a4708aa40a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425479"
---
# <a name="modify-existing-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="bf106-103">Ändern vorhandener Registrierungs Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf106-103">Modify existing Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf106-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf106-104">

<span> </span></span></span>

<span data-ttu-id="bf106-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bf106-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bf106-106">Mithilfe der Registrierungsstelle können Sie Protokolle für die Proxyserverauthentifizierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bf106-106">You can use the Registrar to configure proxy server authentication protocols.</span></span> <span data-ttu-id="bf106-107">Informationen zu den verfügbaren Protokollen finden Sie unter Erstellen von Registrierungsstellen- [Konfigurationseinstellungen in lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="bf106-107">For information about the available protocols, see [Create Registrar configuration settings in Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bf106-p102">Es wird empfohlen, sowohl Kerberos als auch NTLM zu aktivieren, wenn ein Server die Authentifizierung von Remote- und Unternehmensclients unterstützt. Durch eine Kommunikation des Edgeservers mit den internen Servern wird gewährleistet, dass Remoteclients nur die NTLM-Authentifizierung verwenden können. Wenn auf diesen Servern nur Kerberos verwendet wird, ist eine Authentifizierung von Remotebenutzern nicht möglich. Wenn Unternehmensbenutzer sich ebenfalls über den Server authentifizieren, wird Kerberos verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf106-p102">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span>



</div>

<span data-ttu-id="bf106-112">Führen Sie die folgenden Schritte aus, um eine vorhandene Registrierungsstelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bf106-112">Follow these steps to modify an existing Registrar.</span></span>

<div>

## <a name="to-modify-existing-registrar-configuration-settings"></a><span data-ttu-id="bf106-113">So ändern Sie vorhandene Registrierungsstellenkonfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="bf106-113">To modify existing registrar configuration settings</span></span>

1.  <span data-ttu-id="bf106-114">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="bf106-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="bf106-115">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf106-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bf106-116">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bf106-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bf106-117">Klicken Sie in der linken Navigationsleiste auf **Sicherheit** und dann auf **Registrierungsstelle**.</span><span class="sxs-lookup"><span data-stu-id="bf106-117">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="bf106-118">Klicken Sie auf der Seite **Registrierungsstelle** auf einen Dienst, klicken Sie auf **Bearbeiten** und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="bf106-118">On the **Registrar** page, click a service, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="bf106-119">Wählen Sie im Abschnitt **Registrierungsstelleneinstellung bearbeiten** je nach Funktionen der Clients und der Unterstützung in Ihrer Umgebung eine oder mehrere der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="bf106-119">In **Edit Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="bf106-120">**Kerberos-Authentifizierung aktivieren**: Die Server im Pool stellen Authentifizierungsaufforderungen mithilfe der Kerberos-Authentifizierung aus.</span><span class="sxs-lookup"><span data-stu-id="bf106-120">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="bf106-121">**NTLM-Authentifizierung aktivieren**: Die Server im Pool stellen Authentifizierungsaufforderungen mithilfe von NTLM aus.</span><span class="sxs-lookup"><span data-stu-id="bf106-121">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="bf106-122">**Zertifikatauthentifizierung aktivieren**: Die Server im Pool stellen Zertifikate an Clients aus.</span><span class="sxs-lookup"><span data-stu-id="bf106-122">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

6.  <span data-ttu-id="bf106-123">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="bf106-123">Click **Commit**.</span></span>

<span data-ttu-id="bf106-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf106-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

