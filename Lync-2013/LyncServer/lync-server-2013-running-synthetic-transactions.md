---
title: 'Lync Server 2013: Ausführen synthetischer Transaktionen'
description: 'Lync Server 2013: Ausführen synthetischer Transaktionen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running synthetic transactions
ms:assetid: 2b56c7bd-8956-4fa1-8232-1876b959b258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720911(v=OCS.15)
ms:contentKeyID: 63969593
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26b0c26024f361dac196319eaf849c1847033cc9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442180"
---
# <a name="running-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="aadb2-103">Ausführen synthetischer Transaktionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aadb2-103">Running synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aadb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aadb2-104">

<span> </span></span></span>

<span data-ttu-id="aadb2-105">_**Letztes Änderungsdatum des Themas:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="aadb2-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="aadb2-106">Synthetische Transaktionen werden in der Regel auf zwei Arten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="aadb2-106">Synthetic transactions are typically conducted in two ways.</span></span> <span data-ttu-id="aadb2-107">Sie können die CsHealthMonitoringConfiguration-Cmdlets verwenden, um Testbenutzer für die einzelnen registrierungspools einzurichten.</span><span class="sxs-lookup"><span data-stu-id="aadb2-107">You can use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="aadb2-108">Bei diesen Testbenutzern handelt es sich um ein paar Benutzer, die für die Verwendung mit synthetischen Transaktionen vorkonfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="aadb2-108">These test users are a pair of users who were preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="aadb2-109">(In der Regel handelt es sich hierbei um Testkonten und nicht um Konten, die tatsächlichen Benutzern gehören.) Bei Testbenutzern, die für einen Pool konfiguriert sind, können Sie eine synthetische Transaktion für diesen Pool ausführen, ohne die Identitäten (und die Anmeldeinformationen für) der am Test beteiligten Benutzerkonten angeben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="aadb2-109">(Typically these are test accounts and not accounts that belong to actual users.) With test users configured for a pool, you can run a synthetic transaction against that pool without having to specify the identities of (and supply the credentials for) the user accounts involved in the test.</span></span>

<span data-ttu-id="aadb2-110">Oder Sie können eine synthetische Transaktion unter Verwendung tatsächlicher Benutzerkonten ausführen.</span><span class="sxs-lookup"><span data-stu-id="aadb2-110">Or, you can run a synthetic transaction by using actual user accounts.</span></span> <span data-ttu-id="aadb2-111">Wenn beispielsweise zwei Benutzer keine Chatnachrichten austauschen können, können Sie eine synthetische Transaktion unter Verwendung dieser beiden Benutzerkonten (anstelle eines Paars von Testkonten) ausführen und dann versuchen, das Problem zu diagnostizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="aadb2-111">For example, if two users cannot exchange instant messages, you could run a synthetic transaction using those two user accounts (instead of a pair of test accounts), and then try to diagnose and resolve the issue.</span></span> <span data-ttu-id="aadb2-112">Wenn Sie sich entscheiden, eine synthetische Transaktion mit tatsächlichen Benutzerkonten durchzuführen, müssen Sie die Anmeldenamen und Kennwörter für jeden Benutzer angeben.</span><span class="sxs-lookup"><span data-stu-id="aadb2-112">If you decide to conduct a synthetic transaction using actual user accounts, you must supply the logon names and passwords for each user.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="aadb2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aadb2-113">See Also</span></span>


[<span data-ttu-id="aadb2-114">Konfigurieren von Watcher-Knotentest Benutzern und Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aadb2-114">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>](lync-server-2013-configuring-watcher-node-test-users-and-configuration-settings.md)  
[<span data-ttu-id="aadb2-115">Spezielle Einrichtungsanweisungen für synthetische Transaktionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aadb2-115">Special setup instructions for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md)  
  

<span data-ttu-id="aadb2-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aadb2-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

