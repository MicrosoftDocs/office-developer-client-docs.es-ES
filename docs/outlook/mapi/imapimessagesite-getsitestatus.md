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
ms.openlocfilehash: 9b804728541b0f2a0499bbf0078bfee2e5aed6ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563810"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve información de un objeto de sitio de mensaje acerca del mensaje de las capacidades del sitio para el mensaje actual.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parámetros

 _lpulStatus_
  
> [out] Un puntero a una máscara de bits de indicadores que proporciona información sobre el estado del mensaje. Se pueden establecer los siguientes indicadores:
    
VCSTATUS_COPY 
  
> Se puede copiar el mensaje. 
    
VCSTATUS_DELETE 
  
> Se puede eliminar el mensaje.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Cuando se elimina, se mueve un mensaje a una carpeta de **Elementos eliminados** en su almacén de mensajes en lugar de que se quita inmediatamente de su almacén de mensajes. 
    
VCSTATUS_MOVE 
  
> Se puede mover el mensaje.
    
VCSTATUS_NEW_MESSAGE 
  
> Se puede crear un nuevo mensaje.
    
VCSTATUS_SAVE 
  
> Se puede guardar el mensaje.
    
VCSTATUS_SUBMIT 
  
> Se puede enviar el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIMessageSite::GetSiteStatus** para obtener las capacidades del objeto de sitio de mensaje para el mensaje actual. Los indicadores devueltos en el parámetro _lpulStatus_ proporcionan información sobre el sitio de mensaje. Normalmente, un formulario habilita o deshabilita los comandos de menú, dependiendo de la información que proporcionan los indicadores acerca de las capacidades de la implementación de sitio de mensaje. Si se carga un nuevo mensaje en un formulario mediante el método [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) o el método [IPersistMessage::Load](ipersistmessage-load.md) , los indicadores de estado deben estar protegidos. Algunos objetos de sitio de mensaje, especialmente objetos de sólo lectura, no permitir los mensajes que se guarden o eliminado. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

El método **IMAPIMessageSite::GetSiteStatus** puede requerir la aplicación de cliente que realice algunos cálculos para determinar qué operaciones pueden o no se puede realizar en el mensaje actual. Normalmente, que implica busca en la fila de estado de proveedor de almacén de mensajes del mensaje actual o consultar el proveedor de almacenamiento para determinar las acciones que puede realizar la aplicación cliente mediante el almacén de mensajes. Por ejemplo, para determinar si se debe devolver el indicador MAPI_DELETE_IS_MOVE, compruebe la mensaje almacén de propiedad del objeto **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) para ver si hay una carpeta de **Elementos eliminados** en el almacén de mensajes. 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI usa el método **IMAPIMessageSite::GetSiteStatus** para obtener el estado del sitio especificado. Puede devolver VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE o VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Vea también



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Propiedad canónico PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

