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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326407"
---
# <a name="canceling-a-notification"></a>Cancelar una notificación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para cancelar una notificación, los clientes llaman al método desaconsejable de un origen de notificaciones. **** Llamar **** a Unadvise es importante porque hace que el proveedor de servicios libere su referencia a su receptor de notificaciones. Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, el receptor de notificaciones puede seguir recibiendo [IMAPIAdviseSink:: BENOTIFY](imapiadvisesink-onnotify.md) calls. De hecho, debido a la naturaleza asincrónica de la notificación de eventos, se puede notificar a los clientes incluso **** después de una llamada de desaconsejar correctamente. Los clientes deben poder administrar la recepción de notificaciones en cualquier momento. 
  
Debido a que las implementaciones del proveedor de servicios son distintas **** , los clientes que no llaman a inaconsejable para cancelar una notificación no pueden asumir nada sobre cuándo un proveedor libera su referencia a su receptor de notificaciones. Algunos proveedores de servicios liberan sus referencias para informar a los receptores cuando liberan sus orígenes de notificaciones. Algunos proveedores de servicios no lo hacen. Siempre que un proveedor de servicios mantenga una referencia a un receptor de notificaciones, el receptor de notificaciones puede seguir recibiendo notificaciones. 
  

