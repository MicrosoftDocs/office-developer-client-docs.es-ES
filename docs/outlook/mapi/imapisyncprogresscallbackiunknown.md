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
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593714"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
   
## <a name="see-also"></a>Recursos adicionales



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

