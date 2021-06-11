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
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436030"
---
# <a name="opening-the-default-message-store"></a>Abrir el almacén de mensajes predeterminado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En cualquier sesión en particular, un almacén de mensajes actúa como almacén de mensajes predeterminado. Un almacén de mensajes predeterminado tiene las siguientes características:
  
- La **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) se establece en TRUE.
    
- La STATUS_DEFAULT_STORE se establece en la **propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crea automáticamente el subárbol IPM y las carpetas raíz para resultados de búsqueda, vistas comunes y vistas personales cuando se abre el almacén de mensajes. Para obtener más información acerca de estas carpetas, vea [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md). 
    
Para recuperar el identificador de entrada del almacén de mensajes predeterminado, debe llamar a [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla del almacén de mensajes y aplicar una restricción adecuada en una llamada a [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** devolverá un conjunto de filas con la fila que representa el almacén de mensajes predeterminado. La restricción que se pasa a **HrQueryAllRows** puede tener uno de los siguientes formularios: 
  
1. Una **restricción AND** que usa una estructura **SAndRestriction** para combinar: 
    
   - Existe una restricción que usa una **estructura SExistRestriction** para probar la existencia de la **PR_DEFAULT_STORE** propiedad. 
    
   - Una restricción de propiedad que usa una [estructura SPropertyRestriction](spropertyrestriction.md) para buscar el valor TRUE en la **PR_DEFAULT_STORE** propiedad. 
    
2. Una restricción de máscara de bits que usa una estructura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como máscara en la **PR_RESOURCE_FLAGS** propiedad. 
    
## <a name="see-also"></a>Vea también

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

