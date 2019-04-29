---
title: Implementar un objeto receptor de notificaciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412110"
---
# <a name="implementing-an-advise-sink-object"></a>Implementar un objeto receptor de notificaciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede implementar sus propios objetos del receptor de notificaciones o usar una función de utilidad, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crea un objeto de notificación de notificaciones con una implementación de **Notify** que invoca una función de devolución de llamada. 
  
El uso de **HrAllocAdviseSink**tiene ventajas y desventajas. Puede guardar el trabajo, pero no proporciona ningún control sobre el recuento de referencias del objeto de notificación de aviso que crea. Por lo tanto, los clientes que necesiten controlar minuciosamente la versión del receptor de notificaciones o que tienen interdependencias entre su receptor de notificaciones y otro objeto de cliente deben crear su propia implementación de **IMAPIAdviseSink** y evitar el uso **de HrAllocAdviseSink** por completo. 
  
Un cliente que implemente su propio receptor de notificaciones debe convertirlo en un objeto independiente que no esté relacionado o en función de los demás objetos, a fin de eliminar posibles complicaciones en el recuento de referencias y la liberación de objetos. Sin embargo, si debe implementar su receptor de notificaciones como parte de otro objeto o incluir un puntero de reverso a otro objeto como miembro de datos, se recomienda mantener dos recuentos de referencias independientes: uno para el objeto al que hace referencia el receptor de notificaciones y otro para el notificar al receptor. 
  
Cuando el recuento de referencia del objeto al que se hace referencia cae en cero, se puede producir un error en todos sus métodos y se puede destruir su vtable, pero la memoria para el receptor de notificaciones debe permanecer intacta hasta que su recuento de referencia también caiga en cero. Esto significa que el método de **liberación** del receptor de notificaciones debe disminuir su recuento de referencia y finalizar la destrucción del objeto cuando ese contador llegue a cero. Si no se mantienen dos recuentos de referencia independientes, sería fácil destruir accidentalmente el receptor de notificaciones como parte del proceso de **liberación** del objeto que abarca. 
  
Los clientes que usan **HrAllocAdviseSink** para implementar un receptor de notificaciones deben tener la misma cuidado de no incluir su función de devolución de llamada como un método en otro objeto receptor de notificaciones. Para los clientes de C++, es tentador hacerlo y pasar el puntero _this_ como un parámetro. Se trata de una estrategia peligrosa porque los clientes suelen liberar un objeto cuando su recuento de referencia llega a cero. Si se libera la memoria para el objeto del receptor de notificaciones, el puntero _this_ no será válido. 
  
Según el tipo de evento y el origen de Advise, el método **BENOTIFY** puede controlar eventos de varias formas. En la tabla siguiente se ofrecen sugerencias sobre cómo controlar algunos de los eventos estándar. 
  
|**Tipo de evento**|**Controlar en Notify**|
|:-----|:-----|
|Objeto movido  <br/> |Si el primario original del objeto trasladado está relacionado con el nuevo elemento primario, actualice la vista comenzando con el contenedor de la carpeta o la libreta de direcciones que tenga el mayor nivel en la jerarquía. Si los dos contenedores primarios no están relacionados, actualice ambas vistas.  <br/> |
|Nuevo mensaje  <br/> |Cambiar la interfaz de usuario para informar al usuario de la llegada de uno o más mensajes nuevos. Situar la carpeta de recepción en la vista actual.  <br/> |
|Error  <br/> |Para todos los objetos, a excepción de la sesión, registre el error si es necesario y vuelva. Para el objeto Session, cierre la sesión si es posible.  <br/> |
|Búsqueda completada  <br/> |No es necesario realizar ningún procesamiento.  <br/> |
   
> [!NOTE]
> Los controladores de notificación deben ser reentrantes. 
  

