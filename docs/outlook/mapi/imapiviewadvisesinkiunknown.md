---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567191"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recibe las notificaciones de formularios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Vista de aviso receptor objetos  <br/> |
|Se implementa mediante:  <br/> |Visores de formulario  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Se notifica al Visor de formulario que se está cerrando un formulario.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Se notifica al Visor de formulario que ha cargado un nuevo o un mensaje existente en un formulario.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Se notifica el Visor de formulario del estado de impresión de un formulario.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Se notifica al Visor de formulario que se ha enviado el mensaje actual a la cola de MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Se notifica el Visor de formulario que se ha guardado el mensaje actual en un formulario.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

