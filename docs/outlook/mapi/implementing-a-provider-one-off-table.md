---
title: Implementación de una tabla de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332868"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementación de una tabla de un proveedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI llama al método [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) del proveedor cuando el usuario de una aplicación cliente agrega un destinatario a un mensaje saliente. Normalmente, los tipos de direcciones que se solicitan son únicos para el sistema de mensajería. Si el proveedor admite la creación de destinatarios, debe proporcionar una tabla única que exponga las plantillas para cada tipo de dirección de destinatario compatible. Si su proveedor no admite la creación de destinatarios, devuelva MAPI_E_NO_SUPPORT de la llamada a **GetOneOffTable** . 
  
MAPI suele mantener abierta la tabla única del proveedor durante el período de duración de la sesión, que la libera solo cuando un cliente llama al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) de la libreta de direcciones o del subsistema. MAPI registra las notificaciones en esta tabla de modo que, si se agregan o se eliminan plantillas, estos cambios se pueden reflejar en el usuario. 
  
 **Para implementar IABLogon:: GetOneOffTable**
  
1. Compruebe el valor del parámetro flags, _ulFlags_. Si se establece la marca MAPI_UNICODE y el proveedor no admite Unicode, se produce un error y se devuelve MAPI_E_BAD_CHARWIDTH. 
    
2. Compruebe si ya se ha creado la tabla de uso único del proveedor. Como las tablas de uso único suelen ser estáticas, el proveedor nunca tiene que pasar por el proceso de creación más de una vez. Si ya existe una tabla, devuelva un puntero a ella. 
    
3. Si aún no existe una tabla de uso único, llame a **createTable** para crear una. 
    
4. Establezca las siguientes propiedades para las columnas de las filas de la tabla:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el nombre del tipo de destinatario que la plantilla puede crear. 
    
  - **** Es ([PidTagEntryId](pidtagentryid-canonical-property.md)) al identificador de entrada de la plantilla única.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar el nivel de jerarquía en la visualización de la tabla de un solo uso.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) en true para indicar si la fila representa una plantilla y false en caso contrario.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) al tipo de dirección creada por la plantilla.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER u otro valor que indique el tipo de presentación de la plantilla.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) a un valor binario único. 
    
5. Llame a [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) para modificar la tabla directamente. 
    
6. Llame a [ITableData:: HrGetView](itabledata-hrgetview.md) para crear una implementación de la interfaz **IMAPITable** para volver a la persona que llama. 
    

