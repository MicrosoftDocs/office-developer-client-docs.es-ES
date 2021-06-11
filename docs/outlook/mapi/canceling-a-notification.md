---
title: Cancelar una notificación
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409765"
---
# <a name="canceling-a-notification"></a>Cancelar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para cancelar una notificación, los clientes llaman al método **Unadvise** de un origen de aviso. Llamar **a Unadvise** es importante porque hace que el proveedor de servicios libere su referencia al receptor de notificaciones. Siempre que un proveedor de servicios mantenga una referencia a un receptor de avisos, el receptor de notificaciones puede seguir recibiendo llamadas [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) De hecho, debido a la naturaleza asincrónica de la notificación de eventos, se puede notificar a los clientes incluso después de una llamada **unadvise** correcta. Los clientes deben poder controlar la recepción de notificaciones en cualquier momento. 
  
Dado que las implementaciones del proveedor de servicios difieren, los clientes que no pueden llamar a **Unadvise** para cancelar una notificación no pueden asumir nada acerca de cuándo un proveedor liberará su referencia al receptor de notificaciones. Algunos proveedores de servicios liberan sus referencias para avisar a los receptores cuando liberan sus orígenes de asesoramiento. Algunos proveedores de servicios no lo hacen. Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, ese receptor de avisos puede seguir recibiendo notificaciones. 
  

