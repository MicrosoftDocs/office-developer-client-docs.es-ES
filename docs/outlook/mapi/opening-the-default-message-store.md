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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348604"
---
# <a name="opening-the-default-message-store"></a>Abrir el almacén de mensajes predeterminado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En cualquier sesión en particular, un almacén de mensajes actúa como almacén de mensajes predeterminado. Un almacén de mensajes predeterminado tiene las siguientes características:
  
- La propiedad **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) se establece en true.
    
- La marca STATUS_DEFAULT_STORE se establece en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crea automáticamente el subárbol IPM y las carpetas raíz para los resultados de la búsqueda, las vistas comunes y las vistas personales cuando se abre el almacén de mensajes. Para obtener más información acerca de estas carpetas, vea [IPM SUBTREE](ipm-subtree.md) y [MAPI Special folders](mapi-special-folders.md). 
    
Para recuperar el identificador de entrada para el almacén de mensajes predeterminado, debe llamar a [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla de almacén de mensajes y aplicar una restricción adecuada en una llamada a [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** devolverá un conjunto de filas con la fila que representa el almacén de mensajes predeterminado. La restricción que se pasa a **HrQueryAllRows** puede realizarse en una de las siguientes formas: 
  
1. Una restricción **and** que usa una estructura **SAndRestriction** para combinar: 
    
   - Una restricción de EXISTS que usa una estructura **SExistRestriction** para comprobar la existencia de la propiedad **PR_DEFAULT_STORE** . 
    
   - Una restricción de propiedad que usa una estructura [SPropertyRestriction](spropertyrestriction.md) para comprobar el valor true en la propiedad **PR_DEFAULT_STORE** . 
    
2. Una restricción de máscara de subred que usa una estructura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como máscara en la propiedad **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Vea también

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

