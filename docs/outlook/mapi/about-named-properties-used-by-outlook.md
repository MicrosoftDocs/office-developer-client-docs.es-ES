---
title: Acerca de las propiedades con nombre usadas por Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 75a08db313ac1b38a400fb329eefa914858ec71e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816354"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="f7b6b-103">Acerca de las propiedades con nombre usadas por Outlook</span><span class="sxs-lookup"><span data-stu-id="f7b6b-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="f7b6b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7b6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7b6b-p101">MAPI proporciona una utilidad para asignar nombres a determinadas propiedades, para asignar estos nombres a los identificadores �nicos y para hacer que este nombre-a-identificador de asignaci�n persistente entre sesiones. Propiedades con nombre se identifican mediante un nombre y un identificador �nico global (GUID) para un conjunto de propiedades. El nombre puede ser un n�mero o una cadena. Para Microsoft Outlook 2013 o Microsoft Outlook 2010, el conjunto de propiedades a menudo es un espacio de nombres definido por Outlook 2013 o Outlook 2010, como **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="f7b6b-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="f7b6b-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span><span class="sxs-lookup"><span data-stu-id="f7b6b-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="f7b6b-p103">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span><span class="sxs-lookup"><span data-stu-id="f7b6b-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="f7b6b-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propiedad can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span><span class="sxs-lookup"><span data-stu-id="f7b6b-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="f7b6b-120">Esta referencia describe un n�mero de propiedades con nombre que se enumeran a continuaci�n.</span><span class="sxs-lookup"><span data-stu-id="f7b6b-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="f7b6b-121">Propiedades con nombre en el espacio de nombres **PSETID_Address** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-122">Propiedad can�nico de PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="f7b6b-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-123">Propiedad can�nico de PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f7b6b-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-124">Propiedad can�nico de PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b6b-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-125">Propiedad can�nico de PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="f7b6b-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-126">Propiedad can�nico de PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-127">Propiedad can�nico de PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f7b6b-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-128">Propiedad can�nico de PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-129">Propiedad can�nico de PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b6b-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-130">Propiedad can�nico de PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="f7b6b-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-131">Propiedad can�nico de PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-132">Propiedad can�nico de PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f7b6b-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-133">Propiedad can�nico de PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-134">Propiedad can�nico de PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b6b-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-135">Propiedad can�nico de PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-136">Propiedad can�nico de PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-137">Propiedad can�nico de PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="f7b6b-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-138">Propiedad can�nico de PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="f7b6b-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-139">Propiedad can�nico de PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="f7b6b-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-140">Propiedad can�nico de PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="f7b6b-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-141">Propiedad can�nico de PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="f7b6b-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-142">Propiedad can�nico de PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="f7b6b-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-143">Propiedad can�nico de PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="f7b6b-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-144">Propiedad can�nico de PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="f7b6b-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-145">Propiedad can�nico de PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-146">Propiedad can�nico de PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-147">Propiedad can�nico de PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="f7b6b-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="f7b6b-148">Propiedades con nombre en el espacio de nombres **PSETID_Appointment** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-149">Propiedad can�nico de PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="f7b6b-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-150">Propiedad can�nico de PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="f7b6b-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-151">Propiedad can�nico de PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="f7b6b-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-152">Propiedad can�nico de PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="f7b6b-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-153">Propiedad can�nico de PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="f7b6b-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-154">Propiedad can�nico de PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="f7b6b-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-155">Propiedad can�nico de PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="f7b6b-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-156">Propiedad can�nico de PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="f7b6b-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-157">Propiedad can�nico de PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="f7b6b-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-158">Propiedad can�nico de PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="f7b6b-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="f7b6b-159">Propiedades con nombre en el espacio de nombres **PSETID_Common** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-160">Propiedad can�nico de PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="f7b6b-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-161">Propiedad can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="f7b6b-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-162">Propiedad can�nico de PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="f7b6b-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-163">Propiedad can�nico de PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="f7b6b-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-164">Propiedad can�nico de PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="f7b6b-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-165">Propiedad can�nico de PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="f7b6b-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-166">Propiedad can�nico de PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="f7b6b-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-167">Propiedad can�nico de PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="f7b6b-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-168">Propiedad can�nico de PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="f7b6b-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-169">Propiedad can�nico de PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="f7b6b-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-170">Propiedad can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="f7b6b-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-171">Propiedad can�nico de PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="f7b6b-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-172">Propiedad can�nico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="f7b6b-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-173">Propiedad can�nico de PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="f7b6b-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-174">Propiedad can�nico de PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="f7b6b-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-175">Propiedad can�nico de PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="f7b6b-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-176">Propiedad can�nico de PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="f7b6b-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="f7b6b-177">Propiedades con nombre en el espacio de nombres **PSETID_Meeting** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-178">Propiedad can�nico de PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="f7b6b-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="f7b6b-179">Propiedades con nombre en el espacio de nombres **PSETID_Task** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-180">Propiedad can�nico de PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="f7b6b-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-181">Propiedad can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="f7b6b-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-182">Propiedad can�nico de PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="f7b6b-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-183">Propiedad can�nico de PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="f7b6b-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-184">Propiedad can�nico de PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="f7b6b-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-185">Propiedad can�nico de PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="f7b6b-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="f7b6b-186">Propiedades con nombre en el espacio de nombres **PS_INTERNET_HEADERS** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-187">Propiedad can�nico de PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="f7b6b-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="f7b6b-188">Propiedades con nombre en el espacio de nombres **PSETID_Log** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-189">Propiedad can�nico de PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="f7b6b-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-190">Propiedad can�nico de PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="f7b6b-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-191">Propiedad can�nico de PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="f7b6b-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-192">Propiedad can�nico de PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="f7b6b-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="f7b6b-193">Propiedades con nombre en el espacio de nombres **PS_PUBLIC_STRINGS** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7b6b-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="f7b6b-194">Propiedad can�nico de PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="f7b6b-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="f7b6b-195">Propiedad can�nico de PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="f7b6b-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="f7b6b-196">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="f7b6b-196">See also</span></span>



[<span data-ttu-id="f7b6b-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f7b6b-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f7b6b-198">Determinar si Outlook descarga solo el encabezado de un mensaje</span><span class="sxs-lookup"><span data-stu-id="f7b6b-198">Determine if Outlook Downloaded Only the Header of a Message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="f7b6b-199">Obtener la dirección de correo electrónico de un elemento de contacto</span><span class="sxs-lookup"><span data-stu-id="f7b6b-199">Get the Email Address of a Contact Item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="f7b6b-200">Quitar la definición de formulario personalizada que se guarda con un mensaje</span><span class="sxs-lookup"><span data-stu-id="f7b6b-200">Remove Custom Form Definition Saved With a Message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

