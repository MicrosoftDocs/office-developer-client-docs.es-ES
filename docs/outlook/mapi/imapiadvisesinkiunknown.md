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
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409569"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Implementa un objeto de receptor de aviso para controlar la notificación. Un puntero a un objeto receptor de aviso se pasa en una llamada al método **Advise** de un proveedor de servicios, el mecanismo usado para registrarse para la notificación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Aconsejar objetos de receptor  <br/> |
|Implementado por:  <br/> |Aplicaciones cliente y MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Responde a una notificación realizando una o varias tareas. Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

