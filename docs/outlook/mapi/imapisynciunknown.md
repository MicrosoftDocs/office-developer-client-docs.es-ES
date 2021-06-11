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
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405597"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona un mecanismo para sincronizar el correo electrónico en lugar de usar la API de transporte. Esta interfaz se expone en un objeto store. Mediante esta interfaz e [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), un proveedor de transporte puede proporcionar mejores mensajes de progreso y error que los que aparecen en el cuadro de diálogo Enviar o recibir en Microsoft Outlook.
  
La bandeja de salida sigue estando en el almacén predeterminado. Outlook seguirá usando las API de transporte para enviar correo porque el mensaje saliente no puede estar en el almacén externo.
  
|||
|:-----|:-----|
|Expuesto por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Proveedores de almacenamiento y transporte  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Implementado por proveedores de almacén de mensajes. Se llama a este método Outlook 2010 y Outlook 2013 para iniciar la sincronización.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

