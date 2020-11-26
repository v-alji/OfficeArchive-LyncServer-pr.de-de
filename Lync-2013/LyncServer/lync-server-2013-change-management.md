---
title: 'Lync Server 2013: Änderungsverwaltung'
description: 'Lync Server 2013: Änderungsverwaltung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435126"
---
# <a name="change-management-in-lync-server-2013"></a>Änderungsverwaltung in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-08-18_

Änderungen an der IT-Umgebung sind unvermeidlich. Zu den Änderungen gehören neue Technologien, Systeme, Anwendungen, Hardware, Tools, Prozesse und Änderungen an Rollen und Zuständigkeiten. Mit einem effektiven Änderungsverwaltungssystem können Sie Änderungen an der IT-Umgebung schnell und mit minimaler Dienstunterbrechung einführen. Ein Change Management System führt die Teams zusammen, die an der Änderung eines Systems beteiligt sind. Beispielsweise die Entscheidung, die Vorteile der Office Web Apps zu nutzen. Hierbei handelt es sich um eine integrierte lync-Dienstanwendung, mit der Benutzer Dokumente in einem Browser lesen und bearbeiten können. Die Implementierung dieses Diensts erfordert, nachdem Sie die Produktion durchlaufen haben, die Einbindung mehrerer Teams:

  - **Test Team**   Diese Team Auslastung testet die Office Web Apps auf einem Testserver, wobei Informationen zu den erwarteten Verwendungsmustern und der erwarteten Leistung der Produktionsserver bereitgestellt werden.

  - **Lync-Administratoren**   Dieses Team ermittelt die Bereitstellungsstrategie und erstellt Skripts für die Installation, sofern dies möglich war. Das Team ist dafür verantwortlich, sicherzustellen, dass die Änderung in der Produktionsumgebung bereitgestellt wird, und ist danach für die Verwaltung verantwortlich. Das Team muss die Auswirkungen der Änderungen verstehen und in Verfahren einbeziehen, bevor die Änderungen in die Produktion übernommen werden.

  - **Netzwerk Team**   Dieses Team ist für Änderungen an Firewallregeln verantwortlich, die den Zugriff aus dem Internet auf die internen lync-Pool Server zulassen. Das Team ist auch für die Zusammenarbeit mit den lync-Administratoren verantwortlich, um sicherzustellen, dass die verfügbare Bandbreite die zusätzliche Last unterstützenkann.

  - **Sicherheits Team**   Dieses Team bewertet die Sicherheit und minimiert Risiken. Das Sicherheitsteam muss bekannte Sicherheitsanfälligkeiten überprüfen und sicherstellen, dass Sicherheitsrisiken minimiert werden.

  - **Benutzerakzeptanz Team**   Dieses Team besteht aus Benutzern, die bereit sind, das System zu testen und Feedback zu Verbesserungen anzubieten.

Der Change Management-Prozess definiert die Zuständigkeiten der einzelnen Teams und plant die auszuführende Arbeit, wobei die erforderlichen Prüfungen und Tests integriert werden. Die Steuerelemente für Änderungen variieren abhängig von der Komplexität und dem erwarteten Effekt einer Änderung. Sie können von der automatischen Genehmigung für geringfügige Änderungen, über Änderungs Überprüfungs Besprechungen bis hin zu vollständigen Bewertungen auf Projektebene variieren. Um dies besser zu erklären, werden die Gruppen von Änderungen in diesem Abschnitt erläutert.

  - **Wichtige Änderungen**   Größere Änderungen haben eine globale Auswirkung auf das System und erfordern möglicherweise Eingaben von verschiedenen Teams. Ein Beispiel hierfür ist das Upgrade auf lync Server 2013. Wichtige Änderungen betreffen viele Teams und möglicherweise andere Systeme. Der Change Management-Prozess umfasst wahrscheinlich eine oder mehrere Änderungs Überprüfungs Besprechungen, um die Teams zu informieren, die an der Änderung beteiligt sind oder von der Änderung betroffen sein werden.

  - **Signifikante Änderungen**   Wesentliche Änderungen erfordern erhebliche Ressourcen, um zu planen, zu erstellen und zu implementieren. Es sollten geeignete Änderungs Steuerelemente eingeführt werden, um sicherzustellen, dass die Auswirkungen der Änderung verstanden werden, Bereitstellungsverfahren getestet und die Rollback-und Notfallpläne bereit sind. Ein Beispiel für eine wesentliche Änderung ist die Bereitstellungeines neuen kumulativen Updates.

  - **Geringfügige Änderungen**   Geringfügige Änderungen haben keine nennenswerten Auswirkungen auf die IT-Umgebung, beispielsweise das Ändern bestimmter lync-Richtlinien über die Microsoft lync Server 2013-Systemsteuerung.

  - **Standard Änderungen**   Standard Änderungen werden regelmäßig durchgeführt und sind gut verstanden und dokumentiert. Der Change Management-Prozess sollte alle Änderungen an den Prozeduren überprüfen. Es sollte nicht für Routineänderungen wie das Erstellen einer Inhaltsdatenbank oder das Hinzufügen eines Benutzers benötigt werden.

