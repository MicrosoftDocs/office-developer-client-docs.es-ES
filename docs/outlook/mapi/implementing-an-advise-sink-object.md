---
title: Implementar un objeto receptor de sugerencias
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a95222f8ec75c519558636cf54111f28cbe14066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817682"
---
# <a name="implementing-an-advise-sink-object"></a>Implementar un objeto receptor de sugerencias

  
  
**Hace referencia a**: Outlook 
  
Un cliente puede implementar sus propios objetos de receptor advise o utilizar una función de utilidad, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** crea un objeto de receptor advise con una implementación de **OnNotify** que invoca una función de devolución de llamada. 
  
Existen ventajas y desventajas al uso de **HrAllocAdviseSink**. Puede guardar el trabajo, pero no proporciona ningún control sobre el objeto de receptor advise que crea de recuento de referencias. Por lo tanto, deben construir su propia implementación de **IMAPIAdviseSink** y evitar el uso de **los clientes que necesitan controlar cuidadosamente la versión del receptor de sus notificaciones o que tienen interdependencias entre su receptor de notificaciones y otro objeto de cliente HrAllocAdviseSink** por completo. 
  
Un cliente implementar su propio receptor de notificaciones hacen que un objeto independiente no relacionados a o dependen de otros objetos con el fin de eliminar posibles complicaciones en versión de objeto y el recuento de referencia. Sin embargo, si debe implementar su receptor de notificaciones como parte de otro objeto o incluir un puntero a otro objeto como un miembro de datos, se recomienda que se mantienen dos recuentos de referencia independientes: uno para el objeto al que hace referencia el receptor de notificaciones y otro para el receptor de aviso. 
  
Cuando el recuento de referencia del objeto que se hace referencia llega a cero, todos sus métodos pueden producirse un error y se puede destruir su tabla vtable, pero la memoria para el receptor de notificaciones debe permanecer intacta hasta después de que su recuento de referencia también entra en cero. Esto significa que debe reducir su recuento de referencia y de fin destruir el objeto cuando ese recuento llega a cero (método) **versión** del receptor de notificaciones. Si no se mantienen dos recuentos de referencia independiente, sería fácil de destruir accidentalmente el receptor de notificaciones como parte del proceso de **versión** del objeto que abarca. 
  
Uso de **HrAllocAdviseSink** para implementar un receptor de notificaciones de clientes deben ser igualmente cuidados de no incluir su función de devolución de llamada como un método en otro objeto de receptor advise. Para los clientes de C++, es tentador hacerlo y pasar el puntero _this_ como un parámetro. Ésta es una estrategia peligrosa debido a que los clientes normalmente liberan un objeto cuando su recuento de referencia llega a cero. Liberación de la memoria para el objeto de receptor advise haría que el puntero _this_ no válido. 
  
Según el tipo de evento y el origen de advise, su **OnNotify (** método) puede controlar los eventos de varias formas. En la siguiente tabla se ofrece sugerencias en el procedimiento para tratar algunos de los eventos estándares. 
  
|**Tipo de evento**|**Tratamiento de OnNotify**|
|:-----|:-----|
|Objeto movido  <br/> |Si primario original del objeto que se ha movido está relacionado con el nuevo elemento primario, actualice el principio de la vista con la carpeta o el contenedor de la libreta de direcciones más alto en la jerarquía. Si los contenedores dos principales no están relacionados, actualizar ambas de las vistas.  <br/> |
|Nuevo mensaje  <br/> |Cambiar la interfaz de usuario para informar al usuario de la llegada de uno o varios mensajes nuevos. Colocar la carpeta de recepción en la vista actual.  <br/> |
|Error  <br/> |Para todos los objetos excepto la sesión, inicie el error si es necesario y devolución. Para el objeto de sesión, cierre la sesión si es posible.  <br/> |
|Búsqueda completa  <br/> |No es necesario el procesamiento.  <br/> |
   
> [!NOTE]
> Controladores de notificación deben ser reentrantes. 
  

