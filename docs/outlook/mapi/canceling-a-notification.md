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
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816510"
---
# <a name="canceling-a-notification"></a>Cancelar una notificación

  
  
**Hace referencia a**: Outlook 
  
Para cancelar una notificación, los clientes llaman (método) de un origen advise **Unadvise** . Llamar a **Unadvise** es importante debido a que se hace que el proveedor de servicios liberar su referencia a su receptor de notificaciones. Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir el receptor de notificaciones recibir las llamadas de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . De hecho, debido a la naturaleza asincrónica de notificación de eventos, los clientes se pueden notificar incluso después de llamar a una correcta **Unadvise** . Los clientes deben poder controlar la recepción de notificaciones en cualquier momento. 
  
Debido a que difieren de las implementaciones del proveedor de servicio, los clientes que no se llama a **Unadvise** para cancelar una notificación no pueden suponer nada sobre cuando un proveedor liberará a su referencia a su receptor de notificaciones. Algunos proveedores de servicios de liberar sus referencias para receptores con notificación cuando éstos liberan sus orígenes advise. Algunos proveedores de servicios de lo contrario. Como un proveedor de servicios mantiene una referencia a un receptor de notificaciones, puede seguir ese receptor de notificaciones recibir notificaciones. 
  

