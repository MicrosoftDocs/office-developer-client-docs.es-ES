---
title: Procesamiento diferido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816635"
---
# <a name="deferring-processing"></a>Procesamiento diferido

  
  
**Hace referencia a**: Outlook 
  
Pase el indicador MAPI_DEFERRED_ERRORS a las llamadas de método medida de lo posible. Muchas de las llamadas al método MAPI se han optimizado para que acepte esta marca, lo que provoca que el proveedor ya sea posponer la tarea solicitada hasta que se pueden realizar varias tareas a la vez o puede esperar a que los resultados ya no.
  
Por ejemplo, si se pasa MAPI_DEFERRED_ERRORS a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir una carpeta, la apertura de la carpeta y un posible remoto de llamadas se puede posponer hasta que se realiza otra llamada, como una llamada a la carpeta **GetHierarchyTable** o ** GetProps** métodos. **GetHierarchyTable** y **GetProps** requieren la devolución de datos del proveedor de servicios, una tarea que se debe realizar inmediatamente. 
  
Otra forma de procesarla es simplemente no realizar una llamada. Al que se va a tener en cuenta del usuario y cuando el usuario puede perciben un consumo de recursos o el tiempo de procesamiento, puede determinar cuando tenga sentido para realizar llamadas. No hay una oportunidad para mejorar el rendimiento mediante la realización de llamadas, ya sea a la vez cuando el usuario no observará o por no realizarlos.
  
Por ejemplo, considere la situación cuando recibe más de una notificación por segundo desde un almacén de mensajes que está moviendo un gran número de mensajes. Se muestra un indicador de progreso para indicar el porcentaje de finalización de la operación. Normalmente, los usuarios no notarán esta operación para ser lenta, hasta que se han pasado unos segundos. Por lo tanto, si va a actualizar el indicador de progreso, no realice ningún cambio hasta que al menos cuatro segundos después de la iniciación de la operación de movimiento. Esto va a ahorrar tiempo en los casos comunes cuando la operación es rápida e informar a los usuarios de manera oportuna cuando la operación es lenta.
  

