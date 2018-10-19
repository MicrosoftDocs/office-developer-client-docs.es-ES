---
title: Información sobre las propiedades con nombre que usa Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566232"
---
# <a name="about-named-properties-used-by-outlook"></a><span data-ttu-id="b62ab-103">Información sobre las propiedades con nombre que usa Outlook</span><span class="sxs-lookup"><span data-stu-id="b62ab-103">About Named Properties Used by Outlook</span></span>

  
  
<span data-ttu-id="b62ab-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b62ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b62ab-p101">MAPI proporciona un lugar para asignar nombres a algunas propiedades, para asignar estos nombres a identificadores únicos y para hacer que esta asociación nombre-a-identificador sea persistentes en todas las sesiones. Las propiedades con nombre se identifican por un nombre y un identificador único global (GUID) para un conjunto de propiedades. El nombre puede ser un número o una cadena. Para Microsoft Outlook 2013 o Microsoft Outlook 2010, el conjunto de propiedades suele ser un espacio de nombres definido por Outlook 2013 o Outlook 2010, como **PSETID_Appointment**.</span><span class="sxs-lookup"><span data-stu-id="b62ab-p101">MAPI provides a facility for assigning names to certain properties, for mapping these names to unique identifiers, and for making this name-to-identifier mapping persistent across sessions. Named properties are identified by a name and a globally unique identifier (GUID) for a property set. The name can be a number or a string. For Microsoft Outlook 2013 or Microsoft Outlook 2010, the property set is often a namespace defined by Outlook 2013 or Outlook 2010, such as **PSETID_Appointment**.</span></span> 
  
