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
ms.openlocfilehash: 619357a608dd160cbe4811cc7db7ae3b392db858
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576893"
---
# <a name="imslogonopenentry"></a>IMSLogon::OpenEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se abre una carpeta o un objeto de mensaje y devuelve un puntero al objeto para proporcionar más acceso. 
  
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

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero a la dirección del identificador de entrada del objeto de carpeta o mensaje para abrir. 
    
 _lpInterface_
  
> [entrada] Un puntero para el identificador de interfaz (IID) para el objeto. Pasar un valor NULL indica que el objeto se convierte en la interfaz estándar para este tipo de objeto. El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el objeto. 
    
 _ulOpenFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto. Se pueden establecer los siguientes indicadores:
    
MAPI_BEST_ACCESS 
  
> El objeto se debe abrir con los permisos máximos permitidos para el usuario y los permisos de la aplicación cliente máximo. Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se abre el objeto con permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, el objeto se abre con permiso de sólo lectura. El cliente puede recuperar el nivel de permisos mediante la obtención de la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_DEFERRED_ERRORS 
  
> Se autoriza la llamada se realice correctamente, incluso si el objeto subyacente no está disponible para la aplicación de llamada. Si el objeto no está disponible, una llamada posterior al objeto devolverá un error.
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se crean con permiso de sólo lectura, y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lpulObjType_
  
> [out] Un puntero al tipo del objeto abierto.
    
 _lppUnk_
  
> [out] Un puntero al puntero para el objeto abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

MAPI llama al método **IMSLogon::OpenEntry** para abrir una carpeta o un mensaje en un almacén de mensajes. MAPI pasa el identificador de entrada del objeto que se va a abrir. El proveedor de almacén de mensajes debe devolver un puntero que permite obtener acceso al objeto especificado en el parámetro _lppUnk_ . 
  
Antes de MAPI llama a **IMSLogon::OpenEntry**, primero determina que el mensaje determinado o el identificador de entrada de carpeta coincide con uno registrado por este proveedor de almacén de mensajes. Para obtener más información acerca de cómo registran los proveedores de almacén los identificadores de entrada, vea [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
  
 **IMSLogon::OpenEntry** es idéntico al método [IMsgStore::OpenEntry](imsgstore-openentry.md) del objeto de almacén de mensaje, excepto en que el cliente no llama a **IMSLogon::OpenEntry**; Las llamadas de MAPI **IMSLogon::OpenEntry** cuando se procesa un método **IMAPISession::OpenEntry** . Objetos abiertos mediante el uso de **IMSLogon::OpenEntry** deben ser exactamente el mismo se trata como objetos abiertos utilizando el mensaje almacenan el objeto; en concreto, objetos abiertos mediante el uso de esta llamada deben invalidarse cuando se libera el objeto de almacén de mensajes. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

