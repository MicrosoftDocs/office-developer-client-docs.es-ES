---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430129"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve información de un objeto de sitio de mensaje acerca de las capacidades del sitio de mensaje para el mensaje actual.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [salida] Puntero a una máscara de bits de marcas que proporciona información sobre el estado del mensaje. Se pueden establecer las siguientes marcas:
    
VCSTATUS_COPY 
  
> El mensaje se puede copiar. 
    
VCSTATUS_DELETE 
  
> El mensaje se puede eliminar.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Cuando se elimina, un mensaje se mueve a una **carpeta Elementos** eliminados en su almacén de mensajes en lugar de quitarse inmediatamente de su almacén de mensajes. 
    
VCSTATUS_MOVE 
  
> El mensaje se puede mover.
    
VCSTATUS_NEW_MESSAGE 
  
> Se puede crear un mensaje nuevo.
    
VCSTATUS_SAVE 
  
> El mensaje se puede guardar.
    
VCSTATUS_SUBMIT 
  
> El mensaje se puede enviar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los objetos Form llaman **al método IMAPIMessageSite::GetSiteStatus** para obtener las capacidades del objeto de sitio de mensaje para el mensaje actual. Las marcas devueltas en el  _parámetro lpulStatus_ proporcionan información sobre el sitio del mensaje. Normalmente, un formulario habilita o deshabilita los comandos de menú, en función de la información que proporcionan las marcas sobre las capacidades de la implementación del sitio del mensaje. Si el método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) o el método [IPersistMessage::Load](ipersistmessage-load.md) cargan un nuevo mensaje en un formulario, se deben comprobar las marcas de estado. Algunos objetos de sitio de mensajes, especialmente los objetos de solo lectura, no permiten que los mensajes se guarden o eliminen. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El **método IMAPIMessageSite::GetSiteStatus** puede requerir que la aplicación cliente realice algún cálculo para determinar qué operaciones se pueden o no se pueden realizar en el mensaje actual. Normalmente, esto implica ver la fila de estado del proveedor de almacén de mensajes del mensaje actual o consultar al proveedor de almacenamiento para determinar qué acciones puede realizar la aplicación cliente mediante el almacén de mensajes. Por ejemplo, para determinar si se devuelve la marca MAPI_DELETE_IS_MOVE, compruebe la propiedad **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) del objeto del almacén de mensajes para ver si hay una carpeta **Elementos** eliminados en el almacén de mensajes. 
  
Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI usa el **método IMAPIMessageSite::GetSiteStatus** para obtener el estado del sitio especificado. Puede devolver VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE o VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Vea también



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propiedad canónica PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

