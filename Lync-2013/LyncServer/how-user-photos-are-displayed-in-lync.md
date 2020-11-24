---
title: So werden Benutzerfotos in Lync angezeigt
description: Wie Benutzer Fotos in lync angezeigt werden
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: How user photos are displayed in Lync
ms:assetid: b44a364d-a1d2-4d45-b27a-b5f77775e233
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn783119(v=OCS.15)
ms:contentKeyID: 62835297
ms.date: 08/27/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ea9e19b3965994c025659f1b2249c49ec32a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394807"
---
# <a name="how-user-photos-are-displayed-in-lync"></a><span data-ttu-id="a437a-103">So werden Benutzerfotos in Lync angezeigt</span><span class="sxs-lookup"><span data-stu-id="a437a-103">How user photos are displayed in Lync</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a437a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a437a-104">

<span> </span></span></span>

<span data-ttu-id="a437a-105">_**Letztes Änderungsdatum des Themas:** 2014-08-25_</span><span class="sxs-lookup"><span data-stu-id="a437a-105">_**Topic Last Modified:** 2014-08-25_</span></span>

<span data-ttu-id="a437a-106">**Zusammenfassung:** Benutzer Fotos, die in lync-Client angezeigt werden, können je nach verwendetem lync-Feature unterschiedlich sein, beispielsweise in einer Konferenz oder im Chat.</span><span class="sxs-lookup"><span data-stu-id="a437a-106">**Summary:** User photos displayed in Lync client can be different depending on which Lync feature you are using, such as when in a conference or an IM chat.</span></span>

<span data-ttu-id="a437a-107">Lync 2010 hat die Möglichkeit eingeführt, ein Foto in Ihr lync-Profil einzubeziehen, das für andere lync-Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a437a-107">Lync 2010 introduced the ability to include a photo with your Lync profile that is displayed to other Lync users.</span></span> <span data-ttu-id="a437a-108">Sie können auch auswählen, ob Fotos für Ihre Kontakte in lync-Client angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a437a-108">You can also choose whether or not to display photos for your contacts in Lync client.</span></span> <span data-ttu-id="a437a-109">In lync 2013: Unterstützung für Fotos mit hoher Auflösung für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a437a-109">In Lync 2013, support for high-resolution photos for users.</span></span> <span data-ttu-id="a437a-110">In diesem Thema wird beschrieben, wie Benutzer Fotos vom lync-Client abgerufen und angezeigt werden, wo die Bilder gespeichert werden, welche Einschränkungen für die einzelnen Bildquellen gelten und wie Benutzer Fotos von verschiedenen lync-Diensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-110">This topic describes how Lync client gets and displays user photos, where the images are stored, the limitations for each image source, and how user photos are used by different Lync services.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="a437a-111">Planungsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="a437a-111">Planning considerations</span></span>

<span data-ttu-id="a437a-112">Bei der Planung der Implementierung der Unterstützung für Benutzer Fotos sollten Sie Folgendes berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="a437a-112">You should consider the following when planning to implement support for user photos.</span></span>

  - <span data-ttu-id="a437a-113">Für die Unterstützung von Benutzer Fotos mit hoher Auflösung muss das Postfach des Benutzers auf Exchange 2013 und das lync-Benutzerkonto im lync 2013-Pool gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="a437a-113">High-definition user photo support requires that the user’s mailbox be located on Exchange 2013 and the Lync user account to be in Lync 2013 pool.</span></span>

  - <span data-ttu-id="a437a-114">Benutzer Fotos mit hoher Auflösung werden nur in einer Umgebung unterstützt, in der sowohl lync Server 2013 als auch Exchange 2013 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-114">High-definition user photos are supported only in an environment where both Lync Server 2013 and Exchange 2013 are used.</span></span>

  - <span data-ttu-id="a437a-115">Benutzer mit Postfächern in Exchange 2010 verwenden immer das **thumbnailPhoto** -Attribut aus AD DS als Quelle für das Benutzer Foto.</span><span class="sxs-lookup"><span data-stu-id="a437a-115">Users with Mailboxes on Exchange 2010 will always use the **thumbnailPhoto** attribute from AD DS as the source for their user photo.</span></span>

  - <span data-ttu-id="a437a-116">Ein Benutzer Foto, das als **thumbnailPhoto** -Attribut in AD DS gespeichert ist, wird für externe/verbundene Kontakte nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-116">A user photo stored as the **thumbnailPhoto** attribute from AD DS will not be displayed to external / federated contacts.</span></span>

  - <span data-ttu-id="a437a-117">Wenn die Fotos für Benutzer Kontakte in AD DS gespeichert sind, ist die verwendete Bilddatei auf 96 × 96 Pixel und auf eine Dateigröße von 100 KB limitiert.</span><span class="sxs-lookup"><span data-stu-id="a437a-117">If the photos for user contacts are stored in AD DS, the image file used is limited to 96×96 pixels and no more than 100 KB file size.</span></span>

  - <span data-ttu-id="a437a-118">Wenn die Konnektivität zwischen lync Server und Exchange Server verloren geht, werden die **thumbnailPhoto** der Benutzer mit niedriger Auflösung von AD DS und nur internen Benutzern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-118">If connectivity between Lync Server and Exchange Server is lost, the user’s low resolution **thumbnailPhoto** from AD DS will be displayed, and to internal users only.</span></span>

  - <span data-ttu-id="a437a-119">Benutzer Fotos mit hoher Auflösung werden in lync 2013-Besprechungen angezeigt, wenn für einen aktiven Lautsprecher kein Video aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-119">High-resolution user photos are displayed in Lync 2013 meetings when an active speaker does not have video enabled.</span></span> <span data-ttu-id="a437a-120">Wenn Sie den Mauszeiger über ein Miniaturbild im Katalog bewegen, wird auch das Foto mit hoher Auflösung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-120">Also, moving the mouse over thumbnail photo in the gallery will display the high-resolution photo.</span></span>

