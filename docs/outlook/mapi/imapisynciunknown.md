---
title: IUnknown IMAPISync
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
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341282"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona un mecanismo para sincronizar el correo electrónico en lugar de usar la API de transporte. Esta interfaz se expone en un objeto Store. Mediante esta interfaz y [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), un proveedor de transporte puede proporcionar un mejor progreso y mensajes de error que los que aparecen en el cuadro de diálogo de envío y recepción de Microsoft Outlook.
  
La bandeja de salida sigue en el almacén predeterminado. Outlook seguirá usando las API de transporte para enviar correo, ya que el mensaje saliente no puede estar en el almacén externo.
  
|||
|:-----|:-----|
|Expuesto por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Lo implementan los proveedores de almacenamiento de mensajes. Este método es invocado por Outlook 2010 y Outlook 2013 para iniciar la sincronización.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

