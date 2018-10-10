---
title: 'Capítulo 7: Controlar eventos de ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485995"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="47411-102">Capítulo 7: Controlar eventos de ADO</span><span class="sxs-lookup"><span data-stu-id="47411-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="47411-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="47411-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="47411-p101">El modelo de eventos de ADO admite ciertas operaciones sincrónicas y asincrónicas de ADO que generan *eventos*, o notificaciones, antes de iniciar la operación o después de completarla. Un evento es realmente una llamada a una rutina de controlador de eventos que se define en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="47411-p101">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes. An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="47411-p102">Si proporciona procedimientos o funciones de controlador para el grupo de eventos que ocurren antes de iniciarse una operación, podrá examinar o modificar los parámetros que se pasaron a la operación. Puesto que aún no se ha ejecutado, puede cancelar la operación o bien permitir que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="47411-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="47411-p103">El grupo de eventos que ocurren tras completar una operación es especialmente importante si utiliza ADO asincrónicamente. Por ejemplo, para una aplicación que inicia una operación asincrónica [Recordset.Open](open-method-ado-recordset.md) la notificación de que la operación concluyó se realiza mediante un evento de finalización de ejecución.</span><span class="sxs-lookup"><span data-stu-id="47411-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="47411-110">El uso del modelo de eventos de ADO agrega alguna sobrecarga a la aplicación, pero proporciona mucha más flexibilidad que otros métodos de trabajar con operaciones asincrónicas, tales como el de vigilar la propiedad [State](state-property-ado.md) de un objeto con un bucle.</span><span class="sxs-lookup"><span data-stu-id="47411-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

