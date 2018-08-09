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
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817511"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Hace referencia a**: Outlook 
  
Recupera las direcciones de la memoria de asignación y cancelación de asignación de funciones de MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Parámetros

 _lppAllocateBuffer_
  
> [out] Un puntero a un puntero a la función **MAPIAllocateBuffer** . **MAPIAllocateBuffer** asigna memoria. 
    
 _lppAllocateMore_
  
> [out] Un puntero a un puntero a la función **MAPIAllocateMore** . **MAPIAllocateMore** asigna memoria adicional para la memoria que se asignó originalmente mediante el uso de **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> [out] Un puntero a un puntero a la función **MAPIFreeBuffer** . **MAPIFreeBuffer** libera memoria. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las direcciones de función correctamente se han devuelto.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::GetMemAllocRoutines** se implementa para todos los objetos de soporte técnico. Proveedores de servicios de llamar a **GetMemAllocRoutines** para obtener las direcciones de las funciones de asignación de tres memoria que se pasan a su función de inicialización ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)o [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>Vea también



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

