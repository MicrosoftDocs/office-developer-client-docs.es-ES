---
title: Acerca de las propiedades con nombre usadas por Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8c245ec2-bb18-ecf0-b4ad-8c164c5924cf
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: aa4d52d25f120e8b3e2a4c0dcaa4845ad576127a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566232"
---
# <a name="about-named-properties-used-by-outlook"></a>Acerca de las propiedades con nombre usadas por Outlook

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona una utilidad para asignar nombres a determinadas propiedades, para asignar estos nombres a los identificadores �nicos y para hacer que este nombre-a-identificador de asignaci�n persistente entre sesiones. Propiedades con nombre se identifican mediante un nombre y un identificador �nico global (GUID) para un conjunto de propiedades. El nombre puede ser un n�mero o una cadena. Para Microsoft Outlook 2013 o Microsoft Outlook 2010, el conjunto de propiedades a menudo es un espacio de nombres definido por Outlook 2013 o Outlook 2010, como **PSETID_Appointment**. 
  
Named properties are manipulated by using the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function and the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) function. The name and the property set GUID are passed to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) function to obtain a property identifier that is valid for the current MAPI session. Because this property identifier can vary from computer to computer, the only consistent way to access a named property is to know its name and property set GUID. The range for identifiers is always in the 0x8000 and 0xFFFE range. 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Specifically, a MAPI service provider or a MAPI client must implement [IMAPIProp::GetProps](imapiprop-getprops.md) to get values of named properties. Setting named properties used by Outlook 2013 or Outlook 2010 is not supported because of the risk of corrupting data that is shared with other MAPI providers or clients. 
  
Outlook 2013 and Outlook 2010 use MAPI named properties to implement many of their features, for example, attachment security and meeting counter-proposals. Above this underlying data, Outlook 2013 and Outlook 2010 expose some of these properties as item properties in their Outlook 2013 and Outlook 2010 object models. For example, the **Email1Address** property of the **ContactItem** object in the object model corresponds to the named [Propiedad can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) in the **PSETID_Address** namespace. But in general, due to concerns for compatibility and data integrity, many of the MAPI properties that are used by Outlook 2013 and Outlook 2010 are not exposed in the object model. 
  
Esta referencia describe un n�mero de propiedades con nombre que se enumeran a continuaci�n.
  
Propiedades con nombre en el espacio de nombres **PSETID_Address** son los siguientes: 
  
- [Propiedad can�nico de PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propiedad can�nico de PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propiedad can�nico de PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propiedad can�nico de PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propiedad can�nico de PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propiedad can�nico de PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propiedad can�nico de PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Appointment** son los siguientes: 
  
- [Propiedad can�nico de PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propiedad can�nico de PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propiedad can�nico de PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propiedad can�nico de PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propiedad can�nico de PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propiedad can�nico de PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propiedad can�nico de PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propiedad can�nico de PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propiedad can�nico de PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propiedad can�nico de PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Common** son los siguientes: 
  
- [Propiedad can�nico de PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propiedad can�nico de PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propiedad can�nico de PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propiedad can�nico de PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propiedad can�nico de PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propiedad can�nico de PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propiedad can�nico de PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propiedad can�nico de PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propiedad can�nico de PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propiedad can�nico de PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propiedad can�nico de PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propiedad can�nico de PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propiedad can�nico de PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propiedad can�nico de PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Meeting** son los siguientes: 
  
- [Propiedad can�nico de PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Task** son los siguientes: 
  
- [Propiedad can�nico de PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propiedad can�nico de PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propiedad can�nico de PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propiedad can�nico de PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propiedad can�nico de PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propiedad can�nico de PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PS_INTERNET_HEADERS** son los siguientes: 
  
- [Propiedad can�nico de PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Log** son los siguientes: 
  
- [Propiedad can�nico de PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propiedad can�nico de PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propiedad can�nico de PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propiedad can�nico de PidLidLogType](pidlidlogtype-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PS_PUBLIC_STRINGS** son los siguientes: 
  
- [Propiedad can�nico de PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propiedad can�nico de PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Vea tambi�n



[Constantes MAPI](mapi-constants.md)
  
[Determinar si Outlook descarga solo el encabezado de un mensaje](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obtener la dirección de correo electrónico de un elemento de contacto](how-to-get-the-email-address-of-a-contact-item.md)
  
[Quitar la definición de formulario personalizada que se guarda con un mensaje](how-to-remove-custom-form-definition-saved-with-a-message.md)

