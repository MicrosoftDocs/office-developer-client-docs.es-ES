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
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817561"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Hace referencia a**: Outlook 
  
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
   
## <a name="see-also"></a>Vea también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

