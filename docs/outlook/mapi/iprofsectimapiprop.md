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
ms.openlocfilehash: a8152a9cad7623a077cd9df3f678a9ada56e3960
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577964"
---
# <a name="iprofsect--imapiprop"></a>IProfSect : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Funciona con las propiedades de objetos de sección de perfil. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Expuestos por:  <br/> |Objetos de sección de perfil  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Identificador de interfaz:  <br/> |IID_IProfSect  <br/> |
|Tipo de puntero:  <br/> |LPPROFSECT  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

Esta interfaz no tiene ningún método único.
  
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="notes-to-callers"></a>Notas para los llamadores

La interfaz **IProfSect** no tiene ningún método único, pero se puede llamar al perfil de los métodos de la sección [IMAPIProp](imapipropiunknown.md) . Existen algunas diferencias entre la implementación de **IProfSect** y otras implementaciones de **IMAPIProp**:
  
- **IProfSect** no es compatible con un modelo de transacción. 
    
- **IProfSect** no es compatible con las propiedades con nombre. 
    
- **IProfSect** se reserva el intervalo de identificadores de 0x67F0 a 0x67ff para propiedades seguras. 
    
No se admite un modelo de transacción significa que todos los cambios que se han realizado en una siguiente de sección de perfil llamadas a la [IMAPIProp::CopyProps](imapiprop-copyprops.md) y métodos de [IMAPIProp::CopyTo](imapiprop-copyto.md) se producen inmediatamente. Las llamadas al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) correctamente, pero en realidad no guardar los cambios. 
  
Para estar protegidos contra los cambios que se producen de forma prematura, proveedores de servicios necesitan realizar copias de sus perfiles en las secciones que se muestran a los usuarios a través de las hojas de propiedades. Las hojas de propiedades deben trabajar con la copia, en lugar de la sección de perfil real. Cuando el usuario hace clic en el botón **Aceptar** para comprobar que los cambios son precisos, se pueden guardar los cambios a la sección de perfil real. 
  
Para implementar una hoja de propiedades mediante el uso de una sección de perfil copiado, use el procedimiento siguiente:
  
1. Abra la sección de perfil llamando al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) o [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . 
    
2. Llame a la función [CreateIProp](createiprop.md) para recuperar un objeto de datos de propiedades: un objeto que admite la interfaz **IPropData** . 
    
3. Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar las propiedades que aparecerán en la hoja de propiedades de la sección de perfil para el objeto de datos de propiedad. 
    
4. Llame al método [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) para solicitar que el proveedor de servicios de mostrar una hoja de propiedades y pase un puntero al objeto de datos de propiedad en el parámetro _lpConfigData_ . 
    
5. Cuando el usuario guarda los cambios realizados a las propiedades de configuración en la hoja de propiedades, llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) para copiar las propiedades del objeto de datos de la propiedad a la sección de perfil. 
    
En las secciones, a diferencia de otros objetos de perfiles, no admiten las propiedades con nombre. Los métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) devuelven MAPI_E_NO_SUPPORT si se les llama en un objeto de sección de perfil. Si se utiliza el método [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer los identificadores de propiedades en el intervalo por encima de 0 x 8000, se devuelve el tipo de propiedad PT_ERROR. 
  
Las secciones del perfil reservan el intervalo de identificadores de 0x67F0 a 0x67FF para propiedades seguras. Proveedores de servicios pueden utilizar este intervalo para almacenar contraseñas y otras credenciales específicas del proveedor. No se devuelven las propiedades de este intervalo en la lista completa de propiedades cuando se pasa NULL en el parámetro _lpPropTag_ del método [IMAPIProp::GetProps](imapiprop-getprops.md) , ni tampoco se devuelven en el parámetro _lppPropTagArray_ de la [ IMAPIProp::GetPropList](imapiprop-getproplist.md) (método). Propiedades seguras deben solicitarse específicamente por sus identificadores. 
  
MAPI proporciona una sección de perfil con la MUID_PROFILE_INSTANCE constante codificado de forma rígida como su identificador y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como su propiedad único. MAPI se asegura de que el valor de la propiedad **PR_SEARCH_KEY** será único entre todos los perfiles creados. Use **PR_SEARCH_KEY** en lugar de **PR_PROFILE_NAME** cuando unicidad es importante, ya que es posible para un perfil eliminado ser seguido por otro perfil con el mismo nombre. 
  
Para obtener más información acerca de cómo usar las secciones del perfil, vea [administración de perfiles y servicios de mensajes](administering-profiles-and-message-services.md).
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

