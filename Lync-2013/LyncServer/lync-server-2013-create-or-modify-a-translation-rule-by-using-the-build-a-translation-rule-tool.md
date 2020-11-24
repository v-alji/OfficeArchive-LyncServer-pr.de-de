---
title: Erstellen oder Ändern einer Übersetzungsregel mithilfe des Tools zum Erstellen einer Übersetzungsregel
description: Erstellen oder Ändern einer Übersetzungsregel mithilfe des Tools zum Erstellen einer Übersetzungsregel
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a translation rule by using the Build a Translation Rule tool
ms:assetid: ba112df8-3bb4-48e4-a353-4bf9110ccd71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412909(v=OCS.15)
ms:contentKeyID: 48185224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116048fff834e797bca76a895f45cd0ebc83ab94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393826"
---
# <a name="create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool-in-lync-server-2013"></a><span data-ttu-id="0ac11-103">Erstellen oder Ändern einer Übersetzungsregel mithilfe des Tools zum Erstellen einer Übersetzungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-103">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ac11-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ac11-104">

<span> </span></span></span>

<span data-ttu-id="0ac11-105">_**Letztes Änderungsdatum des Themas:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="0ac11-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="0ac11-106">Führen Sie die folgenden Schritte aus, wenn Sie eine Übersetzungsregel definieren möchten, indem Sie eine Gruppe von Werten im Tool zum **Erstellen einer Übersetzungsregel** eingeben und die lync Server-Systemsteuerung aktivieren, um das entsprechende Übereinstimmungsmuster und die Übersetzungsregel für Sie zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0ac11-106">Follow these steps if you want to define a translation rule by entering a set of values in the **Build a Translation Rule** tool and enabling Lync Server Control Panel to generate the corresponding matching pattern and translation rule for you.</span></span> <span data-ttu-id="0ac11-107">Alternativ können Sie manuell einen regulären Ausdruck erstellen, um das Vergleichsmuster und die Übersetzungsregel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0ac11-107">Alternatively, you can a write regular expression manually to define the matching pattern and translation rule.</span></span> <span data-ttu-id="0ac11-108">Ausführliche Informationen finden Sie unter [Manuelles Erstellen oder Ändern einer Übersetzungsregel in lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-manually.md).</span><span class="sxs-lookup"><span data-stu-id="0ac11-108">For details, see [Create or modify a translation rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-manually.md).</span></span>

<div>

## <a name="to-define-a-rule-by-using-the-build-a-translation-rule-tool"></a><span data-ttu-id="0ac11-109">So definieren Sie eine Regel mit dem Tool zum Erstellen einer Übersetzungsregel</span><span class="sxs-lookup"><span data-stu-id="0ac11-109">To define a rule by using the Build a Translation Rule tool</span></span>

1.  <span data-ttu-id="0ac11-110">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="0ac11-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="0ac11-111">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0ac11-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="0ac11-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ac11-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0ac11-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0ac11-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0ac11-114">Wenn Sie mit dem Definieren einer Übersetzungsregel beginnen möchten, führen Sie die Schritte unter [Konfigurieren eines Trunks mit medienumgehung in lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) bis Schritt 10 aus, oder [Konfigurieren Sie einen trunk ohne medienumgehung in lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) bis Schritt 9.</span><span class="sxs-lookup"><span data-stu-id="0ac11-114">To begin defining a translation rule, follow the steps in [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) through step 10 or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) through step 9.</span></span>

4.  <span data-ttu-id="0ac11-115">Geben Sie unter **Name** auf der Seite **Neue Übersetzungsregel** oder **Übersetzungsregel bearbeiten** einen Namen ein, der das zu übersetzende Nummernmuster beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0ac11-115">Under **Name** on the **New Translation Rule** or **Edit Translation Rule** page, type a name that describes the number pattern being translated.</span></span>

5.  <span data-ttu-id="0ac11-116">(Optional) Geben Sie unter **Beschreibung** eine Beschreibung der Übersetzungsregel ein, z. B. **US International long-distance dialing**.</span><span class="sxs-lookup"><span data-stu-id="0ac11-116">(Optional) Under **Description**, type a description of the translation rule, for example **US International long-distance dialing**.</span></span>

