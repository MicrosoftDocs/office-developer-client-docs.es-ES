---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817572"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Pase el proveedor de almacenamiento como un campo de la estructura MAPISIB durante una llamada a [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). El proveedor de almacenamiento usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> ||
|Expuestos por:  <br/> |Outlook  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Proveedores de almacén  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |El proveedor de almacenamiento periódicamente llama a esta función para actualizar el estado en el cuadro de diálogo de envío o recepción.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo de envío o recepción.  <br/> |
|[Hecho](imapisyncprogresscallback-done.md) <br/> |El proveedor de almacenamiento llama a esta función para notificar a Outlook que se ha completado la sincronización.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

