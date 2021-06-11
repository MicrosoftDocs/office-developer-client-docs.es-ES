---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416240"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa un proveedor de almacén de mensajes para su operación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de almacenamiento de mensajes que MAPI usó cuando se vinculó. 
    
 _lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.** Es posible que el proveedor del almacén de mensajes necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**. 
    
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
  
> [in] Número de versión de la interfaz del proveedor de servicios (SPI) que utiliza MAPI. Para el número de versión actual, vea el archivo de encabezado Mapispi.h. 
    
 _lpulProviderVer_
  
> [salida] Puntero al número de versión del SPI que usa este proveedor de almacén de mensajes. 
    
 _lppMSProvider_
  
> [salida] Puntero a un puntero al objeto de proveedor del almacén de mensajes inicializado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_VERSION 
  
> La versión SPI que usa MAPI no es compatible con el SPI que usa este proveedor.
    
## <a name="remarks"></a>Comentarios

MAPI llama a la función de punto de entrada **MSProviderInit para** inicializar un proveedor de almacén de mensajes después de un inicio de sesión de cliente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Un proveedor de almacén de mensajes debe implementar **MSProviderInit** como una función de punto de entrada en la DLL del proveedor. La implementación debe basarse en el prototipo de función **MSPROVIDERINIT,** también especificado en MAPISPI.H. MAPI define **MSPROVIDERINIT para** usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, lo que hace que **MSProviderInit** siga la convención de llamada CDECL. Una ventaja de CDECL es que las llamadas se pueden intentar incluso si el número de parámetros de llamada no coincide con el número de parámetros definidos. 
  
Un proveedor se puede inicializar varias veces, como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil. Dado que el objeto provider contiene contexto, **MSProviderInit** debe devolver un objeto de proveedor diferente en  _lppMSProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso. 
  
El DLL del proveedor no debe vincularse con Mapix.dll. En su lugar, debe usar estos punteros para la asignación de memoria o la desasignación. 
  
El proveedor del almacén de mensajes debe usar las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la asignación y desasignación de memoria. En particular, el proveedor debe usar estas funciones para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._ 
  
Para obtener más información acerca de cómo **escribir MSProviderInit,** vea [Loading Message Store Providers](loading-message-store-providers.md). Para obtener más información acerca de las funciones de punto de entrada, vea [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Vea también



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

