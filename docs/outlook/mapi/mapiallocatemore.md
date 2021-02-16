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
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435393"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Asigna un búfer de memoria que está vinculado a otro búfer asignado anteriormente con la [función MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parámetros

 _cbSize_
  
> [entrada] Tamaño, en bytes, del nuevo búfer que se asignará. 
    
 _lpObject_
  
> [entrada] Puntero a un búfer MAPI existente asignado mediante **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [salida] Puntero al búfer recién asignado devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha hecho correctamente y ha devuelto un puntero a la memoria solicitada.
    
## <a name="remarks"></a>Comentarios

Durante **el procesamiento de llamadas MAPIAllocateMore,** la implementación de llamada adquiere un bloque de memoria del sistema operativo. El búfer de memoria se asigna en una dirección de bytes par. En plataformas en las que el acceso entero largo es más eficaz, el sistema operativo asigna el búfer en una dirección cuyo tamaño en bytes es un múltiplo de cuatro. 
  
La única forma de liberar un búfer asignado con **MAPIAllocateMore** es pasar el puntero del búfer especificado en el parámetro _lpObject_ a la [función MAPIFreeBuffer.](mapifreebuffer.md) El vínculo entre los búferes de memoria asignados con [MAPIAllocateBuffer](mapiallocatebuffer.md) y **MAPIAllocateMore** permite a **MAPIFreeBuffer** liberar ambos búferes con una sola llamada. 
  

