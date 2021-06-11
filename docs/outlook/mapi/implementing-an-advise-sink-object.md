---
title: Implementación de un objeto Advise Sink
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
# <a name="implementing-an-advise-sink-object"></a>Implementación de un objeto Advise Sink

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede implementar sus propios objetos de receptor advise o usar una función de utilidad, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crea un objeto de receptor de aviso con una implementación de **OnNotify** que invoca una función de devolución de llamada. 
  
El uso de **HrAllocAdviseSink** tiene ventajas y desventajas. Puede guardar el trabajo, pero no proporciona control sobre el recuento de referencias del objeto receptor de aviso que crea. Por lo tanto, los clientes que necesitan controlar cuidadosamente la versión del receptor de avisos o que tienen interdependencias entre su receptor de asesoramiento y otro objeto de cliente deben construir su propia implementación **IMAPIAdviseSink** y evitar el uso total de **HrAllocAdviseSink.** 
  
Un cliente que implemente su propio receptor de avisos debe convertirlo en un objeto independiente que no está relacionado o depende de otros objetos para eliminar posibles complicaciones en el recuento de referencias y la liberación de objetos. Sin embargo, si debe implementar el receptor de avisos como parte de otro objeto o incluir un puntero hacia atrás a otro objeto como miembro de datos, se recomienda mantener dos recuentos de referencias independientes: uno para el objeto al que hace referencia el receptor de avisos y otro para el receptor de avisos. 
  
Cuando el recuento de referencias del objeto al que se hace referencia cae a cero, todos sus métodos pueden producir errores y su tabla virtual puede destruirse, pero la memoria del receptor de aviso debe permanecer intacta hasta que el recuento de referencias también caiga a cero. Esto significa que el método **Release** del receptor de aviso debe disminuir su recuento de referencias y terminar de destruir el objeto cuando ese recuento alcanza cero. Si no se mantienen dos recuentos de referencias independientes, sería fácil destruir inadvertidamente el receptor de avisos como parte del proceso release del **objeto** que abarca. 
  
Los clientes **que usan HrAllocAdviseSink** para implementar un receptor de aviso deben tener el mismo cuidado de no incluir su función de devolución de llamada como método en otro objeto receptor de aviso. Para los clientes de C++, es tentador hacerlo y pasar el  _puntero_ como parámetro. Se trata de una estrategia peligrosa porque los clientes normalmente liberan un objeto cuando su recuento de referencias alcanza cero. Liberar la memoria del objeto receptor advise haría que este puntero  _no_ sea válido. 
  
Según el tipo de evento y el origen del aviso, el **método OnNotify** puede controlar los eventos de varias maneras. En la siguiente tabla se ofrecen sugerencias sobre cómo controlar algunos de los eventos estándar. 
  
|**Tipo de evento**|**Control en OnNotify**|
|:-----|:-----|
|Objeto movido  <br/> |Si el elemento primario original del objeto movido está relacionado con el nuevo elemento primario, actualice la vista a partir de la carpeta o contenedor de libreta de direcciones más alto de la jerarquía. Si los dos contenedores primarios no están relacionados, actualice ambas vistas.  <br/> |
|Nuevo mensaje  <br/> |Cambie la interfaz de usuario para informar al usuario de la llegada de uno o más mensajes nuevos. Coloque la carpeta de recepción en la vista actual.  <br/> |
|Error  <br/> |Para todos los objetos excepto la sesión, registre el error si es necesario y vuelva. Para el objeto de sesión, cierre la sesión si es posible.  <br/> |
|Búsqueda completada  <br/> |No es necesario procesar.  <br/> |
   
> [!NOTE]
> Los controladores de notificaciones deben ser reenentrantes. 
  

