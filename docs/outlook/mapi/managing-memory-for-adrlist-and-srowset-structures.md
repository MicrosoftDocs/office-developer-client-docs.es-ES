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
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Administración de memoria para estructuras ADRLIST y SRowSet"

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El requisito de asignar toda la memoria de un búfer siempre que sea posible con una sola llamada **MAPIAllocateBuffer** no se aplica al usar la lista de direcciones, **o ADRLIST**, y el conjunto de filas, o **SRowSet**, estructuras. 
  
Estas dos estructuras son excepciones a las reglas estándar para asignar y liberar memoria. Contienen varios niveles de estructuras y están diseñadas para permitir que los miembros individuales se puedan agregar o quitar. Por lo tanto, cada propiedad debe ser una asignación independiente. 

Donde la mayoría de las estructuras se liberan con una llamada a **MAPIFreeBuffer**, cada entrada individual de una estructura **ADRLIST** o **SRowSet** debe liberarse con su propia llamada a **MAPIFreeBuffer** o una sola llamada a **FreeProws** o **FreePadrlist**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)y [SRowSet](srowset.md). 

**FreeProws** y **FreePadrlist** son funciones proporcionadas por MAPI para simplificar la libertad de estas estructuras de datos. Para obtener más información, [vea FreeProws](freeprows.md) y [FreePadrlist](freepadrlist.md). **FreePadrlist** libera la memoria de la estructura **ADRLIST** más toda la memoria asociada para los miembros de la estructura; **FreeProws hace** lo mismo para la **estructura SRowSet.** 
  
En el diagrama siguiente se muestra el diseño de una estructura de datos **ADRLIST,** que indica las asignaciones de memoria independientes necesarias. Los cuadros grises muestran la memoria que se puede asignar y liberar con una llamada. 
  
**Asignación de memoria de ADRLIST**
  
![Asignación de memoria ADRLIST](media/amapi_52.gif "ADRLIST asignación de memoria ADRLIST")
  
## <a name="see-also"></a>Vea también

- [Administración de memoria en MAPI](managing-memory-in-mapi.md)

