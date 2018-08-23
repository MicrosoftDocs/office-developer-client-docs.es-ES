---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e85e2da4d63442dc1fb912c5941be9d6f6f53824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593791"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Reasigna un búfer de memoria. Se utiliza con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |omapix.h  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parámetros

 _LPV_
  
> Un puntero a la memoria que se reasignen.
    
 _ulSize_
  
> El tamaño, en bytes, del búfer que se va a asignar.
    
 _lppv_
  
> Un puntero al búfer devuelto asignado.
    
## <a name="remarks"></a>Comentarios

 **MAPIReallocateBuffer** asigna un nuevo bloque de memoria del tamaño solicitado y copia el contenido del búfer que se pasa en este nuevo bloque de memoria. Si el bloque de memoria que se ha pasado contiene punteros internos, los punteros no cambian para que coincida con la nueva ubicación. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIAllocateBuffer](mapiallocatebuffer.md)

