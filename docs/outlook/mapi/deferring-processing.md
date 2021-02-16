---
title: Aplazar el procesamiento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430934"
---
# <a name="deferring-processing"></a>Aplazar el procesamiento

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Pase la marca MAPI_DEFERRED_ERRORS a las llamadas de método tanto como sea posible. Muchas de las llamadas al método MAPI se han optimizado para aceptar esta marca, lo que hace que el proveedor posponga la tarea solicitada hasta que se puedan realizar varias tareas a la vez o no puede esperar más a los resultados.
  
Por ejemplo, si pasas MAPI_DEFERRED_ERRORS a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir una carpeta, la apertura de la carpeta y una posible llamada remota se pueden posponer hasta que realices otra llamada, como una llamada a los métodos **GetHierarchyTable** o **GetProps** de la carpeta. Tanto **GetHierarchyTable** como **GetProps** requieren la devolución de datos del proveedor de servicios, una tarea que debe realizarse inmediatamente. 
  
Otra forma de aplazar el procesamiento es simplemente no realizar una llamada. Al tener en cuenta al usuario y cuando el usuario puede percibir una purga en los recursos o el tiempo de procesamiento, puede determinar cuándo tiene sentido realizar llamadas. Existe la oportunidad de mejorar el rendimiento realizando llamadas en un momento en que el usuario no se da cuenta o no las realiza en absoluto.
  
Por ejemplo, tenga en cuenta la situación en la que recibe más de una notificación por segundo desde un almacén de mensajes que mueve un gran número de mensajes. Se muestra un indicador de progreso para indicar el porcentaje de finalización de la operación. Normalmente, los usuarios no perciben que esta operación es lenta hasta que transcurran unos segundos. Por lo tanto, si va a actualizar el indicador de progreso, no realice ningún cambio hasta al menos cuatro segundos después del inicio de la operación de movimiento. Esto ahorrará tiempo en los casos comunes cuando la operación es rápida e informará a los usuarios de forma oportuna cuando la operación es lenta.
  

