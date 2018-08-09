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
ms.openlocfilehash: abee768dd29cc807b605a7d13570a579cb271b2c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817627"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Hace referencia a**: Outlook 
  
Administra el registro de un formulario para recibir las notificaciones sobre cambios en el Visor. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parámetros

 _pmvns_
  
> [entrada] Puntero a un formulario de aviso objeto receptor o NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro o la cancelación de la notificación de formulario que se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llame al método de **IMAPIViewContext::SetAdviseSink** a cualquier registro para obtener información acerca de los cambios en el Visor de formulario o cancelar un registro previo. Cuando _pmvns_ se establece en NULL, el formulario desea cancelar un registro. Cuando los puntos de _pmvns_ a un formulario válido de aviso receptor, el formulario desea registrar para las notificaciones futuras. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando **SetAdviseSink** incluye un formulario de aviso puntero receptor, mantener una referencia a él hasta que se realiza otra llamada **SetAdviseSink** para cancelar la notificación. Enviar una notificación cuando se produce un cambio en el Visor y cuando se carga un nuevo mensaje. 
  
Para obtener más información, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementa el método **IMAPIViewContext::SetAdviseSink** en esta función.  <br/> |
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

