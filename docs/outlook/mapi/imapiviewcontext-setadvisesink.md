---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419397"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra el registro de un formulario para recibir notificaciones sobre cambios en el visor. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parameters

 _pmvns_
  
> a Puntero a un objeto receptor de notificaciones de formulario o NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro o la cancelación de la notificación del formulario se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext:: SetAdviseSink** para registrarse para obtener información sobre los cambios en el visor de formularios o cancelar un registro anterior. Cuando _pmvns_ se establece en null, el formulario desea cancelar un registro. Cuando _pmvns_ apunta a un receptor de formulario válido, el formulario desea registrarse para notificaciones futuras. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando **SetAdviseSink** incluye un puntero para notificar al receptor, mantenga una referencia al mismo hasta que se realice otra llamada a **SetAdviseSink** para cancelar la notificación. Envíe una notificación cuando se produzca un cambio en el visor y cuando cargue un mensaje nuevo. 
  
Para obtener más información, consulte [enviar y recibir notificaCiones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SetAdviseSink  <br/> |MFCMAPI implementa el método **IMAPIViewContext:: SetAdviseSink** en esta función.  <br/> |
   
## <a name="see-also"></a>Ver también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

