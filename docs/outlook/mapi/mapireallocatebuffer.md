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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435288"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Reallocates a un búfer de memoria. Se usa con la [función MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |omapix.h  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parameters

 _lpv_
  
> Puntero a la memoria que se va a reasignar.
    
 _ulSize_
  
> Tamaño, en bytes, del búfer que se va a asignar.
    
 _lppv_
  
> Puntero al búfer asignado devuelto.
    
## <a name="remarks"></a>Comentarios

 **MAPIReallocateBuffer** asigna un nuevo bloque de memoria del tamaño solicitado y copia el contenido del búfer que se pasa a este nuevo bloque de memoria. Si el bloque de memoria que se pasa contiene punteros internos, los punteros no cambian para que coincidan con la nueva ubicación. 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)

