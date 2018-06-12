---
title: Actualizar las propiedades de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820916"
---
# <a name="updating-mapi-properties"></a>Actualizar las propiedades de MAPI

**Se aplica a**: Outlook 
  
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

## <a name="see-also"></a>Ver también

- [Informaci�n general sobre MAPI (propiedad)](mapi-property-overview.md)

