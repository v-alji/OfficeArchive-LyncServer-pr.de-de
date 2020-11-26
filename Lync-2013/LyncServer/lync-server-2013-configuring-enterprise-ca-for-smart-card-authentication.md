---
title: 'Lync Server 2013: Konfigurieren der Unternehmenszertifizierungsstelle für die Smartcard-Authentifizierung'
description: 'Lync Server 2013: Konfigurieren der Unternehmenszertifizierungsstelle für die Smartcard-Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433150"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="1fb39-103">Konfigurieren der Unternehmenszertifizierungsstelle für die Smartcard-Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1fb39-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1fb39-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1fb39-104">

<span> </span></span></span>

<span data-ttu-id="1fb39-105">_**Letztes Änderungsdatum des Themas:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="1fb39-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="1fb39-106">Im folgenden Abschnitt wird beschrieben, wie Sie eine Unternehmensstammzertifizierungsstelle konfigurieren, um die Smartcard-Authentifizierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1fb39-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="1fb39-107">Informationen zum Installieren einer Unternehmensstammzertifizierungsstelle finden Sie unter Installieren einer Unternehmensstammzertifizierungsstelle unter [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) .</span><span class="sxs-lookup"><span data-stu-id="1fb39-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="1fb39-108">Konfigurieren einer Unternehmensstammzertifizierungsstelle zur Unterstützung der Smartcard-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="1fb39-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="1fb39-109">In den folgenden Schritten wird das Konfigurieren einer Stammzertifizierungsstelle im Unternehmen zur Unterstützung der SmartCard-Authentifizierung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1fb39-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="1fb39-110">Melden Sie sich beim CA-Computer des Unternehmens mit dem Konto eines Domänenadministrators an.</span><span class="sxs-lookup"><span data-stu-id="1fb39-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="1fb39-111">Starten Sie den System-Manager und überprüfen Sie, ob die Zertifizierungsstellen-Webregistrierungsrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fb39-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="1fb39-112">Öffnen Sie im Menü **Verwaltungstools** die Verwaltungskonsole **Zertifizierungsstelle**.</span><span class="sxs-lookup"><span data-stu-id="1fb39-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="1fb39-113">Erweitern Sie im Navigationsbereich den Knoten **Zertifizierungsstelle**.</span><span class="sxs-lookup"><span data-stu-id="1fb39-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="1fb39-114">Klicken Sie mit der rechten Maustaste auf **Zertifikatvorlagen**, wählen Sie **Neu** und anschließend **Auszustellende Zertifikatvorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="1fb39-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="1fb39-115">Wählen Sie **Enrollment Agent**, **SmartCard-Benutzer** und **SmartCard-Anmeldung** aus.</span><span class="sxs-lookup"><span data-stu-id="1fb39-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="1fb39-116">Klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1fb39-116">Click **OK**.</span></span>

8.  <span data-ttu-id="1fb39-117">Klicken Sie mit der rechten Maustaste auf **Zertifikatvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="1fb39-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="1fb39-118">Wählen Sie **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="1fb39-118">Select **Manage**.</span></span>

10. <span data-ttu-id="1fb39-119">Öffnen Sie die Eigenschaften der Vorlage „SmartCard-Benutzer“.</span><span class="sxs-lookup"><span data-stu-id="1fb39-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="1fb39-120">Klicken Sie auf die Registerkarte **Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="1fb39-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="1fb39-121">Ändern Sie die Berechtigungen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1fb39-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="1fb39-122">Fügen Sie einzelne AD-Konten mit den Berechtigungen „Lesen/Registrieren (Zulassen)“ hinzu, oder</span><span class="sxs-lookup"><span data-stu-id="1fb39-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="1fb39-123">Fügen Sie eine Sicherheitsgruppe hinzu, die SmartCard-Benutzer mit den Berechtigungen „Lesen/Registrieren (Zulassen)“ enthält, hinzu, oder</span><span class="sxs-lookup"><span data-stu-id="1fb39-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="1fb39-124">Fügen Sie die Gruppe „Domänenbenutzer“ mit den Berechtigungen „Lesen/Registrieren (Zulassen“) hinzu</span><span class="sxs-lookup"><span data-stu-id="1fb39-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="1fb39-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1fb39-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

