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
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817556"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Hace referencia a**: Outlook 
  
Convierte el identificador de entrada interno de un almacén de mensajes en un identificador de entrada con el formato estándar de MAPI.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Parámetros

 _cbOrigEntry_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> [entrada] Un puntero al identificador de entrada privada para el almacén de mensajes.
    
 _lpcbWrappedEntry_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> [out] Un puntero a un puntero para el identificador de entrada ajustado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada correctamente ajustado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::WrapStoreEntryID** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de usar **WrapStoreEntryID** para que MAPI genera un identificador de entrada para un almacén de mensajes que se ajusta el identificador de entrada interno de la tienda. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando un cliente llama (método) [IMAPIProp::GetProps](imapiprop-getprops.md) de su almacén de mensajes recuperar su propiedad **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) y el almacén de mensajes usa un identificador de entrada en un formato privado, llamada **WrapStoreEntryID **y devolver el identificador de entrada indicado por el parámetro _lppWrappedEntry_ . 
  
Las llamadas a los métodos [IMSProvider::Logon](imsprovider-logon.md) y [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) siempre obtención el identificador de entrada privada de la tienda; se usa la versión ajustada sólo entre las aplicaciones de cliente y MAPI. 
  
Libere la memoria para el identificador de entrada que apunta el parámetro _lppWrappedEntry_ mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) cuando haya terminado con el identificador de entrada. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

