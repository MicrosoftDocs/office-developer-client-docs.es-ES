---
title: Implementación de una tabla de One-Off proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436296"
---
# <a name="implementing-a-provider-one-off-table"></a>Implementación de una tabla de One-Off proveedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI llama al método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) del proveedor cuando el usuario de una aplicación cliente agrega un destinatario a un mensaje saliente. Normalmente, los tipos de direcciones solicitadas son exclusivos del sistema de mensajería. Si el proveedor admite la creación de destinatarios, debe proporcionar una tabla única que exponga plantillas para cada tipo de dirección de destinatario admitida. Si el proveedor no admite la creación de destinatarios, MAPI_E_NO_SUPPORT de la **llamada GetOneOffTable.** 
  
MAPI normalmente mantendrá abierta la tabla única del proveedor durante la duración de la sesión, liberándose solo cuando un cliente llame al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) del subsistema o de la libreta de direcciones. MAPI se registra para notificaciones en esta tabla de modo que si se agregan o eliminan plantillas, estos cambios se pueden reflejar en el usuario. 
  
 **Para implementar IABLogon::GetOneOffTable**
  
1. Compruebe el valor del parámetro flags,  _ulFlags_. Si la MAPI_UNICODE se establece y el proveedor no admite Unicode, se producirá un error y se devolverá MAPI_E_BAD_CHARWIDTH. 
    
2. Compruebe si ya se ha creado la tabla única del proveedor. Dado que las tablas únicas suelen ser estáticas, el proveedor nunca tiene que pasar por el proceso de creación más de una vez. Si ya existe una tabla, devuelva un puntero a ella. 
    
3. Si aún no existe una tabla única, llame a **CreateTable** para crear una. 
    
4. Establezca las siguientes propiedades para las columnas de las filas de la tabla:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) al nombre del tipo de destinatario que puede crear la plantilla. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) al identificador de entrada de la plantilla de uso único.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar el nivel de jerarquía en la presentación de tabla de un solo usuario.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) a TRUE para indicar si la fila representa una plantilla y FALSE en caso contrario.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) al tipo de dirección creada por la plantilla.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER u otro valor que indica el tipo de presentación de la plantilla.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) a un valor binario único. 
    
5. Llame [a ITableData::HrModifyRow para](itabledata-hrmodifyrow.md) modificar la tabla directamente. 
    
6. Llama [a ITableData::HrGetView para](itabledata-hrgetview.md) crear una implementación de interfaz **IMAPITable** para volver al autor de la llamada. 
    