</div>

<div>

## <a name="user-photos-in-lync-2010"></a><span data-ttu-id="a437a-121">Benutzer Fotos in lync 2010</span><span class="sxs-lookup"><span data-stu-id="a437a-121">User Photos in Lync 2010</span></span>

<span data-ttu-id="a437a-122">Im lync 2010-Client können Sie aus zwei Optionen auswählen, um ein Foto für Ihr Profil, das **standardmäßige Unternehmensbild** und das **Bild von einer Webadresse** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a437a-122">In the Lync 2010 client, you can choose from two options to display a photo for your profile, **Default corporate picture** and **Show picture from a web address**.</span></span>

<div>

## <a name="default-corporate-picture"></a><span data-ttu-id="a437a-123">Standardbild für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="a437a-123">Default corporate picture</span></span>

<span data-ttu-id="a437a-124">Wenn Sie die Standardoption für das **Unternehmensbild** auswählen, ruft lync das für Sie angezeigte Foto in den Active Directory-Domänendiensten ab.</span><span class="sxs-lookup"><span data-stu-id="a437a-124">When you choose the **Default corporate picture** option, Lync gets the photo displayed for you from Active Directory Domain Services.</span></span> <span data-ttu-id="a437a-125">Das verwendete Bild ist das Bild, das als Wert für das **thumbnailPhoto** -Attribut in den Active Directory-Domänendiensten definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-125">The image used is the image defined as the value for the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span> <span data-ttu-id="a437a-126">Hierbei handelt es sich um die gleiche Datei, die von Exchange zum Anzeigen von Bildern in Outlook verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a437a-126">This is the same file that is used by Exchange to display images in Outlook.</span></span>

<span data-ttu-id="a437a-127">Überlegungen zur Verwendung von Bildern aus Active Directory-Domänendiensten umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a437a-127">Considerations for using images from Active Directory Domain Services include the following:</span></span>

  - <span data-ttu-id="a437a-128">Es werden nur Bilder mit einer Größe von bis zu 96 Pixeln von 96 Pixeln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a437a-128">Only images with dimensions up to 96 pixels by 96 pixels are supported.</span></span> <span data-ttu-id="a437a-129">Die Dateigröße für das Bild ist auf 100 KB limitiert.</span><span class="sxs-lookup"><span data-stu-id="a437a-129">The file size for the image is limited to 100 KB.</span></span>

  - <span data-ttu-id="a437a-130">Standardmäßig können Benutzer das für das **thumbnailPhoto** -Attribut verwendete Bild ändern, allerdings nicht direkt über den lync-Client.</span><span class="sxs-lookup"><span data-stu-id="a437a-130">By default, users are able to change the image used for the **thumbnailPhoto** attribute, though not directly through Lync client.</span></span> <span data-ttu-id="a437a-131">Sie können dies über die Active Directory-Domänendienste deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a437a-131">You can disable this through Active Directory Domain Services.</span></span>

  - <span data-ttu-id="a437a-132">Bilder, die in den Active Directory-Domänendiensten gespeichert sind, werden nicht für Kontakte außerhalb Ihrer Organisation angezeigt, auch wenn es sich um Verbund Kontakte handelt.</span><span class="sxs-lookup"><span data-stu-id="a437a-132">Images stored in Active Directory Domain Services are not displayed to contacts external to your organization, even if they are federated contacts.</span></span>

  - <span data-ttu-id="a437a-133">In großen Organisationen kann das Speichern und Abrufen der Bilder für eine große Anzahl von Benutzern Auswirkungen auf die Größe und Leistung der Datenbank für die Active Directory-Domänendienste haben.</span><span class="sxs-lookup"><span data-stu-id="a437a-133">In large organizations, storing and retrieving the images for large numbers of users may impact the Active Directory Domain Services database size and performance.</span></span>

  - <span data-ttu-id="a437a-134">Die geringen Bildabmessungen und die Dateigröße bedeuten, dass nur Bilder mit niedriger Auflösung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a437a-134">The limited image dimensions and file size mean that only low resolution images can be used.</span></span>

<div>

## <a name="how-users-manage-their-user-photos-in-active-directory-domain-services"></a><span data-ttu-id="a437a-135">Verwalten von Benutzer Fotos in Active Directory-Domänendiensten durch Benutzer</span><span class="sxs-lookup"><span data-stu-id="a437a-135">How users manage their user photos in Active Directory Domain Services</span></span>