Im folgenden Beispiel für die Änderungsverwaltung wird untersucht, wie verschiedene Teams interagieren und welche Aktionen ausgeführt werden, wenn ein neues Service Pack bereitgestellt wird. Diese Aktionen werden vom Change Management-Prozess organisiert und verwaltet.

  - **Auslösen einer Änderungsanforderung**   Das Sicherheitsteam hat das neueste Service Pack bewertet und bestätigt, dass es eine mögliche Sicherheitsanfälligkeit im Produktionssystem behebt. Das Team löst eine Änderungsanforderung aus, damit das neue kumulative Update auf alle Server angewendet wird, auf denen lync Server ausgeführt wird.

  - **Übersicht über das Service Pack-Versionshinweise**   Das lync-Administrator Team überprüft die Service Pack-Versionshinweise, um die Auswirkungen auf das System zu ermitteln.

  - **Eine Reihe von Lab-Tests wird durchgeführt**   Das lync-Administrator Team muss Test Updates auf einem Server in einer Testumgebung durchführen, um zu entscheiden, ob das Service Pack erfolgreich angewendet werden kann, ohne die installierten Anwendungen und Server Systeme zu beeinflussen. Wenn es sich um von Drittanbietern oder intern erstellte Anwendungen handelt, die eine Schnittstelle zu lync Server in einer Produktionsumgebung aufweisen, sollten diese ebenfalls getestet werden. Diese Tests können auch verwendet werden, um die Zeit zu schätzen, die für die Ausführung der Upgrades erforderlich ist.

  - **Benutzer werden über den Ausfall informiert**   Das lync-Administrator Team, das Kommunikationsteam oder der Benutzer Helpdesk informiert alle betroffenen Benutzer über den geplanten Wartungszyklus und darüber, wie lange der Dienst nicht verfügbar sein wird.

  - **Vor dem Upgrade wird eine vollständige Sicherung von lync durchgeführt**   .   Das lync-Administrator Team muss überprüfen, ob eine gültige Sicherung vorhanden ist, die verwendet werden kann, um zum ursprünglichen Systemzustand zurückzukehren, wenn die Service Pack-Installation fehlschlägt. Wir empfehlen, dass die Sicherung auf einem Standbyserver wiederhergestellt wird, damit dieses System bei Problemen problemlos zur Verfügung steht.

  - **Das kumulative Update wird bereitgestellt**   .   Das lync-Administrator Team führt die Installation während des geplanten Wartungszyklus durch.

<div>

## <a name="managing-the-timing-of-changes"></a>Verwalten der Anzeigedauer von Änderungen

Wir empfehlen, dass Sie eine Vorgehensweise zum Planen von Änderungen implementieren, um Unterbrechungen in überlappenden Abschnitten ihrer Arbeit zu vermeiden. So können beispielsweise zwei Teams eine geringfügige Änderung an einem System planen. Ein Team kann ein kumulatives Update in einem Pool anwenden, während ein anderes Team ältere Benutzer in diesen Pool migriert. Keines der Teams ist von den Änderungen betroffen, die das andere Team plant, und jedes Team weiß möglicherweise nicht unbedingt, welche Änderungen das andere Team plant. Wenn beide Änderungen gleichzeitig aufgetreten sind, gibt es möglicherweise Probleme beim Implementieren der Änderungen. Wenn nach dem Anwenden der Änderungen Probleme auftreten, beispielsweise wenn die Benutzermigration fehlschlägt, ist es möglicherweise schwierig, zu entscheiden, welche Änderung zurückgesetzt werden soll. Es sollten regelmäßige Wartungszeiten zwischen IT und Verwaltung eingerichtet werden, um die Änderungen zu testen und zu akzeptieren.

</div>

</div>

<span> </span>

</div>

</div>

</div>

