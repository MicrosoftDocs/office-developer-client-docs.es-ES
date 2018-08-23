---
title: Implementar una tabla puntual de proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f484174bd0a83c9bb874bec4896fe3dd925405c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568241"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementar una tabla puntual de proveedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI llama al método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de su proveedor cuando el usuario de una aplicación cliente agrega un destinatario a un mensaje saliente. Normalmente, los tipos de direcciones que se solicitó son únicos para el sistema de mensajería. Si el proveedor admite la creación de destinatarios, debe proporcionar una tabla de uso único que expone las plantillas para cada tipo de dirección del destinatario compatible. Si su proveedor no admite la creación de destinatarios, devolver MAPI_E_NO_SUPPORT de la llamada **GetOneOffTable** . 
  
MAPI normalmente se conserve que tabla de uso único de su proveedor abierta para la duración de la sesión, liberarlo sólo cuando un cliente llama del subsistema o (método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) ) de la libreta de direcciones. MAPI se registra para las notificaciones en esta tabla, por lo que si se agregan o se eliminan las plantillas, pueden reflejarán estos cambios al usuario. 
  
 **Para implementar IABLogon::GetOneOffTable**
  
1. Compruebe el valor del parámetro flags, _ulFlags_. Si se establece el indicador MAPI_UNICODE y su proveedor no admite Unicode, se producirá un error y devolver MAPI_E_BAD_CHARWIDTH. 
    
2. Compruebe si ya se creó la tabla de uso único de su proveedor. Debido a que las tablas de uso único son normalmente estáticas, su proveedor nunca tiene que pasar por el proceso de creación de más de una vez. Si ya existe una tabla, devuelve un puntero a ella. 
    
3. Si todavía no existe una tabla de uso único, llame a **CreateTable** para crear uno. 
    
4. Establezca las siguientes propiedades para las columnas en las filas de tabla:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el nombre del tipo de destinatario que puede crear la plantilla. 
    
  - **Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para el identificador de entrada para la plantilla de uso único.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar el nivel de jerarquía en la visualización de la tabla de uso único.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) en TRUE para indicar si la fila representa una plantilla y FALSE en caso contrario.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para el tipo de dirección creado por la plantilla.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) a DT_MAILUSER o cualquier otro valor que indica el tipo de presentación para la plantilla.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) a un único valor binario. 
    
5. Llame a [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar directamente en la tabla. 
    
6. Llame a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una implementación de interfaz **IMAPITable** para volver al autor de la llamada. 
    

