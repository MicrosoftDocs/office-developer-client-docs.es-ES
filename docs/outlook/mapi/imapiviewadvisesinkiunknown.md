---
title: IUnknown IMAPIViewAdviseSink
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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429421"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Recibe notificaciones de los formularios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Ver los objetos del receptor de avisos  <br/> |
|Implementado por:  <br/> |Visores de formularios  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Shutdown](imapiviewadvisesink-onshutdown.md) <br/> |Notifica al visor de formularios que se va a cerrar un formulario.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Notifica al visor de formularios que ya se ha cargado un mensaje nuevo o existente en un formulario.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Notifica al visor del formulario el estado de impresión de un formulario.  <br/> |
|[Enviado](imapiviewadvisesink-onsubmitted.md) <br/> |Notifica al visor de formularios que el mensaje actual se ha enviado al administrador de trabajos en cola de MAPI.  <br/> |
|[OnSave](imapiviewadvisesink-onsaved.md) <br/> |Notifica al visor de formularios que se ha guardado el mensaje actual en un formulario.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

