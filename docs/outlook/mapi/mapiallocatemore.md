---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818251"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Hace referencia a**: Outlook 
  
Asigna un búfer de memoria que está vinculado a otro búfer asignado previamente con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parámetros

 _cbSize_
  
> [entrada] Tamaño, en bytes, del búfer de nuevo que se va a asignar. 
    
 _lpObject_
  
> [entrada] Puntero a un búfer MAPI existente asignado mediante **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [out] Puntero para el valor devuelto, recién asignado del búfer.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto un puntero a la memoria solicitada.
    
## <a name="remarks"></a>Comentarios

**MAPIAllocateMore** durante el procesamiento de la llamada, la implementación llamada adquiere un bloque de memoria del sistema operativo. Se asigna el búfer de memoria en una dirección de byte pares. En las plataformas donde el acceso de entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro. 
  
Es la única forma de liberar un búfer asignado con **MAPIAllocateMore** pasar el puntero de búfer especificado en el parámetro _lpObject_ a la función [MAPIFreeBuffer](mapifreebuffer.md) . El vínculo entre los búferes de memoria asignada con [MAPIAllocateBuffer](mapiallocatebuffer.md) y **MAPIAllocateMore** permite **MAPIFreeBuffer** liberar ambos búferes con una sola llamada. 
  

