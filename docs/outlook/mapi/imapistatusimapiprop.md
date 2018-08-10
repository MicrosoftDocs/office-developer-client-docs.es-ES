---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817473"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Hace referencia a**: Outlook 
  
Proporciona información de estado sobre el subsistema MAPI, la libreta de direcciones integrada y la cola de MAPI. Un proveedor de servicios implementa **IMAPIStatus** para proporcionar información sobre su propio estado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de estado  <br/> |
|Se implementa mediante:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIStatus  <br/> |
|Tipo de puntero:  <br/> |LPMAPISTATUS  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios.  <br/> |
|[Diálogo Configuración](imapistatus-settingsdialog.md) <br/> |Muestra una hoja de propiedades que permite al usuario que cambie la configuración de un proveedor de servicios.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifica la contraseña de un proveedor de servicios sin mostrar la interfaz de usuario.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Obliga a todos los mensajes en espera de ser enviados o recibidos para cargarse o descargarse inmediatamente.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Los objetos de estado que implementa MAPI admiten los siguientes métodos:
  
|**Objeto de estado**|**Métodos admitidos**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState**  <br/> |
|Libreta de direcciones MAPI  <br/> |**ValidateState**  <br/> |
|Cola MAPI  <br/> |**ValidateState** y **FlushQueues** <br/> |
   
Los objetos de estado que implementa MAPI son necesarios para tener una versión de solo lectura de los métodos de la interfaz de [IMAPIProp](imapipropiunknown.md) y para admitir el método **ValidateState** . Los proveedores de transporte también deben admitir **FlushQueues**. Todos los proveedores deben admitir **diálogo Configuración**; soporte técnico para **ChangePassword** es opcional. 
  
Los clientes usan los objetos de estado para realizar la configuración y para obtener más información sobre el estado de la sesión. Tienen acceso a un objeto de estado llamando al método **OpenStatusEntry** de un objeto de inicio de sesión del proveedor de servicio o el método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar el objeto de estado. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

