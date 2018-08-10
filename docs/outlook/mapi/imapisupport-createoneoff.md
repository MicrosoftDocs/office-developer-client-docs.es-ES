---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1cfd4afbda5892e96a1d74ca56f4a6d1f98e2268
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817474"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Hace referencia a**: Outlook 
  
Crea un identificador de entrada para una dirección de uso único.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpszName_
  
> [entrada] Un puntero para el nombre para mostrar del destinatario de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). El parámetro _lpszName_ puede ser NULL. 
    
 _lpszAdrType_
  
> [entrada] Un puntero para el tipo de dirección (por ejemplo, FAX, SMTP o X500) del destinatario. El parámetro _lpszAdrType_ no puede ser NULL. 
    
 _lpszAddress_
  
> [entrada] Un puntero a la dirección de mensajería del destinatario. El parámetro _lpszAddress_ no puede ser NULL. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que influye en el destinatario de uso único. Se pueden establecer los siguientes indicadores:
    
MAPI_SEND_NO_RICH_INFO 
  
> El destinatario no puede controlar el contenido del mensaje con formato. Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad del destinatario **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE. Si MAPI_SEND_NO_RICH_INFO no está establecido, MAPI establece esta propiedad en TRUE, a menos que se interpreta la dirección del destinatario mensajería indicada por _lpszAddress_ para que sea una dirección de Internet. En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
    
MAPI_UNICODE. 
  
> El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., estas cadenas se encuentran en formato ANSI.
    
 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicada por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada para el destinatario de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente el identificador de entrada único.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::CreateOneOff** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamar a **CreateOneOff** para crear un identificador de entrada para un destinatario de uso único (un destinatario que no pertenezcan a cualquiera de los contenedores desde cualquiera de los proveedores de la libreta de direcciones cargada actualmente). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando haya terminado con el identificador de entrada devuelto por **CreateOneOff**, libere la memoria asignada para el identificador de entrada mediante el uso de la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Notas para los proveedores de transporte

Admitir el formato de encapsulación neutro de transporte (TNEF) y usar el valor de la propiedad **PR_SEND_RICH_INFO** para determinar si debe usar TNEF al transportar un mensaje. No se admite la codificación TNEF o no enviar un mensaje con este formato cuando lo solicita puede ser un problema para los clientes basada en formularios o los clientes que requieren las propiedades personalizadas de MAPI. Esto es debido a que TNEF normalmente se usa para enviar las propiedades personalizadas para las clases de mensaje personalizadas. 
  
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónica PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

