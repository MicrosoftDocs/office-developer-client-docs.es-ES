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
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418340"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Pasa el proveedor de almacén como un campo en la estructura MAPISIB durante una llamada a [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md). El proveedor de la tienda usa esta interfaz para proporcionar comentarios a Microsoft Outlook sobre el estado de la sincronización.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> ||
|Expuesto por:  <br/> |Outlook  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Proveedores de la Tienda  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |El proveedor de almacenamiento llama periódicamente a esta función para actualizar el estado en el cuadro de diálogo De envío o recepción.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función para proporcionar detalles que se muestran en el cuadro de diálogo De envío o recepción.  <br/> |
|[Hecho](imapisyncprogresscallback-done.md) <br/> |El proveedor de almacenamiento llama a esta función para informar a Outlook de que la sincronización se ha completado.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

