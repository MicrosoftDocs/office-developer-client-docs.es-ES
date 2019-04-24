---
title: Desferir el procesamiento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336935"
---
# <a name="deferring-processing"></a>Desferir el procesamiento

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Pase la marca MAPI_DEFERRED_ERRORS a las llamadas de método tanto como sea posible. Muchas de las llamadas del método MAPI se han optimizado para aceptar esta marca, lo que hace que el proveedor posponga la tarea solicitada hasta que se puedan realizar varias tareas a la vez o cuando puede esperar que ya no se produzcan los resultados.
  
Por ejemplo, si pasa MAPI_DEFERRED_ERRORS a [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir una carpeta, se puede posponer la apertura de la carpeta y una posible llamada remota hasta que realice otra llamada, como una llamada al **GetHierarchyTable** de la carpeta o ** Métodos GetProps** . Tanto **GetHierarchyTable** como **GetProps** requieren la devolución de datos del proveedor de servicios, una tarea que debe realizarse inmediatamente. 
  
Otra forma de aplazar el procesamiento es sencillamente no realizar una llamada. Al conocer al usuario y cuando el usuario puede percibir un agotamiento de los recursos o el tiempo de procesamiento, puede determinar si tiene sentido realizar llamadas. Hay una oportunidad de mejorar el rendimiento al realizar llamadas al mismo tiempo que el usuario no las apreciará o no las hará.
  
Por ejemplo, considere la situación en la que recibe más de una notificación por segundo de un almacén de mensajes que está moviendo un gran número de mensajes. Se muestra un indicador de progreso para indicar el porcentaje de finalización de la operación. Por lo general, los usuarios no percibirán que esta operación sea lenta hasta que pasen unos segundos. Por lo tanto, si actualiza el indicador de progreso, no realice ningún cambio hasta al menos cuatro segundos después del inicio de la operación de movimiento. Esto ahorrará tiempo en los casos comunes en los que la operación es rápida e informa a los usuarios de manera oportuna cuando la operación es lenta.
  

