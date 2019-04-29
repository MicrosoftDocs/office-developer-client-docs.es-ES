---
title: Administrar memoria para ADRLIST y estructuras SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407868"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Administración de la memoria para las estructuras ADRLIST y SRowSet "

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El requisito de asignar toda la memoria para un búfer siempre que sea posible con una única llamada de **MAPIAllocateBuffer** no se aplica cuando se usan las estructuras de la lista de direcciones, o **ADRLIST**, o **SRowSet**. 
  
Estas dos estructuras son excepciones a las reglas estándar para la asignación y liberación de la memoria. Contienen varios niveles de estructuras y están diseñados para permitir que se agreguen o eliminen miembros individuales. Por lo tanto, cada propiedad debe ser una asignación independiente. 

Cuando la mayoría de las estructuras se liberan con una llamada a **MAPIFreeBuffer**, cada entrada individual de una estructura **ADRLIST** o **SRowSet** debe liberarse con su propia llamada a **MAPIFreeBuffer** o una sola llamada a **FreeProws** o ** FreePadrlist**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)y [SRowSet](srowset.md). 

**FreeProws** y **FreePadrlist** son funciones que proporciona MAPI para simplificar la liberación de estas estructuras de datos. Para obtener más información, vea [FreeProws](freeprows.md) y [FreePadrlist](freepadrlist.md). **FreePadrlist** libera la memoria de la estructura **ADRLIST** más toda la memoria asociada a los miembros de la estructura; **FreeProws** hace lo mismo para la estructura **SRowSet** . 
  
En el siguiente diagrama se muestra el diseño de una estructura de datos de **ADRLIST** , que indica las asignaciones de memoria independientes necesarias. Los cuadros grises muestran memoria que se puede asignar y liberar con una llamada. 
  
**Asignación de memoria de ADRLIST**
  
![Asignación de memoria de ADRLIST] (media/amapi_52.gif "Asignación de memoria de ADRLIST")
  
## <a name="see-also"></a>Ver también

- [Administración de memoria en MAPI](managing-memory-in-mapi.md)

