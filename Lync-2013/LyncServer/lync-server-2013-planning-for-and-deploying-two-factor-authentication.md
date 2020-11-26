---
title: 'Lync Server 2013: Planen und Bereitstellen der zweistufigen Authentifizierung'
description: 'Lync Server 2013: Planen und Bereitstellen der zweistufigen Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for and deploying two-factor authentication
ms:assetid: 442a88df-ebc2-4335-9c59-0ce1adc1471e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308563(v=OCS.15)
ms:contentKeyID: 54973686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1e04fa7a0c1184152328882a7c7b4bea8e42ec0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437119"
---
# <a name="two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="22bd5-103">Zweistufige Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22bd5-103">Two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22bd5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22bd5-104">

<span> </span></span></span>

<span data-ttu-id="22bd5-105">_**Letztes Änderungsdatum des Themas:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="22bd5-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="22bd5-106">Die zweistufige Authentifizierung bietet verbesserte Sicherheit, da Benutzer zwei Authentifizierungskriterien erfüllen müssen: eine Kombination aus Benutzername und Kennwort sowie ein Token oder Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="22bd5-106">Two-factor authentication provides improved security by requiring users to meet two authentication criteria: a user name/password combination and a token or certificate.</span></span> <span data-ttu-id="22bd5-107">Dies wird auch als „etwas, das du hast, und etwas, das du weißt“ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="22bd5-107">This is also known as “something you have, something you know.”</span></span> <span data-ttu-id="22bd5-108">Ein typisches Beispiel für eine zweistufige Authentifizierung ist die Nutzung von Smartcards.</span><span class="sxs-lookup"><span data-stu-id="22bd5-108">A typical example of two-factor authentication with a certificate is the use of smart cards.</span></span> <span data-ttu-id="22bd5-109">Eine Smartcard enthält ein Zertifikat, das einem Benutzerkonto zugewiesen ist und welches mit den Benutzer- und Zertifikatinformationen überprüft werden kann, die auf einem Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="22bd5-109">A smart card contains a certificate associated with the user account, and can be validated against user and certificate information stored on a server.</span></span> <span data-ttu-id="22bd5-110">Durch Abgleichen der Benutzerinformationen (Benutzername und Kennwort) mit dem bereitgestellten Zertifikat überprüft der Server die Anmeldeinformationen, sodass er den Benutzer authentifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="22bd5-110">By comparing the user information (user name and password) to the certificate provided, the server validates the credentials and authenticates the user.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="22bd5-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="22bd5-111">In This Section</span></span>

[<span data-ttu-id="22bd5-112">Planen der zweistufigen Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22bd5-112">Planning for two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-planning-for-two-factor-authentication.md)

[<span data-ttu-id="22bd5-113">Konfigurieren der zweistufigen Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22bd5-113">Configuring two-factor authentication in Lync Server 2013</span></span>](lync-server-2013-configuring-two-factor-authentication.md)

[<span data-ttu-id="22bd5-114">Verwenden der zweistufigen Authentifizierung mit lync-Client und lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22bd5-114">Using two-factor authentication with Lync client and Lync Server 2013</span></span>](lync-server-2013-using-two-factor-authentication-with-lync-client.md)

<span data-ttu-id="22bd5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22bd5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