6.  <span data-ttu-id="0ac11-117">Geben Sie im Abschnitt **Übersetzungsregel erstellen** des Dialogfelds die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="0ac11-117">In the **Build a Translation Rule** section of the dialog box, enter values in the following fields:</span></span>
    
      - <span data-ttu-id="0ac11-118">**Anfangsziffern**: (Optional) Geben Sie die Anfangsziffern der Nummern ein, die Sie mit dem Muster abgleichen möchten.</span><span class="sxs-lookup"><span data-stu-id="0ac11-118">**Starting digits**: (Optional) Specify the leading digits of numbers you want the pattern to match.</span></span> <span data-ttu-id="0ac11-119">Geben Sie beispielsweise **+** in dieses Feld die Zahlen im E. 164-Format ein (die mit + beginnen).</span><span class="sxs-lookup"><span data-stu-id="0ac11-119">For example, enter **+** in this field to match numbers in E.164 format (which begin with +).</span></span>
    
      - <span data-ttu-id="0ac11-p105">**Länge**: Geben Sie die Anzahl von Ziffern im Vergleichsmuster ein und wählen Sie aus, ob mit dem Muster Nummern abgeglichen werden sollen, die exakt diese Länge, mindestens diese Länge oder eine beliebige Länge aufweisen. Geben Sie beispielsweise **11** ein und wählen Sie in der Dropdownliste die Einstellung **At least**, um Nummern abzugleichen, die mindestens 11 Ziffern umfassen.</span><span class="sxs-lookup"><span data-stu-id="0ac11-p105">**Length**: Specify the number of digits in the matching pattern and select whether you want the pattern to match numbers that are this length exactly, at least this length, or any length. For example, enter **11** and select **At least** in the drop-down list to match numbers that are at least 11 digits in length.</span></span>
    
      - <span data-ttu-id="0ac11-122">**Zu entfernende Ziffern**: (Optional) Geben Sie die Anzahl von Anfangsziffern ein, die entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ac11-122">**Digits to remove**: (Optional) Specify the number of starting digits to be removed.</span></span> <span data-ttu-id="0ac11-123">Geben Sie beispielsweise **1** ein, um den **+** Anfang der Zahl zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0ac11-123">For example, enter **1** to strip out the **+** from the beginning of the number.</span></span>
    
      - <span data-ttu-id="0ac11-p107">**Hinzuzufügende Ziffern**: (Optional) Geben Sie die Ziffern ein, die der übersetzten Nummer vorangestellt werden sollen. Geben Sie beispielsweise **011** ein, wenn bei Anwendung der Regel der übersetzten Nummer die Ziffernfolge 011 vorangestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ac11-p107">**Digits to add**: (Optional) Specify digits to be prepended to the translated numbers. For example, enter **011** if you want 011 to be prepended to the translated numbers when the rule is applied.</span></span>
    
    <span data-ttu-id="0ac11-p108">Die in diesen Feldern eingegebenen Werte werden in den Feldern **Muster für Vergleich** und **Übersetzungsregel** widergespiegelt. Wenn Sie beispielsweise die vorstehend genannten Beispielwerte verwenden, lautet der reguläre Ausdruck im Feld **Muster für Vergleich** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ac11-p108">The values you enter in these fields are reflected in the **Pattern to match** and **Translation rule** fields. For example, if you specify the preceding example values, the resulting regular expression in the **Pattern to match** field is:</span></span>
    
    <span data-ttu-id="0ac11-128">**^\\+ ( \\ d {9} \\ +) $**</span><span class="sxs-lookup"><span data-stu-id="0ac11-128">**^\\+(\\d{9}\\d+)$**</span></span>
    
    <span data-ttu-id="0ac11-p109">Das Feld **Übersetzungsregel** gibt ein Muster für das Format der übersetzten Nummern an. Dieses Muster besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="0ac11-p109">The **Translation rule** field specifies a pattern for the format of translated numbers. This pattern has two parts:</span></span>
    
      - <span data-ttu-id="0ac11-131">Einem Wert (z. B. **$1**), der die Anzahl von Ziffern im Vergleichsmuster repräsentiert</span><span class="sxs-lookup"><span data-stu-id="0ac11-131">A value (for example, **$1**) that represents the number of digits in the matching pattern</span></span>
    
      - <span data-ttu-id="0ac11-132">(Optional) Einem Wert, den Sie durch eine Eingabe im Feld **Hinzuzufügende Ziffern** voranstellen können</span><span class="sxs-lookup"><span data-stu-id="0ac11-132">(Optional) A value that you can prepend by entering it in the **Digits to add** field</span></span>
    
    <span data-ttu-id="0ac11-133">Bei Verwendung der vorstehend genannten Beispiele wird der Wert **011$1** im Feld **Übersetzungsregel** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ac11-133">Using the preceding example values, **011$1** appears in the **Translation rule** field.</span></span>
    
    <span data-ttu-id="0ac11-134">Bei Anwendung dieser Übersetzungsregel wird die Nummer +441235551010 in 011441235551010 umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="0ac11-134">When this translation rule is applied, +441235551010 becomes 011441235551010.</span></span>

7.  <span data-ttu-id="0ac11-135">Klicken Sie auf **OK**, um die Übersetzungsregel zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ac11-135">Click **OK** to save the translation rule.</span></span>

8.  <span data-ttu-id="0ac11-136">Klicken Sie auf **OK**, um die Trunkkonfiguration zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ac11-136">Click **OK** to save the trunk configuration.</span></span>

9.  <span data-ttu-id="0ac11-137">Klicken Sie auf der Seite **Trunkkonfiguration** auf **Commit** und klicken Sie anschließend auf **Commit für alle Elemente ausführen**.</span><span class="sxs-lookup"><span data-stu-id="0ac11-137">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="0ac11-138">Immer dann, wenn Sie eine Übersetzungsregel erstellen oder ändern, müssen Sie den Befehl <STRONG>Commit für alle Elemente ausführen</STRONG> ausführen, um die Konfigurationsänderung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0ac11-138">Whenever you create or modify a translation rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="0ac11-139">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">veröffentlichen ausstehender Änderungen an der VoIP-Routingkonfiguration in lync Server 2013</A> in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="0ac11-139">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0ac11-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ac11-140">See Also</span></span>


[<span data-ttu-id="0ac11-141">Manuelles Erstellen oder Ändern einer Übersetzungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-141">Create or modify a translation rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-manually.md)  
[<span data-ttu-id="0ac11-142">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-142">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="0ac11-143">Konfigurieren eines Trunks ohne medienumgehung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-143">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
[<span data-ttu-id="0ac11-144">Veröffentlichen ausstehender Änderungen an der VoIP-Routingkonfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-144">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="0ac11-145">Globale Medien Umgehungs Optionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ac11-145">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="0ac11-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ac11-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

