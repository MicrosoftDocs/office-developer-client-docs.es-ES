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
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428539"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa un proveedor de transporte para su operación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Proveedores de transporte  <br/> |
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

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de transporte que MAPI usó cuando cargó el DLL.
    
 _lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.** Es posible que el proveedor de transporte necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
 _lpAllocateMore_
  
> [in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas. Se puede establecer la siguiente marca:
    
MAPI_NT_SERVICE 
  
> El proveedor se está cargando en el contexto de un servicio Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario. 
    
 _ulMAPIVer_
  
> [in] Número de versión de la interfaz del proveedor de servicios (SPI) que Mapi.dll usa. Para el número de versión actual, vea el archivo de encabezado Mapispi.h. 
    
 _lpulProviderVer_
  
> [salida] Puntero al número de versión del SPI que usa este proveedor de transporte. 
    
 _lppXPProvider_
  
> [salida] Puntero a un puntero al objeto del proveedor de transporte inicializado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_VERSION 
  
> La versión SPI que usa MAPI no es compatible con el SPI que usa este proveedor.
    
## <a name="remarks"></a>Comentarios

MAPI llama a la función de punto de **entrada XPProviderInit para** inicializar un proveedor de transporte después de un inicio de sesión de cliente. **XPProviderInit** se llama una vez para cada proveedor de transporte especificado en el perfil del cliente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Un proveedor de transporte debe implementar **XPProviderInit** como una función de punto de entrada en la DLL del proveedor. La implementación debe basarse en el prototipo de función **XPPROVIDERINIT,** también especificado en Mapispi.h. MAPI define **XPPROVIDERINIT para** usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, lo que hace que **XPProviderInit** siga la convención de llamada CDECL. Una ventaja de CDECL es que las llamadas se pueden intentar incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos. 
  
Un proveedor se puede inicializar varias veces como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil. Dado que el objeto provider contiene contexto, **XPProviderInit** debe devolver un objeto de proveedor diferente en  _lppXPProvider para_ cada inicialización, incluso para varias inicializaciones en el mismo proceso. 
  
El proveedor de transporte debe usar las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la asignación y desasignación de memoria. En particular, el proveedor debe usar estas funciones para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._ 
  
Para obtener más información acerca de cómo escribir **XPProviderInit**, vea [Initializing the Transport Provider](initializing-the-transport-provider.md). Para obtener más información acerca de las funciones de punto de entrada, vea [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Vea también



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

