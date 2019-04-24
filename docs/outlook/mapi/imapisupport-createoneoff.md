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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322407"
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
  
> a Un puntero al nombre para mostrar del destinatario la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). El parámetro _lpszName_ puede ser null. 
    
 _lpszAdrType_
  
> a Un puntero al tipo de dirección (como FAX, SMTP o X500) del destinatario. El parámetro _lpszAdrType_ no puede ser nulo. 
    
 _lpszAddress_
  
> a Un puntero a la dirección de mensajería del destinatario. El parámetro _lpszAddress_ no puede ser nulo. 
    
 _ulFlags_
  
> a Máscara de bits de marcas que afecta al destinatario de uso único. Se pueden establecer los siguientes indicadores:
    
MAPI_SEND_NO_RICH_INFO 
  
> El destinatario no puede controlar el contenido del mensaje con formato. Si se establece MAPI_SEND_NO_RICH_INFO, MAPI establece la propiedad **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) del destinatario en false. Si no se establece MAPI_SEND_NO_RICH_INFO, MAPI establece esta propiedad en TRUE a menos que la dirección de mensajería del destinatario apuntado por _lpszAddress_ se interprete como una dirección de Internet. En este caso, MAPI establece **PR_SEND_RICH_INFO** en false. 
    
MAPI_UNICODE 
  
> El nombre para mostrar, el tipo de dirección y la dirección están en formato Unicode. Si no se establece la marca MAPI_UNICODE, estas cadenas están en formato ANSI.
    
 _lpcbEntryID_
  
> contempla Un puntero al número de bytes en el identificador de entrada al que apunta el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> contempla Un puntero a un puntero al identificador de entrada para el destinatario de uso único.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente el identificador de entrada de un solo uso.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: CreateOneOff** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios llaman a **CreateOneOff** para crear un identificador de entrada para un destinatario de un solo uso (un destinatario que no pertenece a ninguno de los contenedores de ninguno de los proveedores de libreta de direcciones cargados actualmente). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando termine de usar el identificador de entrada devuelto por **CreateOneOff**, libere la memoria asignada para el identificador de entrada mediante la función [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Notas para los proveedores de transporte

Admitir el formato de encapsulamiento neutro para el transporte (TNEF) y usar el valor de la propiedad **PR_SEND_RICH_INFO** para determinar si se va a usar TNEF al transportar un mensaje. Si no admite TNEF o no envía un mensaje en este formato cuando se solicite, puede ser un problema para los clientes basados en formularios o clientes que requieran propiedades MAPI personalizadas. Esto se debe a que TNEF suele usarse para enviar propiedades personalizadas para clases de mensaje personalizadas. 
  
## <a name="see-also"></a>Vea también



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propiedad canónica PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

