---
title: 'Capítulo 6: Tratamiento de errores'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e00f762ac76023f3f720d8e7341c517b932e3f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483684"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="40cb6-102">Capítulo 6: Tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="40cb6-102">Chapter 6: Error Handling</span></span>


<span data-ttu-id="40cb6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40cb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40cb6-p101">ADO utiliza varios métodos diferentes para notificar a una aplicación los errores que se producen. En este capítulo, se explican los tipos de errores que se pueden producir cuando se trabaja con ADO y cómo se notifican a la aplicación. Se termina con unas sugerencias acerca de cómo tratar estos errores.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p101">ADO uses several different methods to notify an application of errors that occur. This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified. It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="40cb6-107">¿Cómo informa ADO de los errores?</span><span class="sxs-lookup"><span data-stu-id="40cb6-107">How Does ADO Report Errors?</span></span>

<span data-ttu-id="40cb6-108">ADO notifica los errores de varias formas:</span><span class="sxs-lookup"><span data-stu-id="40cb6-108">ADO notifies you about errors in several ways:</span></span>

  - <span data-ttu-id="40cb6-p102">Los errores de ADO generan un error en tiempo de ejecución. Trate un error de ADO de la misma manera que lo haría con cualquier otro error en tiempo de ejecución, por ejemplo, utilizando una instrucción **On Error** en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p102">ADO errors generate a run-time error. Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

  - <span data-ttu-id="40cb6-p103">Su programa puede recibir errores de OLE DB. Un error de OLE DB también genera un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p103">Your program can receive errors from OLE DB. An OLE DB error generates a run-time error as well.</span></span>

  - <span data-ttu-id="40cb6-113">Si el error es específico de su proveedor de datos, aparecen objetos **Error** en la colección **Errors** del objeto **Connection** que se utilizó para obtener acceso al almacén de datos cuando se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="40cb6-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

  - <span data-ttu-id="40cb6-p104">Si el proceso que desencadenó un evento también generó un error, la información de error se incluye en un objeto **Error** y se pasa como parámetro al evento. Vea el [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md)para obtener más información acerca de eventos.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p104">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event. See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

  - <span data-ttu-id="40cb6-p105">Los problemas que se producen al procesar actualizaciones por lotes o al ejecutar otras operaciones masivas que implican a un **conjunto de registros** pueden indicarse mediante la propiedad **Status** del **conjunto de registros**. Por ejemplo, infracciones de restricción de esquema o permisos no suficientes se pueden especificar mediante valores de **RecordStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p105">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**. For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

  - <span data-ttu-id="40cb6-p106">Los problemas que se producen implicando a un **campo** determinado del registro activo también se indican mediante la propiedad **Status** de cada **campo** de la colección **Fields** del **registro** o del **conjunto de registros**. Por ejemplo, actualizaciones que no se han podido completar o tipos de datos incompatibles se pueden especificar mediante valores de **FieldStatusEnum**.</span><span class="sxs-lookup"><span data-stu-id="40cb6-p106">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**. For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="40cb6-120">En las secciones siguientes, se describe cada uno de estos métodos de notificación con más detalle.</span><span class="sxs-lookup"><span data-stu-id="40cb6-120">The following sections describe each of these notification methods in more detail.</span></span>

