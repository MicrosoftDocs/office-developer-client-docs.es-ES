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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579602"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un búfer de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parámetros

 _cbSize_
  
> [entrada] Tamaño, en bytes, del búfer que se va a asignar. 
    
 _lppBuffer_
  
> [out] Puntero al búfer devuelto asignado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el búfer de memoria solicitada.
    
## <a name="remarks"></a>Comentarios

**MAPIAllocateBuffer** durante el procesamiento de la llamada, la implementación llamada adquiere un bloque de memoria del sistema operativo. Se asigna el búfer de memoria en una dirección de byte pares. En las plataformas donde el acceso de entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro. 
  
Llamar a las versiones de la función [MAPIFreeBuffer](mapifreebuffer.md) el búfer de memoria asignado por **MAPIAllocateBuffer**, mediante una llamada a la función [MAPIAllocateMore](mapiallocatemore.md) y los búferes vinculado a él, cuando ya no se necesita la memoria. 
  
## <a name="see-also"></a>Recursos adicionales



[MAPIReallocateBuffer](mapireallocatebuffer.md)

