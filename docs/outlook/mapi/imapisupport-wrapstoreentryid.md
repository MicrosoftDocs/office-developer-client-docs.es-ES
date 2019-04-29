---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430451"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada en el formato MAPI estándar.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Parameters

 _cbOrigEntry_
  
> a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> a Un puntero al identificador de entrada privada para el almacén de mensajes.
    
 _lpcbWrappedEntry_
  
> contempla Un puntero al recuento de bytes en el identificador de entrada al que apunta el parámetro _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> contempla Un puntero a un puntero al identificador de entrada ajustado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada se ha ajustado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: WrapStoreEntryID** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios usan **WrapStoreEntryID** para que MAPI genere un identificador de entrada para un almacén de mensajes que ajuste el identificador de entrada interno de la tienda. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando un cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar su propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y el almacén de mensajes utiliza un identificador de entrada en un formato privado, llame a **WrapStoreEntryID **y devolver el identificador de entrada al que apunta el parámetro _lppWrappedEntry_ . 
  
Las llamadas a los métodos [IMSProvider:: Logon](imsprovider-logon.md) y [IMSLogon:: CompareEntryIDs](imslogon-compareentryids.md) siempre obtienen el identificador de entrada privada del almacén; la versión empaquetada solo se usa entre aplicaciones cliente y MAPI. 
  
Libere la memoria del identificador de entrada al que apunta el parámetro _lppWrappedEntry_ mediante la función [MAPIFreeBuffer](mapifreebuffer.md) cuando termine de usar el identificador de entrada. 
  
## <a name="see-also"></a>Ver también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

