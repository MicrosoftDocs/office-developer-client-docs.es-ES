---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589087"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona un mecanismo para sincronizar el correo electrónico en lugar de usar la API de transporte. Esta interfaz se expone en un objeto de almacén. Mediante el uso de esta interfaz y [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), un proveedor de transporte puede proporcionar un mejor progreso y mensajes de error que los que aparecen en el cuadro de diálogo de envío o recepción en Microsoft Outlook.
  
La Bandeja de salida aún está en el almacén predeterminado. Outlook seguirán usando las API de transporte para enviar correo porque no puede ser el mensaje saliente en el almacén externo.
  
|||
|:-----|:-----|
|Expuestos por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementada por los proveedores de almacén de mensajes. Este método es llamado por Outlook 2010 y Outlook 2013 para iniciar la sincronización.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

