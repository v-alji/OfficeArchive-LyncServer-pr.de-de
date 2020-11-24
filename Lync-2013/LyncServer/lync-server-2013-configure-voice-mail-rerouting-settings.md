---
title: 'Lync Server 2013: Konfigurieren von Einstellungen für die Voicemailumleitung'
description: 'Lync Server 2013: Konfigurieren der Einstellungen für die Umleitung von Voicemail'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure voice mail rerouting settings
ms:assetid: 7ab6be28-eabb-4a79-a796-648887d71b83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398606(v=OCS.15)
ms:contentKeyID: 48184593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 669ea5585f9e732b6a49d9749b8939c14b4e0d9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395231"
---
# <a name="configure-voice-mail-rerouting-settings-in-lync-server-2013"></a><span data-ttu-id="88a8d-103">Konfigurieren von Einstellungen für die Voicemailumleitung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88a8d-103">Configure voice mail rerouting settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88a8d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88a8d-104">

<span> </span></span></span>

<span data-ttu-id="88a8d-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="88a8d-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="88a8d-106">Überlebensfähige Zweigstellen-Appliances und überlebensfähige Verzweigungs Server können bei einem WAN-Ausfall die Überlebensfähigkeit von Sprachnachrichten für Zweig Benutzer gewährleisten, wenn Exchange Unified Messaging (um) auf dem zentralen Standort installiert ist und eine Exchange um-Nachrichten automatische Telefonzentrale (AA) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="88a8d-106">Survivable Branch Appliances and Survivable Branch Servers can provide voice mail survivability for branch users during a WAN outage, if Exchange Unified Messaging (UM) is installed at the central site and an Exchange UM Message Auto Attendant (AA) is deployed.</span></span> <span data-ttu-id="88a8d-107">Wir empfehlen, dass Ihr Exchange-Administrator die AA so konfiguriert, dass nur Nachrichten akzeptiert werden, wodurch andere generische Funktionen wie die Übertragung an einen Benutzer oder die Übertragung an einen Operator deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="88a8d-107">We recommend that your Exchange administrator configure the AA to accept messages only, which disables other generic functionality, such as transfer to a user or transfer to an operator.</span></span> <span data-ttu-id="88a8d-108">Alternativ können Sie eine generische AA-oder AA-Karte verwenden, die für die Weiterleitung des Anrufs angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="88a8d-108">Alternatively, you might use a generic AA or an AA customized to route the call.</span></span>

<span data-ttu-id="88a8d-109">Ausführliche Informationen finden Sie im Abschnitt "Vorbereiten auf die Überlebensfähigkeit von Voicemail" in der Planning-Dokumentation unter Anforderungen an die [Sicherheit von Zweigstellen für lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md) .</span><span class="sxs-lookup"><span data-stu-id="88a8d-109">For details, see the “Preparing for Voice Mail Survivability” section of [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="to-configure-voice-mail-survivability"></a><span data-ttu-id="88a8d-110">So konfigurieren Sie die Überlebensfähigkeit von Voicemail</span><span class="sxs-lookup"><span data-stu-id="88a8d-110">To configure voice mail survivability</span></span>

1.  <span data-ttu-id="88a8d-111">Bitten Sie Ihren Exchange-Administrator, die AA so zu konfigurieren, dass nur Nachrichten akzeptiert werden (in der Exchange-Shell verwenden Sie das folgende Cmdlet: **festlegen-UMAutoAttendant \<AA name\> -CallSomeoneEnabled $false**.</span><span class="sxs-lookup"><span data-stu-id="88a8d-111">Ask your Exchange administrator to configure the AA to accept messages only (in the Exchange Shell use the following cmdlet: **Set-UMAutoAttendant \<AA name\> -CallSomeoneEnabled $false**.</span></span> <span data-ttu-id="88a8d-112">Der Parameter, der angibt, dass das verlassen von Nachrichten (*SendVoiceMsgEnabled*) zulässig ist, ist standardmäßig wahr.</span><span class="sxs-lookup"><span data-stu-id="88a8d-112">The parameter that specifies to allow leaving messages (*SendVoiceMsgEnabled*) is true by default.</span></span>

2.  <span data-ttu-id="88a8d-113">Verwenden Sie in der lync Server-Verwaltungsshell das Cmdlet **New-CSVoiceMailReroutingConfiguration** , um die AA-Telefonnummer als Telefonnummer der Exchange UM-Telefonzentrale in der Konfiguration der Voicemail-Umleitung auf der Survivable Branch-Appliance oder dem Überlebenden Branch-Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="88a8d-113">In the Lync Server Management Shell, use the **New-CSVoiceMailReroutingConfiguration** cmdlet to set the AA phone number as the Exchange UM Auto Attendant phone number in the voice mail rerouting configuration on the Survivable Branch Appliance or Survivable Branch Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88a8d-114">Wenn Sie die Einstellung Voicemail-Umleitung später ändern müssen, verwenden Sie dazu das Cmdlet " <STRONG>Satz-CsVoiceMailReRoutingConfiguration</STRONG> ".</span><span class="sxs-lookup"><span data-stu-id="88a8d-114">If you need to modify the voice mail rerouting setting later, use the <STRONG>Set-CsVoiceMailReRoutingConfiguration</STRONG> cmdlet to do so.</span></span> <span data-ttu-id="88a8d-115">Ausführliche Informationen zu <STRONG>New-</STRONG> und CSVoiceMailReroutingConfiguration finden Sie in den Shell <STRONG>-</STRONG>Hilfethemen.</span><span class="sxs-lookup"><span data-stu-id="88a8d-115">For details, about <STRONG>New-</STRONG> and <STRONG>Set-CSVoiceMailReroutingConfiguration</STRONG>, in the Shell Help topics.</span></span>

    
    </div>

3.  <span data-ttu-id="88a8d-116">Legen Sie die Exchange-um-Teilnehmerzugriffsnummer fest, die dem Exchange um-Wählplan des Zweig Benutzers als die Exchange um-Teilnehmerzugriffsnummer in der Konfiguration der Voicemail-Umleitung auf der Survivable Branch-Appliance oder dem Survivable Branch-Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="88a8d-116">Set the Exchange UM subscriber access number that corresponds to the branch user’s Exchange UM dial plan as the Exchange UM subscriber access number in the voice mail rerouting configuration on the Survivable Branch Appliance or Survivable Branch Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="88a8d-117">Konfigurieren Sie den Wählplan der Exchange um-Benutzer so, dass nur ein Wählplan für alle Verzweigungs Benutzer vorgesehen ist, die während eines WAN-Ausfalls Zugriff auf die Funktion "Voicemail erhalten" benötigen.</span><span class="sxs-lookup"><span data-stu-id="88a8d-117">Configure the Exchange UM users’ dial plan so that there is only one dial plan associated with all branch users who need access to the Get Voice Mail functionality during a WAN outage.</span></span>

    
    </div>

<span data-ttu-id="88a8d-118">**Nächster Schritt** für Survivor-Branch-Appliances oder Survivable Branch-Server: [Privatbenutzer auf einer Survivable Branch-Appliance oder einem Server in lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="88a8d-118">**Next step** for Survivable Branch Appliances or Survivable Branch Servers: [Home users on a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-home-users-on-a-survivable-branch-appliance-or-server.md).</span></span>

<span data-ttu-id="88a8d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88a8d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

