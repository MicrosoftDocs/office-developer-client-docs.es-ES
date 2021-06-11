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
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408302"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información de estado sobre el subsistema MAPI, la libreta de direcciones integrada y la cola MAPI. Un proveedor de servicios implementa **IMAPIStatus para** proporcionar información sobre su propio estado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos de estado  <br/> |
|Implementado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIStatus  <br/> |
|Tipo de puntero:  <br/> |LPMAPISTATUS  <br/> |
|Modelo de transacciones:  <br/> |No transacted  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Muestra una hoja de propiedades que permite al usuario cambiar la configuración de un proveedor de servicios.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Fuerza a que todos los mensajes que esperan ser enviados o recibidos se carguen o descarguen inmediatamente.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lectura/escritura  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Los objetos de estado que implementa MAPI admiten los métodos siguientes:
  
|**Status (objeto)**|**Métodos admitidos**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState** only  <br/> |
|Libreta de direcciones MAPI  <br/> |**ValidateState** only  <br/> |
|Cola MAPI  <br/> |**ValidateState** y **FlushQueues** <br/> |
   
Los objetos de estado que implementa MAPI son necesarios para tener una versión de solo lectura de los métodos de la [interfaz IMAPIProp](imapipropiunknown.md) y para admitir el **método ValidateState.** Los proveedores de transporte también deben **admitir FlushQueues**. Todos los proveedores deben admitir **SettingsDialog**; La compatibilidad **con ChangePassword** es opcional. 
  
Los clientes usan objetos de estado para realizar la configuración y para obtener información sobre el estado de la sesión. Obtienen acceso a un objeto de estado llamando al método **OpenStatusEntry** de un objeto de inicio de sesión del proveedor de servicios o al método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar el objeto status. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

