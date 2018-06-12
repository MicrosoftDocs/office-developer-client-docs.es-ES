---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816367"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Se aplica a**: Outlook 
  
Inicializa un proveedor de la libreta de direcciones para la operación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Se implementa mediante:  <br/> |Proveedores de la libreta de direcciones  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Sintaxis

 _hInstance_
  
> [entrada] La instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de libreta de direcciones que MAPI utiliza cuando vincula. 
    
 _lpMalloc_
  
> [entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** . El proveedor de la libreta de direcciones que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se utilizará cuando sea necesario por MAPI para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se utilizará cuando sea necesario por MAPI para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará cuando sea necesario por MAPI para liberar memoria. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores. Se puede establecer la marca siguiente:
    
MAPI_NT_SERVICE 
  
> Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario. 
    
 _ulMAPIVer_
  
> [entrada] Número de versión de la interfaz de proveedor de servicios (SPI) que MAPI. Se utiliza el archivo DLL. Para el número de versión actual, vea la MAPISPI. Archivo de encabezado H. 
    
 _lpulProviderVer_
  
> [out] Puntero al número de versión de la SPI que usa este proveedor de libreta de direcciones. 
    
 _lppABProvider_
  
> [out] Puntero a un puntero para el objeto de proveedor de la libreta de direcciones inicializado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_VERSION 
  
> La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.
    
## <a name="remarks"></a>Notas

MAPI llama a la función de punto de entrada **ABProviderInit** para inicializar un proveedor de la libreta de direcciones siguiendo un inicio de sesión de cliente. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Un proveedor de la libreta de direcciones debe implementar **ABProviderInit** como una función de punto de entrada en el archivo DLL del proveedor. La implementación debe basarse en el prototipo de función **ABPROVIDERINIT** , también especificado en MAPISPI. H. MAPI define **ABPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **ABProviderInit** que se deben seguir la convención de llamada CDECL. 
  
Se puede inicializar un proveedor de varias veces, como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil. Debido a que el objeto de proveedor contiene contexto, **ABProviderInit** debe devolver un objeto de proveedor diferente en _lppABProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso. 
  
El proveedor de la libreta de direcciones debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación. En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ . 
  
Para obtener más información sobre cómo escribir **ABProviderInit**, vea [implementar una función de punto de entrada de dirección de la libreta de proveedor](implementing-an-address-book-provider-entry-point-function.md). Para obtener más información sobre las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Ver también

- [IABProvider: IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

