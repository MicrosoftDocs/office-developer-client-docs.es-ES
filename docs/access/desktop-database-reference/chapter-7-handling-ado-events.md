---
title: 'Capítulo 7: Control de eventos de ADO'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296405"
---
# <a name="chapter-7-handling-ado-events"></a>Capítulo 7: Control de eventos de ADO

**Se aplica a:** Access 2013, Office 2013

El modelo de eventos de ADO admite ciertas operaciones sincrónicas y asincrónicas de ADO que generan *eventos*, o notificaciones, antes de iniciar la operación o después de completarla. Un evento es realmente una llamada a una rutina de controlador de eventos que se define en una aplicación.

Si proporciona procedimientos o funciones de controlador para el grupo de eventos que ocurren antes de iniciarse una operación, podrá examinar o modificar los parámetros que se pasaron a la operación. Puesto que aún no se ha ejecutado, puede cancelar la operación o bien permitir que se ejecute.

El grupo de eventos que ocurren tras completar una operación es especialmente importante si utiliza ADO asincrónicamente. Por ejemplo, para una aplicación que inicia una operación asincrónica [Recordset.Open](open-method-ado-recordset.md) la notificación de que la operación concluyó se realiza mediante un evento de finalización de ejecución.

El uso del modelo de eventos de ADO agrega alguna sobrecarga a la aplicación, pero proporciona mucha más flexibilidad que otros métodos de trabajar con operaciones asincrónicas, tales como el de vigilar la propiedad [State](state-property-ado.md) de un objeto con un bucle.

En este capítulo, se tratan los temas siguientes:

- [Resumen del controlador de eventos de ADO](ado-event-handler-summary.md)
- [Tipos de eventos](types-of-events.md)
- [Parámetros de evento](event-parameters.md)
- [Cómo funcionan los controladores de eventos combinados](how-event-handlers-work-together.md)
- [Creación de instancias de eventos de ADO por idioma (ADO)](ado-event-instantiation-by-language-ado.md)
