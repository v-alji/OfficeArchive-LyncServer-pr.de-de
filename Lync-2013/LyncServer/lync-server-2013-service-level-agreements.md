---
title: 'Lync Server 2013: Service Level Agreements'
description: 'Lync Server 2013: Service Level Agreements.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Service level agreements
ms:assetid: 10899bad-e8b0-422d-83c9-1599fb3a7d17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720321(v=OCS.15)
ms:contentKeyID: 63969580
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 817aa8e092d9d368dfd8cb920958553ee32e8600
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441830"
---
# <a name="service-level-agreements-in-lync-server-2013"></a><span data-ttu-id="6bc71-103">Service Level Agreements in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6bc71-103">Service level agreements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bc71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bc71-104">

<span> </span></span></span>

<span data-ttu-id="6bc71-105">_**Letztes Änderungsdatum des Themas:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="6bc71-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="6bc71-106">Bei der SLA handelt es sich um ein Dokument, das die Dienste definiert, die Ihr Kunde von Ihnen erwartet.</span><span class="sxs-lookup"><span data-stu-id="6bc71-106">The SLA is a document that defines the services that your customer expects from you.</span></span> <span data-ttu-id="6bc71-107">Die Komplexität und der Inhalt dieses Dokuments hängen weitgehend davon ab, ob Kunden intern (innerhalb Ihrer Umgebung) oder extern sind.</span><span class="sxs-lookup"><span data-stu-id="6bc71-107">The complexity and content of this document depends largely on whether customers are internal (within your environment) or external.</span></span>

<div>

## <a name="external-customers"></a><span data-ttu-id="6bc71-108">Externe Kunden</span><span class="sxs-lookup"><span data-stu-id="6bc71-108">External Customers</span></span>

<span data-ttu-id="6bc71-109">Wenn Ihr Kunde extern ist, kann die SLA Teil eines rechtlichen Vertrags mit finanziellen Anreizen und Strafen für die Leistung sein, die innerhalb oder außerhalb definierter Dienstebenen liegt.</span><span class="sxs-lookup"><span data-stu-id="6bc71-109">If your customer is external, the SLA may be part of a legal contract with financial incentives and penalties for performance that falls inside or outside defined levels of service.</span></span> <span data-ttu-id="6bc71-110">Die Definition dieser Dienstebenen sollte Teil der gesamten Vertragsverhandlung sein.</span><span class="sxs-lookup"><span data-stu-id="6bc71-110">Defining these levels of service should be part of the overall contract negotiation.</span></span>

<span data-ttu-id="6bc71-111">Wie bei allen Verträgen ist es wichtig, dass beide Parteien die Erwartungen verstehen.</span><span class="sxs-lookup"><span data-stu-id="6bc71-111">As with all contracts, it’s important that both parties understand expectations.</span></span> <span data-ttu-id="6bc71-112">Die SLA definiert diese Erwartungen.</span><span class="sxs-lookup"><span data-stu-id="6bc71-112">The SLA defines these expectations.</span></span> <span data-ttu-id="6bc71-113">Der Inhalt des Dokuments sollte selten und nur aufgrund von Verhandlungen mit dem Kunden geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-113">The contents of the document should change infrequently and only because of negotiations with the customer.</span></span>

</div>

<div>

## <a name="internal-customers"></a><span data-ttu-id="6bc71-114">Interne Kunden</span><span class="sxs-lookup"><span data-stu-id="6bc71-114">Internal Customers</span></span>

<span data-ttu-id="6bc71-115">Wenn Ihr Kunde intern ist, möchten Sie möglicherweise dennoch die Dienste definieren, die von Operations Teams und IT-Systemen erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-115">If your customer is internal, you may still want to define the services that are expected of operations teams and of IT systems.</span></span> <span data-ttu-id="6bc71-116">Die SLA kann vom Betriebspersonal erstellt und als eine Reihe von Zielen für die Verfügbarkeit von IT-Diensten innerhalb Ihrer Organisation vorgesehen werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-116">The SLA may be created by the operations staff and intended as a set of goals for the availability of IT services within your organization.</span></span> <span data-ttu-id="6bc71-117">Oder, Leistungsstufen können vom Management festgesetzt und als Benchmarks bei der Beurteilung der Mitarbeiterleistung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-117">Or, performance levels may be set by management and used as benchmarks when assessing staff performance.</span></span>

