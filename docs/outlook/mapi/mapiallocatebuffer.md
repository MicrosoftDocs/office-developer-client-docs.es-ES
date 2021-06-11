---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425697"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un búfer de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parameters

 _cbSize_
  
> [in] Tamaño, en bytes, del búfer que se va a asignar. 
    
 _lppBuffer_
  
> [salida] Puntero al búfer asignado devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha hecho correctamente y ha devuelto el búfer de memoria solicitado.
    
## <a name="remarks"></a>Comentarios

Durante **el procesamiento de llamadas MAPIAllocateBuffer,** la implementación de llamada adquiere un bloque de memoria del sistema operativo. El búfer de memoria se asigna en una dirección de bytes numerada par. En plataformas donde el acceso a enteros largos es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro. 
  
Al llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) se libera el búfer de memoria asignado por **MAPIAllocateBuffer**, llamando a la función [MAPIAllocateMore](mapiallocatemore.md) y a los búferes vinculados a él, cuando la memoria ya no es necesaria. 
  
## <a name="see-also"></a>Vea también



[MAPIReallocateBuffer](mapireallocatebuffer.md)

