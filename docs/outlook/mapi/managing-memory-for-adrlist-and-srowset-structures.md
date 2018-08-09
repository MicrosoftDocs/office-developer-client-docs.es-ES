---
title: Administración de la memoria para las estructuras ADRLIST y SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ab582b869fb5a53d7ac4e97e039d9bde4a4f0430
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818058"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Administración de la memoria para las estructuras ADRLIST y SRowSet"

**Hace referencia a**: Outlook 
  
El requisito de asignar toda la memoria para un búfer siempre que sea posible con una sola llamada **MAPIAllocateBuffer** no se aplica cuando se usa la lista de direcciones, o las estructuras de **ADRLIST**y el conjunto de filas o **SRowSet**. 
  
Estos dos estructuras son excepciones a las reglas estándares para asignar y liberar memoria. Contienen varios niveles de estructuras y están diseñados para permitir que se agreguen o eliminen miembros individuales. Por lo tanto, cada propiedad debe ser una asignación independiente. 

Donde se libera la mayoría de las estructuras con una llamada a **MAPIFreeBuffer**, cada entrada individual de una estructura de **ADRLIST** o **SRowSet** se debe liberar con su propia llamada a **MAPIFreeBuffer** o una sola llamada a **FreeProws** o ** FreePadrlist**. Para obtener más información, vea [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)y [SRowSet](srowset.md). 

**FreeProws** y **FreePadrlist** son funciones proporcionadas por MAPI para simplificar la liberación de estas estructuras de datos. Para obtener más información, vea [FreeProws](freeprows.md) y [FreePadrlist](freepadrlist.md). **FreePadrlist** libera la memoria para la estructura **ADRLIST** más la memoria de todos los asociados para los miembros de la estructura; **FreeProws** hace lo mismo para la estructura **SRowSet** . 
  
En el siguiente diagrama muestra el diseño de una estructura de datos **ADRLIST** , que indica las asignaciones de memoria independientes necesarias. Los cuadros gris muestran de memoria que puede se asignan y liberan con una llamada. 
  
**Asignación de memoria de ADRLIST**
  
![Memoria de adrlist] (media/amapi_52.gif "Memoria de adrlist")
  
## <a name="see-also"></a>Vea también

- [Administración de memoria en MAPI](managing-memory-in-mapi.md)