</div>

<div>

## <a name="typical-criteria"></a><span data-ttu-id="6bc71-118">Typische Kriterien</span><span class="sxs-lookup"><span data-stu-id="6bc71-118">Typical Criteria</span></span>

<span data-ttu-id="6bc71-119">SLAs enthalten Abschnitte, die Kriterien für mindestverfügbarkeits-, Support-und Kapazitäts Ebenen definieren.</span><span class="sxs-lookup"><span data-stu-id="6bc71-119">SLAs include sections that define criteria of minimum levels of availability, support, and capacity.</span></span>

  - <span data-ttu-id="6bc71-120">**Verfügbarkeit**   Definieren Sie die Stunden und die Betriebssysteme, auf denen Websites und andere lync-Dienste verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="6bc71-120">**Availability**   Define the hours and the operating systems on which sites and other Lync services will be available.</span></span> <span data-ttu-id="6bc71-121">Jede Routinewartung, die sich auf die Dienstverfügbarkeit auswirkt, sollte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-121">Any routine maintenance that affects service availability should be defined.</span></span> <span data-ttu-id="6bc71-122">Definieren Sie externe Faktoren, die sich auf den Dienst auswirken, beispielsweise den Verlust der Internet Verbindung.</span><span class="sxs-lookup"><span data-stu-id="6bc71-122">Define external factors that affect service, for example, the loss of Internet connectivity.</span></span>

  - <span data-ttu-id="6bc71-123">**Unterstützung**   Definieren Sie die Stunden, wenn die Unterstützung für ein System verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="6bc71-123">**Support**   Define the hours when support for a system will be available.</span></span> <span data-ttu-id="6bc71-124">Geben Sie Methoden für Kunden an, die sich an das Supportpersonal wenden möchten, wie Vorfälle gruppiert sind, und geben Sie den Zeitpunkt für die Reaktion an und beheben Sie den Vorfall.</span><span class="sxs-lookup"><span data-stu-id="6bc71-124">Specify methods for customers to contact support staff, how incidents are grouped, and target time to respond and to resolve the incident.</span></span> <span data-ttu-id="6bc71-125">Festlegen von Häufigkeit und Inhalt des Feedbacks an den Kunden</span><span class="sxs-lookup"><span data-stu-id="6bc71-125">Define frequency and content of feedback to the customer.</span></span>

  - <span data-ttu-id="6bc71-126">**Kapazität**   Definieren Sie die maximale Größe von lync-Websites und die Schritte, die ausgeführt werden müssen, wenn der Grenzwert überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="6bc71-126">**Capacity**   Define the maximum enabled size of Lync sites and the steps to take if the limit is exceeded.</span></span> <span data-ttu-id="6bc71-127">Definieren Sie die maximale aktivierte Zeit für Standardaufgaben, beispielsweise die Zeit zum Abrufen eines Dokuments aus einer Dokumentbibliothek.</span><span class="sxs-lookup"><span data-stu-id="6bc71-127">Define the maximum enabled time to do standard tasks, such as the time to retrieve a document from a document library.</span></span> <span data-ttu-id="6bc71-128">Definieren Sie die maximale Anzahl von Benutzern pro lync-Pool, und stimmen Sie einem Prozess zu, um die Kapazität zu erhöhen, wenn mehr Benutzer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6bc71-128">Define the maximum number of users per Lync pool and agree to a process to increase capacity if more users are added.</span></span>

<span data-ttu-id="6bc71-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bc71-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

