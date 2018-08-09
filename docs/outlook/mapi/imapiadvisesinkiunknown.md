---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817186"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Implementa un objeto de receptor advise para controlar la notificación. Un puntero a un objeto de receptor advise se pasa en la llamada al método **Advise** de un proveedor de servicios, el mecanismo utilizado para registrar la notificación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos del receptor de aviso  <br/> |
|Se implementa mediante:  <br/> |Las aplicaciones cliente y MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Responde a una notificación mediante la realización de una o varias tareas. Las tareas que realiza dependen del tipo de evento y el objeto que genera la notificación.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

