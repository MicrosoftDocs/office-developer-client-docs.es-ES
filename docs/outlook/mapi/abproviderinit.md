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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428287"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa un proveedor de libreta de direcciones para su funcionamiento. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Proveedores de libreta de direcciones  <br/> |
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

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Instancia de la biblioteca de vínculos dinámicos (DLL) del proveedor de libreta de direcciones que MAPI usó cuando se vinculó. 
    
 _lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.** Es posible que el proveedor de libreta de direcciones necesite usar este método de asignación al trabajar con determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará cuando sea necesario por MAPI para asignar memoria. 
    
 _lpAllocateMore_
  
> [in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará cuando sea necesario por MAPI para asignar memoria adicional. 
    
 _lpFreeBuffer_
  
> [in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará cuando sea necesario por MAPI para liberar memoria. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas. Se puede establecer la siguiente marca:
    
MAPI_NT_SERVICE 
  
> El proveedor se está cargando en el contexto de un servicio Windows, un tipo especial de proceso sin acceso a ninguna interfaz de usuario. 
    
 _ulMAPIVer_
  
> [in] Número de versión de la interfaz del proveedor de servicios (SPI) que MAPI.DLL usa. Para el número de versión actual, vea MAPISPI. Archivo de encabezado H. 
    
 _lpulProviderVer_
  
> [salida] Puntero al número de versión del SPI que usa este proveedor de libreta de direcciones. 
    
 _lppABProvider_
  
> [salida] Puntero a un puntero al objeto de proveedor de libreta de direcciones inicializada.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_VERSION 
  
> La versión SPI que usa MAPI no es compatible con el SPI que usa este proveedor.
    
## <a name="remarks"></a>Comentarios

MAPI llama a la función de punto de **entrada ABProviderInit para** inicializar un proveedor de libreta de direcciones después de un inicio de sesión de cliente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Un proveedor de libreta de direcciones debe implementar **ABProviderInit** como una función de punto de entrada en la DLL del proveedor. La implementación debe basarse en el prototipo de función **ABPROVIDERINIT,** también especificado en MAPISPI.H. MAPI define **ABPROVIDERINIT para** usar el tipo de llamada de inicialización MAPI estándar, STDMAPIINITCALLTYPE, lo que hace que **ABProviderInit** siga la convención de llamada CDECL. 
  
Un proveedor se puede inicializar varias veces, como resultado de aparecer en varios perfiles en uso simultáneo o de aparecer más de una vez en el mismo perfil. Dado que el objeto provider contiene contexto, **ABProviderInit** debe devolver un objeto de proveedor diferente en  _lppABProvider_ para cada inicialización, incluso para varias inicializaciones en el mismo proceso. 
  
El proveedor de libreta de direcciones debe usar las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la asignación y desasignación de memoria. En particular, el proveedor debe usar estas funciones para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Si el proveedor también espera usar el asignador de memoria OLE, debe llamar al método **IUnknown::AddRef** del objeto de asignador al que apunta el parámetro _lpMalloc._ 
  
Para obtener más información sobre cómo escribir **ABProviderInit**, vea [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md). Para obtener más información sobre las funciones de punto de entrada, vea [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Vea también

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

