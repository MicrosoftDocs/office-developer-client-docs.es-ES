---
title: Actualización de propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407525"
---
# <a name="updating-mapi-properties"></a>Actualización de propiedades MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y proveedores de servicios pueden actualizar un valor de propiedad llamando a:
  
- Método [IMAPIProp::SetProps](imapiprop-setprops.md) de un objeto para actualizar el valor de una o varias de las propiedades de un objeto. 
    
- La [función HrSetOneProp](hrsetoneprop.md) para actualizar solo una propiedad a la vez. Use **HrSetOneProp** solo si el objeto de destino es local; esta función puede provocar una degradación del rendimiento cuando se usa con objetos remotos. 
    
El siguiente procedimiento ilustra cómo usar **SetProps** para actualizar la clase de mensaje o PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de un mensaje. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Para actualizar la clase de mensaje de un mensaje 
  
1. Asigne una [estructura SPropValue](spropvalue.md) para la clase de mensaje y establezca sus miembros según corresponda. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Llame al método **IMAPIProp::SetProps** del mensaje para establecer la nueva clase de mensaje. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