<span data-ttu-id="b62ab-p102">Las propiedades con nombre se manipulan utilizando las funciones [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). El nombre y el GUID del conjunto de propiedades se pasan a la función [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener un identificador de propiedad que sea válido para la sesión MAPI actual. Como este identificador de propiedad puede variar de un equipo a otro, la única forma consistente para acceder a una propiedad con nombre es conocer el nombre y el GUID del conjunto de propiedades. El intervalo de identificadores está siempre en el rango de 0x8000 y 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="b62ab-p102">Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range.</span></span> 
  
<span data-ttu-id="b62ab-p103">Cualquier objeto que implemente la interfaz [IMAPIProp: IUnknown](imapipropiunknown.md) admite propiedades con nombre. En concreto, un proveedor de servicios MAPI o un cliente MAPI tendrá que implementar [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener los valores de propiedades con nombre. La configuración de propiedades con nombre usada por Outlook 2013 o Outlook 2010 no se admite por el riesgo de que se dañen los datos que se comparten con otros clientes o proveedores MAPI.</span><span class="sxs-lookup"><span data-stu-id="b62ab-p103">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients.</span></span> 
  
<span data-ttu-id="b62ab-p104">Outlook 2013 y Outlook 2010 usan propiedades con nombre MAPI para implementar muchas de sus características, por ejemplo, la seguridad de datos adjuntos y las contrapropuestas de reunión. Por encima de estos datos subyacentes, Outlook 2013 y Outlook 2010 exponen algunas de estas propiedades como propiedades de elementos en sus modelos de objetos de Outlook 2013 y Outlook 2010. Por ejemplo, la propiedad **Email1Address** del objeto **ContactItem** en el modelo de objetos se corresponde con la [Propiedad canónica con nombre PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) en el espacio de nombres **PSETID_Address**. Pero, en general, debido a posibles problemas de compatibilidad e integridad de datos, muchas de las propiedades MAPI que usan Outlook 2013 y Outlook 2010 no se exponen en el modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="b62ab-p104">Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model.</span></span> 
  
<span data-ttu-id="b62ab-120">Esta referencia describe una serie de propiedades con nombre que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="b62ab-120">This reference describes a number of named properties that are listed below.</span></span>
  
<span data-ttu-id="b62ab-121">Propiedades con nombre en el espacio de nombres **PSETID_Address** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-121">Named properties in the **PSETID_Address** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-122">Propiedad canónica PidLidEmail1AddressType</span><span class="sxs-lookup"><span data-stu-id="b62ab-122">PidLidEmail1AddressType Canonical Property</span></span>](pidlidemail1addresstype-canonical-property.md)
    
- [<span data-ttu-id="b62ab-123">Propiedad canónica PidLidEmail1EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b62ab-123">PidLidEmail1EmailAddress Canonical Property</span></span>](pidlidemail1emailaddress-canonical-property.md)
    
- [<span data-ttu-id="b62ab-124">Propiedad canónica PidLidEmail1OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="b62ab-124">PidLidEmail1OriginalEntryId Canonical Property</span></span>](pidlidemail1originalentryid-canonical-property.md)
    
- [<span data-ttu-id="b62ab-125">Propiedad canónica PidLidEmail2AddressType</span><span class="sxs-lookup"><span data-stu-id="b62ab-125">PidLidEmail2AddressType Canonical Property</span></span>](pidlidemail2addresstype-canonical-property.md)
    
- [<span data-ttu-id="b62ab-126">Propiedad canónica PidLidEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-126">PidLidEmail2DisplayName Canonical Property</span></span>](pidlidemail2displayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-127">Propiedad canónica PidLidEmail2EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b62ab-127">PidLidEmail2EmailAddress Canonical Property</span></span>](pidlidemail2emailaddress-canonical-property.md)
    
- [<span data-ttu-id="b62ab-128">Propiedad canónica PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-128">PidLidEmail2OriginalDisplayName Canonical Property</span></span>](pidlidemail2originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-129">Propiedad canónica PidLidEmail2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="b62ab-129">PidLidEmail2OriginalEntryId Canonical Property</span></span>](pidlidemail2originalentryid-canonical-property.md)
    
- [<span data-ttu-id="b62ab-130">Propiedad canónica PidLidEmail3AddressType</span><span class="sxs-lookup"><span data-stu-id="b62ab-130">PidLidEmail3AddressType Canonical Property</span></span>](pidlidemail3addresstype-canonical-property.md)
    
- [<span data-ttu-id="b62ab-131">Propiedad canónica PidLidEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-131">PidLidEmail3DisplayName Canonical Property</span></span>](pidlidemail3displayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-132">Propiedad canónica PidLidEmail3EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b62ab-132">PidLidEmail3EmailAddress Canonical Property</span></span>](pidlidemail3emailaddress-canonical-property.md)
    
- [<span data-ttu-id="b62ab-133">Propiedad canónica PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-133">PidLidEmail3OriginalDisplayName Canonical Property</span></span>](pidlidemail3originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-134">Propiedad canónica PidLidEmail3OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="b62ab-134">PidLidEmail3OriginalEntryId Canonical Property</span></span>](pidlidemail3originalentryid-canonical-property.md)
    
- [<span data-ttu-id="b62ab-135">Propiedad canónica PidLidEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-135">PidLidEmail1DisplayName Canonical Property</span></span>](pidlidemail1displayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-136">Propiedad canónica PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="b62ab-136">PidLidEmail1OriginalDisplayName Canonical Property</span></span>](pidlidemail1originaldisplayname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-137">Propiedad canónica PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="b62ab-137">PidLidFileUnder Canonical Property</span></span>](pidlidfileunder-canonical-property.md)
    
- [<span data-ttu-id="b62ab-138">Propiedad canónica PidLidInstantMessagingAddress</span><span class="sxs-lookup"><span data-stu-id="b62ab-138">PidLidInstantMessagingAddress Canonical Property</span></span>](pidlidinstantmessagingaddress-canonical-property.md)
    
- [<span data-ttu-id="b62ab-139">Propiedad canónica PidLidWorkAddressCity</span><span class="sxs-lookup"><span data-stu-id="b62ab-139">PidLidWorkAddressCity Canonical Property</span></span>](pidlidworkaddresscity-canonical-property.md)
    
- [<span data-ttu-id="b62ab-140">Propiedad canónica PidLidWorkAddressCountry</span><span class="sxs-lookup"><span data-stu-id="b62ab-140">PidLidWorkAddressCountry Canonical Property</span></span>](pidlidworkaddresscountry-canonical-property.md)
    
- [<span data-ttu-id="b62ab-141">Propiedad canónica PidLidWorkAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="b62ab-141">PidLidWorkAddressPostalCode Canonical Property</span></span>](pidlidworkaddresspostalcode-canonical-property.md)
    
- [<span data-ttu-id="b62ab-142">Propiedad canónica PidLidWorkAddressPostOfficeBox</span><span class="sxs-lookup"><span data-stu-id="b62ab-142">PidLidWorkAddressPostOfficeBox Canonical Property</span></span>](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [<span data-ttu-id="b62ab-143">Propiedad canónica PidLidWorkAddressState</span><span class="sxs-lookup"><span data-stu-id="b62ab-143">PidLidWorkAddressState Canonical Property</span></span>](pidlidworkaddressstate-canonical-property.md)
    
- [<span data-ttu-id="b62ab-144">Propiedad canónica PidLidWorkAddressStreet</span><span class="sxs-lookup"><span data-stu-id="b62ab-144">PidLidWorkAddressStreet Canonical Property</span></span>](pidlidworkaddressstreet-canonical-property.md)
    
- [<span data-ttu-id="b62ab-145">Propiedad canónica PidLidYomiCompanyName</span><span class="sxs-lookup"><span data-stu-id="b62ab-145">PidLidYomiCompanyName Canonical Property</span></span>](pidlidyomicompanyname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-146">Propiedad canónica PidLidYomiFirstName</span><span class="sxs-lookup"><span data-stu-id="b62ab-146">PidLidYomiFirstName Canonical Property</span></span>](pidlidyomifirstname-canonical-property.md)
    
- [<span data-ttu-id="b62ab-147">Propiedad canónica PidLidYomiLastName</span><span class="sxs-lookup"><span data-stu-id="b62ab-147">PidLidYomiLastName Canonical Property</span></span>](pidlidyomilastname-canonical-property.md)
    
<span data-ttu-id="b62ab-148">Propiedades con nombre en el espacio de nombres **PSETID_Appointment** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-148">Named properties in the **PSETID_Appointment** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-149">Propiedad canónica PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="b62ab-149">PidLidAllAttendeesString Canonical Property</span></span>](pidlidallattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="b62ab-150">Propiedad canónica PidLidAppointmentCounterProposal</span><span class="sxs-lookup"><span data-stu-id="b62ab-150">PidLidAppointmentCounterProposal Canonical Property</span></span>](pidlidappointmentcounterproposal-canonical-property.md)
    
- [<span data-ttu-id="b62ab-151">Propiedad canónica PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="b62ab-151">PidLidAppointmentDuration Canonical Property</span></span>](pidlidappointmentduration-canonical-property.md)
    
- [<span data-ttu-id="b62ab-152">Propiedad canónica PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="b62ab-152">PidLidAppointmentEndWhole Canonical Property</span></span>](pidlidappointmentendwhole-canonical-property.md)
    
- [<span data-ttu-id="b62ab-153">Propiedad canónica PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="b62ab-153">PidLidAppointmentStartWhole Canonical Property</span></span>](pidlidappointmentstartwhole-canonical-property.md)
    
- [<span data-ttu-id="b62ab-154">Propiedad canónica PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b62ab-154">PidLidBusyStatus Canonical Property</span></span>](pidlidbusystatus-canonical-property.md)
    
- [<span data-ttu-id="b62ab-155">Propiedad canónica PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="b62ab-155">PidLidCcAttendeesString Canonical Property</span></span>](pidlidccattendeesstring-canonical-property.md)
    
- [<span data-ttu-id="b62ab-156">Propiedad canónica PidLidLocation</span><span class="sxs-lookup"><span data-stu-id="b62ab-156">PidLidLocation Canonical Property</span></span>](pidlidlocation-canonical-property.md)
    
- [<span data-ttu-id="b62ab-157">Propiedad canónica PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="b62ab-157">PidLidRecurring Canonical Property</span></span>](pidlidrecurring-canonical-property.md)
    
- [<span data-ttu-id="b62ab-158">Propiedad canónica PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="b62ab-158">PidLidToAttendeesString Canonical Property</span></span>](pidlidtoattendeesstring-canonical-property.md)
    
<span data-ttu-id="b62ab-159">Propiedades con nombre en el espacio de nombres **PSETID_Common** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-159">Named properties in the **PSETID_Common** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-160">Propiedad canónica PidLidCommonEnd</span><span class="sxs-lookup"><span data-stu-id="b62ab-160">PidLidCommonEnd Canonical Property</span></span>](pidlidcommonend-canonical-property.md)
    
- [<span data-ttu-id="b62ab-161">Propiedad canónica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="b62ab-161">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)
    
- [<span data-ttu-id="b62ab-162">Propiedad canónica PidLidCompanies</span><span class="sxs-lookup"><span data-stu-id="b62ab-162">PidLidCompanies Canonical Property</span></span>](pidlidcompanies-canonical-property.md)
    
- [<span data-ttu-id="b62ab-163">Propiedad canónica PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="b62ab-163">PidLidContacts Canonical Property</span></span>](pidlidcontacts-canonical-property.md)
    
- [<span data-ttu-id="b62ab-164">Propiedad canónica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="b62ab-164">PidLidCustomFlag Canonical Property</span></span>](pidlidcustomflag-canonical-property.md)
    
- [<span data-ttu-id="b62ab-165">Propiedad canónica PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="b62ab-165">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="b62ab-166">Propiedad canónica PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="b62ab-166">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="b62ab-167">Propiedad canónica PidLidHeaderItem</span><span class="sxs-lookup"><span data-stu-id="b62ab-167">PidLidHeaderItem Canonical Property</span></span>](pidlidheaderitem-canonical-property.md)
    
- [<span data-ttu-id="b62ab-168">Propiedad canónica PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="b62ab-168">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="b62ab-169">Propiedad canónica PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="b62ab-169">PidLidPropertyDefinitionStream Canonical Property</span></span>](pidlidpropertydefinitionstream-canonical-property.md)
    
- [<span data-ttu-id="b62ab-170">Propiedad canónica PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="b62ab-170">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)
    
- [<span data-ttu-id="b62ab-171">Propiedad canónica PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="b62ab-171">PidLidReminderTime Canonical Property</span></span>](pidlidremindertime-canonical-property.md)
    
- [<span data-ttu-id="b62ab-172">Propiedad canónica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="b62ab-172">PidLidFlagRequest Canonical Property</span></span>](pidlidflagrequest-canonical-property.md)
    
- [<span data-ttu-id="b62ab-173">Propiedad canónica PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="b62ab-173">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
- [<span data-ttu-id="b62ab-174">Propiedad canónica PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="b62ab-174">PidLidSmartNoAttach Canonical Property</span></span>](pidlidsmartnoattach-canonical-property.md)
    
- [<span data-ttu-id="b62ab-175">Propiedad canónica PidLidToDoTitle</span><span class="sxs-lookup"><span data-stu-id="b62ab-175">PidLidToDoTitle Canonical Property</span></span>](pidlidtodotitle-canonical-property.md)
    
- [<span data-ttu-id="b62ab-176">Propiedad canónica PidLidUseTnef</span><span class="sxs-lookup"><span data-stu-id="b62ab-176">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)
    
<span data-ttu-id="b62ab-177">Propiedades con nombre en el espacio de nombres **PSETID_Meeting** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-177">Named properties in the **PSETID_Meeting** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-178">Propiedad canónica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="b62ab-178">PidLidMeetingType Canonical Property</span></span>](pidlidmeetingtype-canonical-property.md)
    
<span data-ttu-id="b62ab-179">Propiedades con nombre en el espacio de nombres **PSETID_Task** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-179">Named properties in the **PSETID_Task** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-180">Propiedad canónica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="b62ab-180">PidLidTaskActualEffort Canonical Property</span></span>](pidlidtaskactualeffort-canonical-property.md)
    
- [<span data-ttu-id="b62ab-181">Propiedad canónica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="b62ab-181">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
    
- [<span data-ttu-id="b62ab-182">Propiedad canónica PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="b62ab-182">PidLidTaskEstimatedEffort Canonical Property</span></span>](pidlidtaskestimatedeffort-canonical-property.md)
    
- [<span data-ttu-id="b62ab-183">Propiedad canónica PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="b62ab-183">PidLidTaskFRecurring Canonical Property</span></span>](pidlidtaskfrecurring-canonical-property.md)
    
- [<span data-ttu-id="b62ab-184">Propiedad canónica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="b62ab-184">PidLidTaskStartDate Canonical Property</span></span>](pidlidtaskstartdate-canonical-property.md)
    
- [<span data-ttu-id="b62ab-185">Propiedad canónica PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="b62ab-185">PidLidTaskStatus Canonical Property</span></span>](pidlidtaskstatus-canonical-property.md)
    
<span data-ttu-id="b62ab-186">Propiedades con nombre en el espacio de nombres **PS_INTERNET_HEADERS** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-186">Named properties in the **PS_INTERNET_HEADERS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-187">Propiedad canónica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="b62ab-187">PidTagInternetReturnPath Canonical Property</span></span>](pidtaginternetreturnpath-canonical-property.md)
    
<span data-ttu-id="b62ab-188">Propiedades con nombre en el espacio de nombres **PSETID_Log** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-188">Named properties in the **PSETID_Log** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-189">Propiedad canónica PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="b62ab-189">PidLidLogDuration Canonical Property</span></span>](pidlidlogduration-canonical-property.md)
    
- [<span data-ttu-id="b62ab-190">Propiedad canónica PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="b62ab-190">PidLidLogEnd Canonical Property</span></span>](pidlidlogend-canonical-property.md)
    
- [<span data-ttu-id="b62ab-191">Propiedad canónica PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="b62ab-191">PidLidLogStart Canonical Property</span></span>](pidlidlogstart-canonical-property.md)
    
- [<span data-ttu-id="b62ab-192">Propiedad canónica PidLidLogType</span><span class="sxs-lookup"><span data-stu-id="b62ab-192">PidLidLogType Canonical Property</span></span>](pidlidlogtype-canonical-property.md)
    
<span data-ttu-id="b62ab-193">Propiedades con nombre en el espacio de nombres **PS_PUBLIC_STRINGS** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b62ab-193">Named properties in the **PS_PUBLIC_STRINGS** namespace are the following:</span></span> 
  
- [<span data-ttu-id="b62ab-194">Propiedad canónica PidNameKeywords</span><span class="sxs-lookup"><span data-stu-id="b62ab-194">PidNameKeywords Canonical Property</span></span>](pidnamekeywords-canonical-property.md)
    
- [<span data-ttu-id="b62ab-195">Propiedad canónica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="b62ab-195">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a><span data-ttu-id="b62ab-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="b62ab-196">See also</span></span>



[<span data-ttu-id="b62ab-197">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b62ab-197">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b62ab-198">Determinar si Outlook descarga solo el encabezado de un mensaje</span><span class="sxs-lookup"><span data-stu-id="b62ab-198">Determine if Outlook downloaded only the header of a message</span></span>](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[<span data-ttu-id="b62ab-199">Obtener la dirección de correo electrónico de un elemento de contacto</span><span class="sxs-lookup"><span data-stu-id="b62ab-199">Get the email address of a Contact item</span></span>](how-to-get-the-email-address-of-a-contact-item.md)
  
[<span data-ttu-id="b62ab-200">Quitar la definición de formulario personalizada que se guarda con un mensaje</span><span class="sxs-lookup"><span data-stu-id="b62ab-200">Remove custom form definition saved with a message</span></span>](how-to-remove-custom-form-definition-saved-with-a-message.md)

