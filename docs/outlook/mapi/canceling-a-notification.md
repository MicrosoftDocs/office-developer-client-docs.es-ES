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
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564776"
---
# <a name="canceling-a-notification"></a>Cancelar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para cancelar una notificación, los clientes llaman (método) de un origen advise **Unadvise** . Llamar a **Unadvise** es importante debido a que se hace que el proveedor de servicios liberar su referencia a su receptor de notificaciones. Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir el receptor de notificaciones recibir las llamadas de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . De hecho, debido a la naturaleza asincrónica de notificación de eventos, los clientes se pueden notificar incluso después de llamar a una correcta **Unadvise** . Los clientes deben poder controlar la recepción de notificaciones en cualquier momento. 
  
Debido a que difieren de las implementaciones del proveedor de servicio, los clientes que no se llama a **Unadvise** para cancelar una notificación no pueden suponer nada sobre cuando un proveedor liberará a su referencia a su receptor de notificaciones. Algunos proveedores de servicios de liberar sus referencias para receptores con notificación cuando éstos liberan sus orígenes advise. Algunos proveedores de servicios de lo contrario. Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir ese receptor de notificaciones recibir notificaciones. 
  

