---
title: Abrir el almacén de mensajes predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0366e889f1c63e5fe40760ca80cec701cd6b3713
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573540"
---
# <a name="opening-the-default-message-store"></a>Abrir el almacén de mensajes predeterminado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En cualquier sesión en particular, un almacén de mensajes actúa como almacén de mensajes predeterminado. Un almacén de mensajes predeterminado tiene las siguientes características:
  
- La propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) está establecida en TRUE.
    
- El indicador STATUS_DEFAULT_STORE se establece en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crea automáticamente el subárbol IPM y las carpetas raíz de resultados de búsqueda, vistas comunes y vistas personales cuando se abre el almacén de mensajes. Para obtener más información acerca de estas carpetas, vea [Subárbol IPM](ipm-subtree.md) y [Las carpetas especiales de MAPI](mapi-special-folders.md). 
    
Para recuperar el identificador de entrada para el almacén de mensajes de forma predeterminada, se debe llamar a [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla de almacén de mensajes y aplicar una restricción adecuada en una llamada a [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** devolverá un conjunto con la fila que representa el almacén de mensajes predeterminado de filas. Puede tomar la restricción que se pase a **HrQueryAllRows** en uno de los siguientes formatos: 
  
1. Una restricción **y** que usa una estructura de **SAndRestriction** para combinar: 
    
   - Una restricción que usa una estructura de **SExistRestriction** para probar la existencia de la propiedad **PR_DEFAULT_STORE** de existe. 
    
   - Una restricción de propiedad que utiliza una estructura de [SPropertyRestriction](spropertyrestriction.md) para comprobar el valor TRUE en la propiedad **PR_DEFAULT_STORE** . 
    
2. Una restricción de máscara de bits que usa una estructura de [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como una máscara con respecto a la propiedad **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Recursos adicionales

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

