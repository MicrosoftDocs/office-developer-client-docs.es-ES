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
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411998"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpszName_
  
> [in] Puntero al nombre para mostrar del destinatario de la **propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). El  _parámetro lpszName_ puede ser NULL. 
    
 _lpszAdrType_
  
> [in] Puntero al tipo de dirección (como FAX, SMTP o X500) del destinatario. El  _parámetro lpszAdrType_ no puede ser NULL. 
    
 _lpszAddress_
  
> [in] Puntero a la dirección de mensajería del destinatario. El  _parámetro lpszAddress_ no puede ser NULL. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que afecta al destinatario único. Se pueden establecer las siguientes marcas:
    
MAPI_SEND_NO_RICH_INFO 
  
> El destinatario no puede controlar el contenido del mensaje con formato. Si MAPI_SEND_NO_RICH_INFO se establece, MAPI establece la propiedad PR_SEND_RICH_INFO **del** destinatario ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) en FALSE. Si MAPI_SEND_NO_RICH_INFO no se establece, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario señalada por  _lpszAddress_ se interprete como una dirección de Internet. En este caso, MAPI establece **PR_SEND_RICH_INFO** en FALSE. 
    
MAPI_UNICODE 
  
> El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode. Si la MAPI_UNICODE no está establecida, estas cadenas tienen el formato ANSI.
    
 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada del destinatario único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada único se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::CreateOneOff** se implementa para todos los objetos de soporte del proveedor de servicios. Los proveedores de servicios llaman a **CreateOneOff** para crear un identificador de entrada para un destinatario único (un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libreta de direcciones cargados actualmente). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando haya terminado de usar el identificador de entrada devuelto por **CreateOneOff**, liberar la memoria asignada para el identificador de entrada mediante la [función MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="notes-to-transport-providers"></a>Notas a proveedores de transporte

Admite el formato de encapsulación neutro de transporte (TNEF) y usa el valor de la propiedad **PR_SEND_RICH_INFO** para determinar si se va a usar TNEF al transportar un mensaje. No admitir TNEF o no enviar un mensaje en este formato cuando se solicita puede ser un problema para clientes basados en formularios o clientes que requieren propiedades MAPI personalizadas. Esto se debe a que TNEF se usa normalmente para enviar propiedades personalizadas para clases de mensaje personalizadas. 
  
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónica PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

