---
title: 'Capítulo 7: Controlar eventos de ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 816dd98e5e4c21f3159edf18b5687b2b0578e399
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860843"
---
# <a name="chapter-7-handling-ado-events"></a>Capítulo 7: Controlar eventos de ADO


**Se aplica a**: Access 2013 | Office 2013

El modelo de eventos de ADO admite ciertas operaciones sincrónicas y asincrónicas de ADO que generan *eventos*, o notificaciones, antes de iniciar la operación o después de completarla. Un evento es realmente una llamada a una rutina de controlador de eventos que se define en una aplicación.

Si proporciona procedimientos o funciones de controlador para el grupo de eventos que ocurren antes de iniciarse una operación, podrá examinar o modificar los parámetros que se pasaron a la operación. Puesto que aún no se ha ejecutado, puede cancelar la operación o bien permitir que se ejecute.

El grupo de eventos que ocurren tras completar una operación es especialmente importante si utiliza ADO asincrónicamente. Por ejemplo, para una aplicación que inicia una operación asincrónica [Recordset.Open](open-method-ado-recordset.md) la notificación de que la operación concluyó se realiza mediante un evento de finalización de ejecución.

El uso del modelo de eventos de ADO agrega alguna sobrecarga a la aplicación, pero proporciona mucha más flexibilidad que otros métodos de trabajar con operaciones asincrónicas, tales como el de vigilar la propiedad [State](state-property-ado.md) de un objeto con un bucle.

En este capítulo, se tratan los temas siguientes:

- [Resumen de controladores de eventos de ADO](ado-event-handler-summary.md)

- [Tipos de eventos](types-of-events.md)

- [Parámetros de evento](event-parameters.md)

- [Cómo funcionan los controladores de eventos combinados](how-event-handlers-work-together.md)

- [ADO Event Instantiation by Language (ADO)](ado-event-instantiation-by-language-ado.md)