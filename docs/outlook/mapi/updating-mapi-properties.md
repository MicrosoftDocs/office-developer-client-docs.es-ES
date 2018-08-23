---
title: Actualizar las propiedades de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581352"
---
# <a name="updating-mapi-properties"></a>Actualizar las propiedades de MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y proveedores de servicios pueden actualizar un valor de la propiedad llamando:
  
- Un método del objeto [IMAPIProp::SetProps](imapiprop-setprops.md) para actualizar el valor de una o varias de las propiedades de un objeto. 
    
- La función [HrSetOneProp](hrsetoneprop.md) para actualizar una sola propiedad a la vez. Usar **HrSetOneProp** sólo si el objeto de destino es local; Esta función puede provocar una degradación del rendimiento cuando se usa con objetos remotos. 
    
El siguiente procedimiento ilustra cómo usar **SetProps** para actualizar la clase de mensaje o la propiedad PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), de un mensaje. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Para actualizar la clase de mensaje de un mensaje 
  
1. Asignar una estructura de [SPropValue](spropvalue.md) para la clase de mensaje y establecer a sus miembros según corresponda. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Llamar al método **IMAPIProp::SetProps** del mensaje para establecer la nueva clase de mensaje. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

