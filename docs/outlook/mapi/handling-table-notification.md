---
title: Administrar las notificaciones de la tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299492"
---
# <a name="handling-table-notification"></a>Administrar las notificaciones de la tabla

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como alternativa a registrarse directamente con un objeto de origen Advise, como una carpeta o un usuario de mensajería, un cliente puede registrarse para recibir notificaciones en una tabla de contenido o de jerarquía. El seguimiento de los cambios en las entradas, carpetas y mensajes de la libreta de direcciones a través de una tabla de contenido o jerarquía puede ser más sencillo y sencillo que a través de objetos individuales. 

Por ejemplo, puede llamar a [IMAPITable:: Advise](imapitable-advise.md) en la tabla de jerarquía de una carpeta para detectar cuándo se producen cambios en una de sus subcarpetas. Si admite la visualización de mensajes remotos, Regístrese en la tabla de estado para observar la actividad de los proveedores de transporte y la cola MAPI. 
  
Sin embargo, no siempre es preferible usar notificaciones de tabla en lugar de notificaciones de objeto. La supervisión de los cambios en el número de mensajes de una carpeta es un ejemplo de Cuándo es posible que el cliente deba registrarse para recibir notificaciones de objeto en una carpeta en lugar de en una tabla implementada por la carpeta.
  

