---
title: Controlar la notificación de la tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816955"
---
# <a name="handling-table-notification"></a>Controlar la notificación de la tabla

**Hace referencia a**: Outlook 
  
Como alternativa al registro directamente con un objeto de origen advise, como una carpeta o un usuario de mensajería, un cliente puede registrar para recibir notificaciones en un contenido o una tabla de jerarquía. Seguimiento de cambios de dirección libreta entradas, carpetas y mensajes a través de un contenido o tabla de jerarquía puede ser más sencilla y más sencillo que a través de los objetos individuales. 

Por ejemplo, puede llamar a [IMAPITable::Advise](imapitable-advise.md) en la tabla de jerarquía de la carpeta para detectar cuando se producen cambios en una de sus subcarpetas. Si admite la visualización de mensajes remotos, registrar con la tabla de estado para observar la actividad por los proveedores de transporte y la cola de MAPI. 
  
Sin embargo, no siempre es preferible usar notificaciones de tabla en lugar de las notificaciones del objeto. Supervisión de los cambios en el número de mensajes en una carpeta es un ejemplo de cuando el cliente que necesite registrar para las notificaciones de objeto en una carpeta en lugar de una tabla de implementada por la carpeta.
  

