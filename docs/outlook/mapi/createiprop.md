---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406811"
---
# <a name="createiprop"></a>CreateIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de datos de propiedad, es decir, un objeto [IPropData](ipropdataimapiprop.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> a Puntero a un identificador de interfaz (IID) para el objeto de datos de la propiedad. El identificador de interfaz válido es IID_IMAPIPropData. Pasar NULL en el parámetro _lpInterface_ también hace que el objeto de datos de propiedad devuelto en el parámetro _lppPropData_ se convierta en la interfaz estándar de un objeto de datos de propiedad. 
    
 _lpAllocateBuffer_
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
 _lpAllocateMore_
  
> a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se va a usar para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _lpvReserved_
  
> [entrada] Reservado; debe ser cero. 
    
 _lppPropData_
  
> contempla Puntero a un puntero al objeto de datos de la propiedad devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> La interfaz solicitada no es compatible con este objeto.
    
## <a name="remarks"></a>Comentarios

Los parámetros de entrada _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)y [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Una aplicación de cliente que llama a **CreateIProp** pasa los punteros a las funciones de MAPI con nombre simplemente; un proveedor de servicios pasa los punteros a estas funciones que recibió en su llamada de inicialización o que se recuperaron con una llamada al método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) 
  

