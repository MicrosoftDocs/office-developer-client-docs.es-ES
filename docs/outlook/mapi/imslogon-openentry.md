---
title: IMSLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenEntry
api_type:
- COM
ms.assetid: 612cbab7-60cb-48bb-906e-18d9135e7a86
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 544aaaace18a9d26972e6484803b63a1ee7060fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416303"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar acceso adicional. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulOpenFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero a la dirección del identificador de entrada de la carpeta o el objeto de mensaje que se debe abrir. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) del objeto. Pasar NULL indica que el objeto se convierte en la interfaz estándar para dicho objeto. El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto. 
    
 _ulOpenFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre el objeto. Se pueden establecer las siguientes marcas:
    
MAPI_BEST_ACCESS 
  
> El objeto debe abrirse con los permisos máximos permitidos para el usuario y los permisos máximos de la aplicación cliente. Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto se abre con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el objeto se abre con permiso de solo lectura. El cliente puede recuperar el nivel de permisos **obteniendo la propiedad PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> Se permite que la llamada se realiza correctamente incluso si el objeto subyacente no está disponible para la aplicación que realiza la llamada. Si el objeto no está disponible, una llamada posterior al objeto puede devolver un error.
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se crean con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [salida] Puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [salida] Puntero al puntero al objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método IMSLogon::OpenEntry** para abrir una carpeta o un mensaje en un almacén de mensajes. MAPI pasa el identificador de entrada del objeto que se debe abrir. El proveedor del almacén de mensajes debe devolver un puntero que permita un acceso adicional al objeto especificado en el _parámetro lppUnk._ 
  
Antes de que MAPI llame a **IMSLogon::OpenEntry,** primero determina que el identificador de entrada de carpeta o mensaje determinado coincide con uno registrado por este proveedor de almacén de mensajes. Para obtener más información acerca de cómo los proveedores de almacenamiento registran identificadores de entrada, vea [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** es idéntico al método [IMsgStore::OpenEntry](imsgstore-openentry.md) del objeto de almacén de mensajes, excepto que el cliente no llama a **IMSLogon::OpenEntry**; MAPI llama **a IMSLogon::OpenEntry** cuando procesa un **método IMAPISession::OpenEntry.** Los objetos abiertos mediante **IMSLogon::OpenEntry** deben tratarse exactamente igual que los objetos abiertos mediante el objeto de almacén de mensajes; en particular, los objetos abiertos mediante esta llamada deben invalidarse cuando se libera el objeto de almacén de mensajes. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

