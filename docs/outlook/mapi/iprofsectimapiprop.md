---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406601"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Funciona con las propiedades de los objetos de sección de perfil. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Expuesto por:  <br/> |Objetos de sección de perfil  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IProfSect  <br/> |
|Tipo de puntero:  <br/> |LPPROFSECT  <br/> |
|Modelo de transacciones:  <br/> |No transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="notes-to-callers"></a>Notas para los llamadores

La **interfaz IProfSect** no tiene métodos únicos, pero puede llamar a los métodos [IMAPIProp](imapipropiunknown.md) de la sección de perfil. Existen algunas diferencias entre la implementación **de IProfSect** y otras implementaciones de **IMAPIProp:**
  
- **IProfSect** no admite un modelo de transacciones. 
    
- **IProfSect** no admite propiedades con nombre. 
    
- **IProfSect** reserva el intervalo de identificadores 0x67F0 para 0x67ff propiedades seguras. 
    
No admitir un modelo de transacciones significa que todos los cambios realizados en una sección de perfil después de las llamadas a los [métodos IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md) se producen inmediatamente. Las llamadas al [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) se realizaron correctamente, pero en realidad no guarda ningún cambio. 
  
Para protegerse de los cambios que se producen prematuramente, los proveedores de servicios deben realizar copias de sus secciones de perfil que se muestran a los usuarios a través de hojas de propiedades. Las hojas de propiedades deben funcionar con la copia, en lugar de la sección de perfil real. Cuando el usuario hace clic en el **botón Aceptar** para comprobar que los cambios son precisos, los cambios se pueden guardar en la sección de perfil real. 
  
Para implementar una hoja de propiedades mediante una sección de perfil copiado, use el siguiente procedimiento:
  
1. Abra la sección de perfil llamando al [método IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) o [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) 
    
2. Llame a [la función CreateIProp](createiprop.md) para recuperar un objeto de datos de propiedad, un objeto que admite la **interfaz IPropData.** 
    
3. Llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar las propiedades que aparecerán en la hoja de propiedades de la sección de perfil en el objeto de datos de propiedad. 
    
4. Llame al método [IMAPISupport::D oConfigPropSheet](imapisupport-doconfigpropsheet.md) para solicitar que el proveedor de servicios muestre una hoja de propiedades y pase un puntero al objeto de datos de propiedad en el parámetro _lpConfigData._ 
    
5. Cuando el usuario guarda los cambios en las propiedades de configuración en la hoja de propiedades, llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) para copiar las propiedades del objeto de datos de propiedad de nuevo a la sección de perfil. 
    
Las secciones de perfil, a diferencia de otros objetos, no admiten propiedades con nombre. Los [métodos IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) devuelven MAPI_E_NO_SUPPORT si se les llama en un objeto de sección de perfil. Si usa el método [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer identificadores de propiedad en el intervalo anterior a 0x8000, se devolverá el tipo de propiedad PT_ERROR propiedad. 
  
Las secciones de perfil reservan el intervalo de 0x67F0 para 0x67FF propiedades seguras. Los proveedores de servicios pueden usar este rango para almacenar contraseñas y otras credenciales específicas del proveedor. Las propiedades de este intervalo no se devuelven en la lista completa de propiedades cuando se pasa NULL en el parámetro _lpPropTag_ del método [IMAPIProp::GetProps,](imapiprop-getprops.md) ni se devuelven en el parámetro _lppPropTagArray_ del método [IMAPIProp::GetPropList.](imapiprop-getproplist.md) Las propiedades seguras deben ser solicitadas específicamente por sus identificadores. 
  
MAPI proporciona una sección de perfil con la constante codificada de forma MUID_PROFILE_INSTANCE como su identificador y PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como su única propiedad. MAPI garantiza que el valor **PR_SEARCH_KEY** propiedad será único entre todos los perfiles creados. Use **PR_SEARCH_KEY** en lugar **de PR_PROFILE_NAME** cuando la singularidad es importante, ya que es posible que un perfil eliminado esté seguido de otro perfil con el mismo nombre. 
  
Para obtener más información acerca de cómo usar las secciones de perfil, vea [Administering Profiles and Message Services](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

