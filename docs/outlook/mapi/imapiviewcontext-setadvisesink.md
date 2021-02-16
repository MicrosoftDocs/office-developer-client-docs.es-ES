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
  
Administra el registro de un formulario para recibir notificaciones sobre los cambios en el visor. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parámetros

 _pmvns_
  
> [entrada] Puntero a un objeto receptor de aviso de formulario o NULL.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro o la cancelación de la notificación de formulario se ha registrado correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext::SetAdviseSink** para registrarse y obtener información sobre los cambios en el visor de formularios o cancelar un registro anterior. Cuando  _pmvns se_ establece en NULL, el formulario desea cancelar un registro. Cuando  _pmvns apunta_ a un receptor de aviso de formulario válido, el formulario desea registrarse para futuras notificaciones. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando **SetAdviseSink** incluye un puntero receptor de aviso de formulario, mantenga una referencia a él hasta que se haga otra llamada **SetAdviseSink** para cancelar la notificación. Envíe una notificación cuando se produzca un cambio en el visor y cuando cargue un mensaje nuevo. 
  
Para obtener más información, vea [Enviar y recibir notificaciones de formulario.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementa el **método IMAPIViewContext::SetAdviseSink** en esta función.  <br/> |
   
## <a name="see-also"></a>Consulte también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

