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
# <a name="about-named-properties-used-by-outlook"></a>Información sobre las propiedades con nombre que usa Outlook

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona un lugar para asignar nombres a algunas propiedades, para asignar estos nombres a identificadores únicos y para hacer que esta asociación nombre-a-identificador sea persistentes en todas las sesiones. Las propiedades con nombre se identifican por un nombre y un identificador único global (GUID) para un conjunto de propiedades. El nombre puede ser un número o una cadena. Para Microsoft Outlook 2013 o Microsoft Outlook 2010, el conjunto de propiedades suele ser un espacio de nombres definido por Outlook 2013 o Outlook 2010, como **PSETID_Appointment**. 
  
Las propiedades con nombre se manipulan utilizando las funciones [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). El nombre y el GUID del conjunto de propiedades se pasan a la función [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener un identificador de propiedad que sea válido para la sesión MAPI actual. Como este identificador de propiedad puede variar de un equipo a otro, la única forma consistente para acceder a una propiedad con nombre es conocer el nombre y el GUID del conjunto de propiedades. El intervalo de identificadores está siempre en el rango de 0x8000 y 0xFFFE. 
  
Cualquier objeto que implemente la interfaz [IMAPIProp: IUnknown](imapipropiunknown.md) admite propiedades con nombre. En concreto, un proveedor de servicios MAPI o un cliente MAPI tendrá que implementar [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener los valores de propiedades con nombre. La configuración de propiedades con nombre usada por Outlook 2013 o Outlook 2010 no se admite por el riesgo de que se dañen los datos que se comparten con otros clientes o proveedores MAPI. 
  
Outlook 2013 y Outlook 2010 usan propiedades con nombre MAPI para implementar muchas de sus características, por ejemplo, la seguridad de datos adjuntos y las contrapropuestas de reunión. Por encima de estos datos subyacentes, Outlook 2013 y Outlook 2010 exponen algunas de estas propiedades como propiedades de elementos en sus modelos de objetos de Outlook 2013 y Outlook 2010. Por ejemplo, la propiedad **Email1Address** del objeto **ContactItem** en el modelo de objetos se corresponde con la [Propiedad canónica con nombre PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md) en el espacio de nombres **PSETID_Address**. Pero, en general, debido a posibles problemas de compatibilidad e integridad de datos, muchas de las propiedades MAPI que usan Outlook 2013 y Outlook 2010 no se exponen en el modelo de objetos. 
  
Esta referencia describe una serie de propiedades con nombre que se muestran a continuación.
  
Propiedades con nombre en el espacio de nombres **PSETID_Address** son los siguientes: 
  
- [Propiedad canónica PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)
    
- [Propiedad canónica PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)
    
- [Propiedad canónica PidLidEmail1OriginalEntryId](pidlidemail1originalentryid-canonical-property.md)
    
- [Propiedad canónica PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)
    
- [Propiedad canónica PidLidEmail2DisplayName](pidlidemail2displayname-canonical-property.md)
    
- [Propiedad canónica PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)
    
- [Propiedad canónica PidLidEmail2OriginalDisplayName](pidlidemail2originaldisplayname-canonical-property.md)
    
- [Propiedad canónica PidLidEmail2OriginalEntryId](pidlidemail2originalentryid-canonical-property.md)
    
- [Propiedad canónica PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)
    
- [Propiedad canónica PidLidEmail3DisplayName](pidlidemail3displayname-canonical-property.md)
    
- [Propiedad canónica PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)
    
- [Propiedad canónica PidLidEmail3OriginalDisplayName](pidlidemail3originaldisplayname-canonical-property.md)
    
- [Propiedad canónica PidLidEmail3OriginalEntryId](pidlidemail3originalentryid-canonical-property.md)
    
- [Propiedad canónica PidLidEmail1DisplayName](pidlidemail1displayname-canonical-property.md)
    
- [Propiedad canónica PidLidEmail1OriginalDisplayName](pidlidemail1originaldisplayname-canonical-property.md)
    
- [Propiedad canónica PidLidFileUnder](pidlidfileunder-canonical-property.md)
    
- [Propiedad canónica PidLidInstantMessagingAddress](pidlidinstantmessagingaddress-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)
    
- [Propiedad canónica PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)
    
- [Propiedad canónica PidLidYomiCompanyName](pidlidyomicompanyname-canonical-property.md)
    
- [Propiedad canónica PidLidYomiFirstName](pidlidyomifirstname-canonical-property.md)
    
- [Propiedad canónica PidLidYomiLastName](pidlidyomilastname-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Appointment** son los siguientes: 
  
- [Propiedad canónica PidLidAllAttendeesString](pidlidallattendeesstring-canonical-property.md)
    
- [Propiedad canónica PidLidAppointmentCounterProposal](pidlidappointmentcounterproposal-canonical-property.md)
    
- [Propiedad canónica PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)
    
- [Propiedad canónica PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)
    
- [Propiedad canónica PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)
    
- [Propiedad canónica PidLidBusyStatus](pidlidbusystatus-canonical-property.md)
    
- [Propiedad canónica PidLidCcAttendeesString](pidlidccattendeesstring-canonical-property.md)
    
- [Propiedad canónica PidLidLocation](pidlidlocation-canonical-property.md)
    
- [Propiedad canónica PidLidRecurring](pidlidrecurring-canonical-property.md)
    
- [Propiedad canónica PidLidToAttendeesString](pidlidtoattendeesstring-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Common** son los siguientes: 
  
- [Propiedad canónica PidLidCommonEnd](pidlidcommonend-canonical-property.md)
    
- [Propiedad canónica PidLidCommonStart](pidlidcommonstart-canonical-property.md)
    
- [Propiedad canónica PidLidCompanies](pidlidcompanies-canonical-property.md)
    
- [Propiedad canónica PidLidContacts](pidlidcontacts-canonical-property.md)
    
- [Propiedad canónica PidLidCustomFlag](pidlidcustomflag-canonical-property.md)
    
- [Propiedad canónica PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propiedad canónica PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propiedad canónica PidLidHeaderItem](pidlidheaderitem-canonical-property.md)
    
- [Propiedad canónica PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propiedad canónica PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)
    
- [Propiedad canónica PidLidReminderSet](pidlidreminderset-canonical-property.md)
    
- [Propiedad canónica PidLidReminderTime](pidlidremindertime-canonical-property.md)
    
- [Propiedad canónica PidLidFlagRequest](pidlidflagrequest-canonical-property.md)
    
- [Propiedad canónica PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
- [Propiedad canónica PidLidSmartNoAttach](pidlidsmartnoattach-canonical-property.md)
    
- [Propiedad canónica PidLidToDoTitle](pidlidtodotitle-canonical-property.md)
    
- [Propiedad canónica PidLidUseTnef](pidlidusetnef-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Meeting** son los siguientes: 
  
- [Propiedad canónica PidLidMeetingType](pidlidmeetingtype-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Task** son los siguientes: 
  
- [Propiedad canónica PidLidTaskActualEffort](pidlidtaskactualeffort-canonical-property.md)
    
- [Propiedad canónica PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)
    
- [Propiedad canónica PidLidTaskEstimatedEffort](pidlidtaskestimatedeffort-canonical-property.md)
    
- [Propiedad canónica PidLidTaskFRecurring](pidlidtaskfrecurring-canonical-property.md)
    
- [Propiedad canónica PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)
    
- [Propiedad canónica PidLidTaskStatus](pidlidtaskstatus-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PS_INTERNET_HEADERS** son los siguientes: 
  
- [Propiedad canónica PidTagInternetReturnPath](pidtaginternetreturnpath-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PSETID_Log** son los siguientes: 
  
- [Propiedad canónica PidLidLogDuration](pidlidlogduration-canonical-property.md)
    
- [Propiedad canónica PidLidLogEnd](pidlidlogend-canonical-property.md)
    
- [Propiedad canónica PidLidLogStart](pidlidlogstart-canonical-property.md)
    
- [Propiedad canónica PidLidLogType](pidlidlogtype-canonical-property.md)
    
Propiedades con nombre en el espacio de nombres **PS_PUBLIC_STRINGS** son los siguientes: 
  
- [Propiedad canónica PidNameKeywords](pidnamekeywords-canonical-property.md)
    
- [Propiedad canónica PidNameExchangeJunkEmailMoveStamp](pidnameexchangejunkemailmovestamp-canonical-property.md)
    
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)
  
[Determinar si Outlook descarga solo el encabezado de un mensaje](how-to-determine-if-outlook-downloaded-only-the-header-of-a-message.md)
  
[Obtener la dirección de correo electrónico de un elemento de contacto](how-to-get-the-email-address-of-a-contact-item.md)
  
[Quitar la definición de formulario personalizada que se guarda con un mensaje](how-to-remove-custom-form-definition-saved-with-a-message.md)

