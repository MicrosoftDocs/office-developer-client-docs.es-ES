---
title: Desconexión y reconexión del conjunto de registros
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c028a7d867a105f35b4848ecbe95339f5fcd4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293864"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d3b2e-102">Desconexión y reconexión del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d3b2e-102">Disconnecting and reconnecting the Recordset</span></span>


<span data-ttu-id="d3b2e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3b2e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d3b2e-104">Desconectar y volver a conectar el objeto Recordset</span><span class="sxs-lookup"><span data-stu-id="d3b2e-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="d3b2e-p101">Una de las características más eficaces de ADO es la posibilidad de abrir un **conjunto de registros** de cliente desde un origen de datos y, a continuación, *desconectar* el **conjunto de registros** del origen de datos. Una vez desconectado el **conjunto de registros**, se puede cerrar la conexión con el origen de datos para liberar así los recursos del servidor que se utilizan para mantenerla. Puede continuar viendo y modificando los datos del **conjunto de registros** mientras está desconectado y, más tarde, volver a conectarse al origen de datos para enviar sus actualizaciones en modo de proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="d3b2e-p101">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source. Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it. You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="d3b2e-p102">Para desconectar un **conjunto de registros**, ábralo con una ubicación de cursor de **adUseClient** y, a continuación, establezca la propiedad **ActiveConnection** en *Nothing* (los usuarios de C++ deben establecer **ActiveConnection** en NULL para desconectar).</span><span class="sxs-lookup"><span data-stu-id="d3b2e-p102">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*. (C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="d3b2e-110">Más adelante en este capítulo, se utilizará un **conjunto de registros** desconectado cuando se hable de la persistencia de **conjuntos de registros** para afrontar un escenario en el que se necesita tener los datos de un **conjunto de registros** disponibles para una aplicación mientras el equipo cliente no está conectado a una red.</span><span class="sxs-lookup"><span data-stu-id="d3b2e-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

