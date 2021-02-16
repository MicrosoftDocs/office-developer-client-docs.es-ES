---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415540"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recupera las direcciones de las funciones de asignación y desasignación de memoria MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parámetros

 _lppAllocateBuffer_
  
> [salida] Puntero a un puntero a la **función MAPIAllocateBuffer.** **MAPIAllocateBuffer** asigna memoria. 
    
 _lppAllocateMore_
  
> [salida] Puntero a un puntero a la **función MAPIAllocateMore.** **MAPIAllocateMore** asigna memoria adicional para la memoria que se asignó originalmente mediante **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> [salida] Puntero a un puntero a la **función MAPIFreeBuffer.** **MAPIFreeBuffer** libera memoria. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las direcciones de función se devolvieron correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::GetMemAllocRoutines** se implementa para todos los objetos de compatibilidad. Los proveedores de servicios llaman a **GetMemAllocRoutines** para obtener las direcciones de las tres funciones de asignación de memoria que se pasan a su función de inicialización ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)o [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Consulte también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

