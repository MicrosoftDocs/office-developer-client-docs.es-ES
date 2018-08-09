---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820999"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Hace referencia a**: Outlook 
  
Inicializa un proveedor de transporte para la operación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Se implementa mediante:  <br/> |Proveedores de transporte  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Parámetros

 _hInstance_
  
> [entrada] La instancia de la biblioteca de vínculos dinámicos del proveedor de transporte (DLL) que MAPI utilizada cuando carga el archivo DLL.
    
 _lpMalloc_
  
> [entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** . El proveedor de transporte que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**. 
    
 _lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de indicadores. Se puede establecer la marca siguiente:
    
MAPI_NT_SERVICE 
  
> Se está cargando el proveedor en el contexto de un servicio de Windows, un tipo especial de proceso sin acceso a cualquier interfaz de usuario. 
    
 _ulMAPIVer_
  
> [entrada] Número de versión de la interfaz de proveedor de servicio (SPI) que usa MAPI.. Para el número de versión actual, vea el archivo de encabezado Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Puntero al número de versión de la SPI que usa este proveedor de transporte. 
    
 _lppXPProvider_
  
> [out] Puntero a un puntero al objeto de proveedor de transporte inicializado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_VERSION 
  
> La versión SPI usada por MAPI no es compatible con el SPI usado por este proveedor.
    
## <a name="remarks"></a>Comentarios

MAPI llama a la función de punto de entrada **XPProviderInit** para inicializar un proveedor de transporte después de un inicio de sesión de cliente. **XPProviderInit** se llama una vez para cada proveedor de transporte especificado en el perfil del cliente. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Un proveedor de transporte debe implementar **XPProviderInit** como una función de punto de entrada en el archivo DLL del proveedor. La implementación debe basarse en el prototipo de función **XPPROVIDERINIT** , también especificado en Mapispi.h. MAPI define **XPPROVIDERINIT** para usar el tipo de llamada de inicialización estándar MAPI, STDMAPIINITCALLTYPE, que hace que **XPProviderInit** que se deben seguir la convención de llamada CDECL. Una ventaja de CDECL es que se pueden intentar llamadas incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos. 
  
Un proveedor se puede inicializar varias veces como consecuencia de que aparezca en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil. Debido a que el objeto de proveedor contiene contexto, **XPProviderInit** debe devolver un objeto de proveedor diferente en _lppXPProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso. 
  
El proveedor de transporte debe usar las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación. En concreto, el proveedor debe usar estas funciones para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Si el proveedor también espera utilizar el asignador de memoria OLE, debe llamar al método **IUnknown:: AddRef** del objeto asignador indicado por el parámetro _lpMalloc_ . 
  
Para obtener más información acerca de cómo escribir **XPProviderInit**, vea [inicializar el proveedor de transporte](initializing-the-transport-provider.md). Para obtener más información acerca de las funciones de punto de entrada, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Vea también



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