<span data-ttu-id="a437a-136">Der Benutzer kann das Bild, das in seinem Active Directory-Domänendienst Profil verwendet wird, nicht direkt über den lync 2010-Client ändern.</span><span class="sxs-lookup"><span data-stu-id="a437a-136">User cannot change the image used in their Active Directory Domain Services profile directly through Lync 2010 client.</span></span> <span data-ttu-id="a437a-137">Sie können eine der folgenden Optionen verwenden, falls verfügbar:</span><span class="sxs-lookup"><span data-stu-id="a437a-137">They can use one of the following options to do so, if available:</span></span>

  - <span data-ttu-id="a437a-138">**SharePoint Server**   Benutzer können ein Foto auf "Meine Website" auf einem SharePoint-Server hochladen und dann die [Profilsynchronisierung in SharePoint konfigurieren](https://go.microsoft.com/fwlink/p/?linkid=507466) , um das Foto mit dem **thumbnailPhoto** -Attribut in den Active Directory-Domänendiensten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a437a-138">**SharePoint Server**   Users can upload a photo to ‘My Site’ on a SharePoint Server and then [configure profile synchronization in SharePoint](https://go.microsoft.com/fwlink/p/?linkid=507466) to synchronize the photo to the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="a437a-139">**Auf öffentlich zugänglicher URL gespeichertes Foto**   Benutzer können Ihr Benutzer Foto so konfigurieren, dass es eine öffentlich zugängliche URL für das Bild angibt, das Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a437a-139">**Photo stored on publicly accessible URL**   Users can configure their user photo specifying a publicly accessible URL for the image that they want to use.</span></span> <span data-ttu-id="a437a-140">Das Bild muss ohne Kennwort öffentlich zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="a437a-140">The image must be publicly accessible without a password.</span></span> <span data-ttu-id="a437a-141">Das Bild, das bei der angegebenen Webadresse gespeichert ist, wird über die Kategorie Visitenkarte in den Anwesenheitsinformationen an andere Benutzer übertragen.</span><span class="sxs-lookup"><span data-stu-id="a437a-141">The image stored at the specified web address is transferred to other users through the contact card category in the presence information.</span></span> <span data-ttu-id="a437a-142">Wenn der lync-Client ein Benutzer Foto anzeigen muss, wird das Bild von der angegebenen Webadresse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a437a-142">When Lync client needs to display a user photo, it retrieves the image from the specified web address.</span></span>

  - <span data-ttu-id="a437a-143">**Exchange 2010-Cmdlets für Windows PowerShell**   Administratoren können das Cmdlet " [Import-RecipientDataProperty](https://go.microsoft.com/fwlink/p/?linkid=507468) " in der Exchange 2010-Verwaltungsshell ausführen, um das **thumbnailPhoto** -Attribut zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a437a-143">**Exchange 2010 cmdlets for Windows PowerShell**   Administrators can run the [Import-RecipientDataProperty](https://go.microsoft.com/fwlink/p/?linkid=507468) cmdlet in the Exchange 2010 Management Shell in to manage the **thumbnailPhoto** attribute.</span></span> <span data-ttu-id="a437a-144">Wenn Bilder mit Exchange 2010-Cmdlets importiert werden, ist die Dateigröße auf 10 KB limitiert.</span><span class="sxs-lookup"><span data-stu-id="a437a-144">When images are imported with Exchange 2010 cmdlets, the file size is limited to 10 KB.</span></span>

  - <span data-ttu-id="a437a-145">**Tools von Drittanbietern**   Benutzer können nur Ihr eigenes Foto für das **thumbnailPhoto** -Attribut hochladen.</span><span class="sxs-lookup"><span data-stu-id="a437a-145">**Third Party tools**   Users can upload only their own photo to for the **thumbnailPhoto** attribute.</span></span>

</div>

</div>

<div>

## <a name="show-a-picture-from-a-web-address"></a><span data-ttu-id="a437a-146">Anzeigen eines Bilds aus einer Internetadresse</span><span class="sxs-lookup"><span data-stu-id="a437a-146">Show a picture from a web address</span></span>

<span data-ttu-id="a437a-147">Wenn Sie die Option **Bild aus einer Webadresse anzeigen** auswählen, ruft lync das Bild an der von Ihnen eingegebenen Adresse ab und zeigt es für Ihr Benutzer Foto in lync an.</span><span class="sxs-lookup"><span data-stu-id="a437a-147">When you choose the **Show a picture from a web address** option, Lync gets the image at the address you enter and displays it for your user photo in Lync.</span></span>

<span data-ttu-id="a437a-148">Überlegungen zur Verwendung von Bildern aus einer Webadresse sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="a437a-148">Considerations for using images from a web address include the following:</span></span>

  - <span data-ttu-id="a437a-149">Die Dateigrößenbeschränkungen werden durch das **MaxPhotoSizeKB** -Attribut in der Clientrichtlinie bestimmt, das mit dem Cmdlet [New-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-149">File size limits are determined by the **MaxPhotoSizeKB** attribute in the client policy, defined with the [New-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463) cmdlet.</span></span> <span data-ttu-id="a437a-150">Die Standardgrößenbeschränkung beträgt 30 KB.</span><span class="sxs-lookup"><span data-stu-id="a437a-150">The default size limit is 30 KB.</span></span> <span data-ttu-id="a437a-151">Der Höchstwert ist 100 KB.</span><span class="sxs-lookup"><span data-stu-id="a437a-151">The maximum value is 100 KB.</span></span> <span data-ttu-id="a437a-152">Es gibt keine Einschränkung für die Auflösung des Bilds, aber wenn Sie versuchen, eine Bilddatei zu verwenden, die die Größenbeschränkung überschreitet, wird Sie nicht auf lync-Clients heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="a437a-152">There is no restriction on the resolution of the image, but if you try to use an image file that exceeds the size limit it will not be downloaded to Lync clients.</span></span> <span data-ttu-id="a437a-153">Sie können den Wert auf 0 setzen, um zu verhindern, dass alle Benutzer Fotos in lync verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-153">You can set the value to 0 to disable all user photos from being used in Lync.</span></span>

  - <span data-ttu-id="a437a-154">Benutzer Fotos von einer Webadresse können von externen Föderationskontakten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-154">User photos from a web address can be seen by external federated contacts.</span></span>

</div>

<div>

## <a name="managing-users-photo-with-client-policy-cmdlets"></a><span data-ttu-id="a437a-155">Verwalten des Fotos eines Benutzers mit Client Richtlinien-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a437a-155">Managing user’s photo with Client Policy cmdlets</span></span>

<span data-ttu-id="a437a-156">In lync Server 2010 werden Clientrichtlinien Einstellungen mit den CsClientPolicy-Cmdlets konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a437a-156">In Lync Server 2010, client policy settings are configured with the CsClientPolicy cmdlets.</span></span> <span data-ttu-id="a437a-157">Die konfigurierten Richtlinieneinstellungen werden über die in-Band-Bereitstellung an Clients gesendet.</span><span class="sxs-lookup"><span data-stu-id="a437a-157">The configured policy settings are sent to clients through in-band provisioning.</span></span> <span data-ttu-id="a437a-158">Die beiden Parameter der CsClientPolicy-Cmdlets, die die Benutzer Fotoerfahrung bestimmen, sind **DisplayPhoto** und **MaxPhotoSizeKB**.</span><span class="sxs-lookup"><span data-stu-id="a437a-158">The two parameters of the CsClientPolicy cmdlets that determine the user photo experience are **DisplayPhoto** and **MaxPhotoSizeKB**.</span></span> <span data-ttu-id="a437a-159">Der entsprechende in-Band-Bereitstellungsparameter für **DisplayPhoto** und **MaxPhotoSizeKB** hat den Namen " **fotousage**".</span><span class="sxs-lookup"><span data-stu-id="a437a-159">The corresponding in-band provisioning parameter for **DisplayPhoto** and **MaxPhotoSizeKB** is named **PhotoUsage**.</span></span> <span data-ttu-id="a437a-160">Werte für den Parameter " **fotousage** " werden über die **endpointConfiguration** **provisiongroup** an Clients gesendet.</span><span class="sxs-lookup"><span data-stu-id="a437a-160">Values for the **PhotoUsage** parameter are send to clients through the **endpointConfiguration** **provisionGroup**.</span></span> <span data-ttu-id="a437a-161">Weitere Informationen finden Sie unter [Übersicht über Client Richtlinien und-Einstellungen](https://go.microsoft.com/fwlink/?linkid=507470) .</span><span class="sxs-lookup"><span data-stu-id="a437a-161">See [Overview of Client Policies and Settings](https://go.microsoft.com/fwlink/?linkid=507470) for more information.</span></span>

<span data-ttu-id="a437a-162">Der **DisplayPhoto** -Parameterwert bestimmt die Quelle des Foto Bilds des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a437a-162">The **DisplayPhoto** parameter value determines the source of the user's photo image.</span></span> <span data-ttu-id="a437a-163">Die unterstützten Werte sind in der folgenden Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="a437a-163">The supported values are included in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a437a-164">DisplayPhoto-Parameterwert</span><span class="sxs-lookup"><span data-stu-id="a437a-164">DisplayPhoto parameter value</span></span></th>
<th><span data-ttu-id="a437a-165">Bildquelle</span><span class="sxs-lookup"><span data-stu-id="a437a-165">Image source</span></span></th>
<th><span data-ttu-id="a437a-166">Lync 2010-Clienteinstellungen</span><span class="sxs-lookup"><span data-stu-id="a437a-166">Lync 2010 client settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a437a-167">Nophoto</span><span class="sxs-lookup"><span data-stu-id="a437a-167">NoPhoto</span></span></p></td>
<td><p><span data-ttu-id="a437a-168">Keine</span><span class="sxs-lookup"><span data-stu-id="a437a-168">none</span></span></p></td>
<td><p><span data-ttu-id="a437a-169"><strong>Mein Bild nicht anzeigen</strong></span><span class="sxs-lookup"><span data-stu-id="a437a-169"><strong>Do not show my picture</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a437a-170">PhotoFromADOnly</span><span class="sxs-lookup"><span data-stu-id="a437a-170">PhotoFromADOnly</span></span></p></td>
<td><p><span data-ttu-id="a437a-171">Active Directory</span><span class="sxs-lookup"><span data-stu-id="a437a-171">Active Directory</span></span></p></td>
<td><p><span data-ttu-id="a437a-172"><strong>Standardbild für Unternehmen</strong></span><span class="sxs-lookup"><span data-stu-id="a437a-172"><strong>Default corporate picture</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a437a-173">Allphotos</span><span class="sxs-lookup"><span data-stu-id="a437a-173">AllPhotos</span></span></p></td>
<td><p><span data-ttu-id="a437a-174">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="a437a-174">Web address</span></span></p></td>
<td><p><span data-ttu-id="a437a-175"><strong>Anzeigen eines Bilds aus einer Internetadresse</strong></span><span class="sxs-lookup"><span data-stu-id="a437a-175"><strong>Show a picture from a web address</strong></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="how-lync-2010-client-gets-photos"></a><span data-ttu-id="a437a-176">So erhält lync 2010-Client Fotos</span><span class="sxs-lookup"><span data-stu-id="a437a-176">How Lync 2010 client gets photos</span></span>

<span data-ttu-id="a437a-177">In lync 2010 werden Benutzer Fotos vom Adressbuchdienst auf dem Server verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a437a-177">In Lync 2010, user photos are managed on the server by the Address Book Service.</span></span> <span data-ttu-id="a437a-178">Der lync-Client ruft Benutzer Fotos ab, indem er zuerst den Adressbuch-Webabfrage Dienst (ABWQ) auf dem Server abfragt, der über den Webdienst für die Verteilerlistenerweiterung verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a437a-178">Lync client gets user photos by first querying the Address Book Web Query (ABWQ) service on the server, which is exposed through the Distribution List Expansion web service.</span></span> <span data-ttu-id="a437a-179">Der Client empfängt die Bilddatei und kopiert Sie dann in den Cache des Benutzers, um zu vermeiden, dass das Bild jedes mal heruntergeladen wird, wenn es angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a437a-179">The client receives the image file and then copies it to the user's cache to avoid downloading the image each time it needs to be displayed.</span></span> <span data-ttu-id="a437a-180">Die von der Abfrage zurückgegebenen Attributwerte werden auch im zwischengespeicherten Adressbuchdienst Eintrag für den Benutzer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a437a-180">The attribute values returned from the query are also stored in the cached Address Book Service entry for the user.</span></span> <span data-ttu-id="a437a-181">Der Adressbuchdienst löscht alle zwischengespeicherten Bilder alle 24 Stunden, was bedeutet, dass es bis zu 24 Stunden dauern kann, bis neue Benutzer Bilder im Cache auf dem Server aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-181">The Address Book Service deletes all cached images every 24 hours, which means that it can take up to 24 hours for new user images to be updated in the cache on the server.</span></span> <span data-ttu-id="a437a-182">Sie können eine Aktualisierung des Caches erzwingen, indem Sie das Cmdlet [Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a437a-182">You can force an update to the cache by using the [Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook) cmdlet.</span></span>

<span data-ttu-id="a437a-183">Benutzer Fotos, die im Anwesenheitsstatus enthalten sind, weisen auch einen zugehörigen Hashwert auf, mit dem lync-Client ermittelt, ob ein neueres Bild verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-183">User photos included in Presence status also have an associated hash value that Lync client uses to determine whether there is a newer image available.</span></span> <span data-ttu-id="a437a-184">Der Client wird automatisch über Änderungen an der im Anwesenheitsstatus verwendeten Bilddatei benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-184">The client is automatically notified of changes to the image file used in Presence status.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="a437a-185">Da Fotos nicht in der GalContacts. DB-Datenbank gespeichert sind, hängt das Herunterladen von Benutzer Fotos nicht von der <STRONG>AddressBookAvailability</STRONG> -Einstellung in der Clientrichtlinie ab (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">Satz-CsClientPolicy</A>).</span><span class="sxs-lookup"><span data-stu-id="a437a-185">Because photos are not stored in the GalContacts.db database, downloading user photos is not dependent on the <STRONG>AddressBookAvailability</STRONG> setting in the client policy (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">Set-CsClientPolicy</A>).</span></span>



</div>

<span data-ttu-id="a437a-186">Die Abfrage des ABWQ-Diensts umfasst die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="a437a-186">The query to the ABWQ service includes the following attributes:</span></span>

  - <span data-ttu-id="a437a-187">**Fotohash**   Der Hashwert der binären Fotodaten und wird verwendet, um zu bestimmen, ob sich das aktuelle Foto geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a437a-187">**PhotoHash**   The hash value of the binary photo data, and is used to determine whether the current photo has changed.</span></span>

  - <span data-ttu-id="a437a-188">**PhotoRelPath**   Der relative Pfad zur Bilddatei, die auf dem Server gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-188">**PhotoRelPath**   The relative path to the image file stored on the server.</span></span>

  - <span data-ttu-id="a437a-189">**Fotos**   Die Größe der Bilddatei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a437a-189">**PhotoSize**   The size of the image file, in bytes.</span></span>

  - <span data-ttu-id="a437a-190">**Timestamp**   Das Datum und die Uhrzeit, zu der die Bilddatei zuletzt vom Server heruntergeladen und in den Clientcache kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a437a-190">**TimeStamp**   The date and time at which the image file was last downloaded from the server and copied to the client cache.</span></span>

<span data-ttu-id="a437a-191">Als nächstes vergleicht der lync 2010-Client nach dem Abrufen der Bilddatei die von der Abfrage zurückgegebenen Attributwerte mit den vom Client empfangenen Attributwerten aus der in-Band-Bereitstellung, um festzustellen, ob Sie sich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a437a-191">Next, after retrieving the image file, Lync 2010 client compares the attribute values returned from the query against the attribute values received by the client from in-band provisioning to see if they are different.</span></span> <span data-ttu-id="a437a-192">Wenn sich die Werte unterscheiden, ruft der Client die Bilddatei des angemeldeten Benutzers mit einer HTTP GET-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="a437a-192">If the values are different, the client retrieves the image file of the signed-in user with an HTTP GET request.</span></span>

<span data-ttu-id="a437a-193">Darüber hinaus überprüft der Client den Server alle 24 Stunden ab dem Zeitpunkt, zu dem die zwischengespeicherte Version der Bilddatei erstellt wurde, um den Wert des Foto **Hash** Attributs auf dem Server mit dem Wert auf dem Client zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a437a-193">Additionally, the client checks with the server every 24 hours from the time at which the cached version of the image file was created to compare the value of the **PhotoHash** attribute on the server with the value on the client.</span></span> <span data-ttu-id="a437a-194">Wenn sich die Werte unterscheiden, weiß der Client, dass sich die Bilddatei geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a437a-194">If the values are different, the client knows that the image file has changed.</span></span> <span data-ttu-id="a437a-195">Um die aktualisierte Image-Datei abzurufen, fragt der Client erneut den ABWQ-Dienst ab, um die Bilddatei im Clientcache mit der Bilddatei auf dem Server zu aktualisieren, wodurch auch der **Zeitstempel** für die Datei im Clientcache zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a437a-195">To obtain the updated image file, the client again queries the ABWQ service to update the image file in the client cache with the image file on the server, which also resets the **TimeStamp** on the file in the client cache.</span></span>

<span data-ttu-id="a437a-196">Im folgenden wird eine Beispielantwort auf eine Abfrage des ABWQ-Diensts veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="a437a-196">The following is an example response to a query to the ABWQ service:</span></span>
```xml
    <Attribute>
              <Name>PhotoRelPath</Name>
              <Value>efa6096aed2746cb9ab2037f7dbdde9d.f2eeeb5946db54a7aa607ecd3ae09d
              95.photo</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
              <Name>PhotoHash</Name>
              <Value>f2eeeb5946db54a7aa607ecd3ae09d95</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
         <Name>PhotoSize</Name>
         <Value>4620</Value>
         <Valuesxmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
    i:nil="true" />
    </Attribute>
```

</div>

</div>

<div>

## <a name="user-photos-in-lync-2013"></a><span data-ttu-id="a437a-197">Benutzer Fotos in lync 2013</span><span class="sxs-lookup"><span data-stu-id="a437a-197">User photos in Lync 2013</span></span>

<span data-ttu-id="a437a-198">Lync 2013 hat Unterstützung für Bilder mit hoher Auflösung für Benutzer Fotos eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a437a-198">Lync 2013 introduced support for high-resolution images for user photos.</span></span> <span data-ttu-id="a437a-199">Lync 2013 umfasst auch die Unterstützung für das Speichern von Benutzer Fotos im Postfach des Benutzers in Exchange 2013, wodurch die in lync 2010 vorhandenen Bildauflösungen und Größenbeschränkungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-199">Lync 2013 also includes support for storing user photos in the user's mailbox on Exchange 2013, which removes the image resolution and size limitations present in Lync 2010.</span></span> <span data-ttu-id="a437a-200">Benutzer Fotos in lync 2013 können bis zu 648 Pixel von 648 Pixeln mit einer Dateigröße von bis zu 20 MB sein.</span><span class="sxs-lookup"><span data-stu-id="a437a-200">User photos in Lync 2013 can be up to 648 pixels by 648 pixels with a file size of up to 20 MB.</span></span> <span data-ttu-id="a437a-201">Fotos mit hoher Auflösung in lync 2013 müssen sich im Postfach des Benutzers in Exchange 2013 befinden und nur mit dem lync 2013-Client unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-201">High-resolution photos in Lync 2013 must be located in the user's mailbox on Exchange 2013, and are supported only with Lync 2013 client.</span></span> <span data-ttu-id="a437a-202">Diese Integration in Exchange nutzt das neue Autorisierungsframework, das in den 2013-Versionen von lync, Exchange und SharePoint namens OAuth enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-202">This integration with Exchange takes advantage of the new authorization framework included in the 2013 versions of Lync, Exchange, and SharePoint called Oauth.</span></span>

<span data-ttu-id="a437a-203">Wenn Exchange 2013 in Ihrer Bereitstellung nicht verwendet wird, ist die Unterstützung für Benutzer Fotos identisch mit lync 2010.</span><span class="sxs-lookup"><span data-stu-id="a437a-203">If Exchange 2013 is not used in your deployment, support for user photos is the same as with Lync 2010.</span></span> <span data-ttu-id="a437a-204">Die Benutzeroptionen zur Auswahl des zu verwendenden Fotos unterscheiden sich jedoch in lync 2013-Client.</span><span class="sxs-lookup"><span data-stu-id="a437a-204">However, the user options to choose the photo to use are different in Lync 2013 client.</span></span> <span data-ttu-id="a437a-205">In lync 2013-Client können Benutzer entweder " **mein Bild verbergen** " oder " **mein Bild anzeigen**" auswählen.</span><span class="sxs-lookup"><span data-stu-id="a437a-205">In Lync 2013 client, users can select either **Hide my picture** or **Show my picture**.</span></span> <span data-ttu-id="a437a-206">Die Option " **Bild von einer Website anzeigen** " ist standardmäßig nicht verfügbar, kann aber durch Zuweisen einer Clientrichtlinie aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a437a-206">The option **Show a picture from a website** is not available by default, but can be enabled by assigning a client policy.</span></span>

<div>

## <a name="hide-my-picture"></a><span data-ttu-id="a437a-207">Mein Bild ausblenden</span><span class="sxs-lookup"><span data-stu-id="a437a-207">Hide my picture</span></span>

<span data-ttu-id="a437a-208">Einstellungen für Benutzer Fotos finden Sie im Dialogfeld " **Optionen** " in lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a437a-208">Settings for user photos are on the **Options** dialog in Lync 2013.</span></span> <span data-ttu-id="a437a-209">Wenn Sie **mein Bild ausblenden** auswählen, wird im lync-Client kein Benutzer Foto angezeigt, aber Ihr Foto wird weiterhin auf Ihrer Visitenkarte und außerhalb von lync angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-209">When you choose **Hide my picture**, no user photo is displayed for you in Lync client, but your photo is still displayed on your contact card and outside of Lync.</span></span>

</div>

<div>

## <a name="show-my-picture"></a><span data-ttu-id="a437a-210">Mein Bild anzeigen</span><span class="sxs-lookup"><span data-stu-id="a437a-210">Show my picture</span></span>

<span data-ttu-id="a437a-211">Wenn Sie die Option " **mein Bild anzeigen** " auswählen, wird das Benutzer Foto in einem lync-Client und anderen Benutzern in lync-Unterhaltungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a437a-211">When you choose the **Show my picture** option, your user photo is displayed in your Lync client and to other users in Lync conversations.</span></span> <span data-ttu-id="a437a-212">Das verwendete Bild wird in AD DS gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a437a-212">The image used is the one stored in AD DS.</span></span>

</div>

<div>

## <a name="show-a-picture-from-a-website"></a><span data-ttu-id="a437a-213">Anzeigen eines Bilds von einer Website</span><span class="sxs-lookup"><span data-stu-id="a437a-213">Show a picture from a website</span></span>

<span data-ttu-id="a437a-214">Die Option **Bild von einer Website anzeigen** steht in lync 2013 nach dem Festlegen einer Clientrichtlinie zum Aktivieren zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a437a-214">The **Show picture from a website** option becomes available in Lync 2013 after a client policy is set to enable it.</span></span> <span data-ttu-id="a437a-215">Die Client Version muss neuer als 15.0.4535.1002 sein, die mit den [kumulierten Updates für lync installiert wird: November 2013](https://go.microsoft.com/fwlink/p/?linkid=509908).</span><span class="sxs-lookup"><span data-stu-id="a437a-215">The client version must be newer than 15.0.4535.1002, which is installed with the [Lync Cumulative Updates: November 2013](https://go.microsoft.com/fwlink/p/?linkid=509908).</span></span> <span data-ttu-id="a437a-216">Benutzer müssen sich möglicherweise abmelden und dann wieder zurück, um die Änderungen im Client anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a437a-216">Users may need to log out and then back in again to see the changes in the client.</span></span>

<span data-ttu-id="a437a-217">Sie können festlegen, dass die Clientrichtlinie für die **Anzeige von Bildern aus einer Website** Einstellung aktiviert ist, indem Sie die Richtlinie für die CsClientPolicy in der lync Server [-](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) Verwaltungsshell ausführen.</span><span class="sxs-lookup"><span data-stu-id="a437a-217">You can set the client policy to enable to **Show picture from a website** setting by running the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) policy in the Lync Server Management Shell.</span></span> <span data-ttu-id="a437a-218">Die folgenden Beispiel-Cmdlets veranschaulichen, wie Sie die Richtlinie für alle Benutzer in Ihrer Bereitstellung global festlegen:</span><span class="sxs-lookup"><span data-stu-id="a437a-218">The following example cmdlets demonstrate how to set the policy globally for all users in your deployment:</span></span>

   ```powershell
    $pe=New-CsClientPolicyEntry -Name EnablePresencePhotoOptions -Value True
   ```

   ```powershell
    $po=Get-CsClientPolicy -Identity Global
   ```

   ```powershell
    $po.PolicyEntry.Add($pe)
   ```

   ```powershell
    Set-CsClientPolicy -Instance $po
   ```


<span data-ttu-id="a437a-219">Wenn ein Bild in das Postfach des Benutzers hochgeladen wird, erstellt Exchange automatisch eine Version der niedrigeren Auflösung des Bilds, die in Clientanwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a437a-219">When an image is uploaded to the user’s mailbox, Exchange automatically creates a lower resolution version of the image which can be used in client applications.</span></span> <span data-ttu-id="a437a-220">Das Benutzer Foto wird in AD DS ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a437a-220">The user photo is also updated in AD DS.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="a437a-221">Wenn eine Bilddatei in AD DS aktualisiert wird, wird ein Bild von 48 x 48 Pixel erstellt und für die thumbnailPhoto in AD DS verwendet.</span><span class="sxs-lookup"><span data-stu-id="a437a-221">When an image file is updated in AD DS, a 48 x 48 pixel image is created and used for the thumbnailPhoto in AD DS.</span></span> <span data-ttu-id="a437a-222">Jedes vorhandene Bild wird ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a437a-222">Any existing image is replaced.</span></span> <span data-ttu-id="a437a-223">Wenn Sie AD DS also ein 96 x 96-Bild hinzugefügt haben, wird es mit dem neuen 48 x 48-Bild überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a437a-223">So if you added a 96 x 96 image to AD DS, it will be overwritten with the new 48 x 48 image.</span></span> <span data-ttu-id="a437a-224">Dies ist nur wichtig, wenn Sie Benutzer in Ihrer Umgebung mit lync 2010-Clients verwenden, da diese Clients Benutzer Fotos von AD DS erhalten.</span><span class="sxs-lookup"><span data-stu-id="a437a-224">This is only important is you have users in your environment using Lync 2010 clients, as those clients will obtain user photos from AD DS.</span></span> <span data-ttu-id="a437a-225">Sie können 96 x 96 Pixelbilder importieren, um diejenigen zu ersetzen, die von AD DS erstellt wurden, wenn Sie über lync 2010-Clients in Ihrer Organisation verfügen.</span><span class="sxs-lookup"><span data-stu-id="a437a-225">You can import 96 x 96 pixel images to replace the ones created by AD DS if you have Lync 2010 clients in your organization.</span></span>



</div>

</div>

<div>

## <a name="user-photo-support-in-lync-2013"></a><span data-ttu-id="a437a-226">Unterstützung für Benutzer Fotos in lync 2013</span><span class="sxs-lookup"><span data-stu-id="a437a-226">User photo support in Lync 2013</span></span>

<span data-ttu-id="a437a-227">In lync 2013 werden für Benutzer Fotos drei Bildauflösungen unterstützt, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a437a-227">In Lync 2013, three image resolutions are supported for user photos as described in the following table.</span></span> <span data-ttu-id="a437a-228">Das verwendete Bild wird von der Clientrichtlinien Einstellung bestimmt, die lync-Benutzern zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a437a-228">The image that is used is determined by the client policy setting assigned to Lync users.</span></span> <span data-ttu-id="a437a-229">Weitere Informationen finden Sie unter "Verwalten des Fotos des Benutzers mit Client Richtlinien-Cmdlets" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="a437a-229">See “Managing user’s photo with Client Policy cmdlets” in this topic for more information.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a437a-230">Bildauflösung (Pixel)</span><span class="sxs-lookup"><span data-stu-id="a437a-230">Image resolution (pixels)</span></span></th>
<th><span data-ttu-id="a437a-231">Anwendung</span><span class="sxs-lookup"><span data-stu-id="a437a-231">Application</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a437a-232">48 x 48</span><span class="sxs-lookup"><span data-stu-id="a437a-232">48 x 48</span></span></p></td>
<td><p><span data-ttu-id="a437a-233">Wird verwendet, wenn kein Bild höherer Auflösung ausgewählt ist</span><span class="sxs-lookup"><span data-stu-id="a437a-233">Used if no higher resolution image is selected</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a437a-234">96 x 96</span><span class="sxs-lookup"><span data-stu-id="a437a-234">96 x 96</span></span></p></td>
<td><p><span data-ttu-id="a437a-235">Verwendung in Outlook Web App und Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="a437a-235">Used in Outlook Web App and Outlook 2013</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a437a-236">648 x 648</span><span class="sxs-lookup"><span data-stu-id="a437a-236">648 x 648</span></span></p></td>
<td><p><span data-ttu-id="a437a-237">Wird in lync 2013-Desktop Client und lync 2013 Web App verwendet</span><span class="sxs-lookup"><span data-stu-id="a437a-237">Used in Lync 2013 desktop client and Lync 2013 Web App</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a437a-238">Jeder Benutzer mit einem in Exchange 2013 aktivierten Postfach kann ein anderes Bild, einschließlich Fotos mit hoher Auflösung, über die Outlook Web Access-oder lync 2013-Clientoptionen hochladen.</span><span class="sxs-lookup"><span data-stu-id="a437a-238">Any user with a mailbox enabled in Exchange 2013 can upload a different image, including high-resolution photos, through Outlook Web Access or Lync 2013 client options.</span></span> <span data-ttu-id="a437a-239">Die empfohlenen Einstellungen für verwendete Bilder sind:</span><span class="sxs-lookup"><span data-stu-id="a437a-239">The recommended settings for images used include:</span></span>

  - <span data-ttu-id="a437a-240">**Bildauflösung**   648 x 648 Pixel</span><span class="sxs-lookup"><span data-stu-id="a437a-240">**Image Resolution**   648 by 648 pixels</span></span>

  - <span data-ttu-id="a437a-241">**Farbtiefe**   24-Bit</span><span class="sxs-lookup"><span data-stu-id="a437a-241">**Color Depth**   24-bit</span></span>

  - <span data-ttu-id="a437a-242">**Bilddateigröße**   bis zu 20 MB</span><span class="sxs-lookup"><span data-stu-id="a437a-242">**Image file size**   up to 20 MB</span></span>

  - <span data-ttu-id="a437a-243">**Dateiformat**   JPEG</span><span class="sxs-lookup"><span data-stu-id="a437a-243">**File format**   JPEG</span></span>

<span data-ttu-id="a437a-244">Ein typisches 24-Bit-JPEG-Bild mit einer Größe von 648 Pixeln von 648 Pixeln hat eine Dateigröße von etwa 240 KB, sodass für alle 4 Benutzer Fotos 1 MB Speicherplatz benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a437a-244">A typical 24-bit JPEG image that is 648 pixels by 648 pixels has a file size of about 240 KB, so 1 MB of storage space is needed for every 4 user photos.</span></span>

<span data-ttu-id="a437a-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a437a-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

