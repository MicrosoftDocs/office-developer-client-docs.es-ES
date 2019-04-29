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
  
Proporciona información de estado acerca del subsistema MAPI, la libreta de direcciones integrada y la cola MAPI. Un proveedor de servicios implementa **IMAPIStatus** para proporcionar información sobre su propio estado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objetos de estado  <br/> |
|Implementado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIStatus  <br/> |
|Tipo de puntero:  <br/> |LPMAPISTATUS  <br/> |
|Modelo de transacción:  <br/> |No transactd  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Muestra una hoja de propiedades que permite al usuario cambiar la configuración de un proveedor de servicios.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifica la contraseña de un proveedor de servicios sin mostrar una interfaz de usuario.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Obliga a que se carguen o descarguen inmediatamente todos los mensajes que esperan ser enviados o recibidos.  <br/> |
   
|**Propiedades requeridas**|**Acceso**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Lectura y escritura  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Lectura y escritura  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

Los objetos de estado que implementa MAPI admiten los métodos siguientes:
  
|**Status (objeto)**|**Métodos admitidos**|
|:-----|:-----|
|Subsistema MAPI  <br/> |Solo **ValidateState**  <br/> |
|Libreta de direcciones MAPI  <br/> |Solo **ValidateState**  <br/> |
|Cola MAPI  <br/> |**ValidateState** y **FlushQueues** <br/> |
   
Los objetos de estado que implementa MAPI deben tener una versión de solo lectura de los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) y para admitir el método **ValidateState** . Los proveedores de transporte también deben ser compatibles con **FlushQueues**. Todos los proveedores deben ser compatibles con **SettingsDialog**; la compatibilidad con **ChangePassword** es opcional. 
  
Los clientes usan objetos de estado para realizar la configuración y para obtener información sobre el estado de la sesión. Tienen acceso a un objeto status mediante una llamada al método **OpenStatusEntry** de un objeto de inicio de sesión de un proveedor de servicios o el método [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para recuperar el objeto status. 
  
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

