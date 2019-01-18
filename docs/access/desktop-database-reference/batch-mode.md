---
title: Modo de proceso por lotes (referencia de escritorio de la base de datos de Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717814"
---
# <a name="batch-mode"></a><span data-ttu-id="393ca-102">Modo por lotes</span><span class="sxs-lookup"><span data-stu-id="393ca-102">Batch mode</span></span>

<span data-ttu-id="393ca-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="393ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="393ca-p101">El modo de proceso por lotes está activo cuando la propiedad **LockType** se ha establecido en **adLockBatchOptimistic** y el proveedor admite la actualización por lotes. Algunas opciones de configuración del tipo de bloqueo no están disponibles según cuál sea la ubicación del cursor. Por ejemplo, un tipo de bloqueo pesimista no está disponible cuando **CursorLocation** está establecido en **adUseClient**. A la inversa, es posible que un proveedor no admita un bloqueo optimista por lotes cuando la ubicación del cursor esté en el servidor. La actualización por lotes se debe utilizar únicamente con un conjunto de claves o con un cursor estático.</span><span class="sxs-lookup"><span data-stu-id="393ca-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="393ca-p102">El método **UpdateBatch** se utiliza para enviar cambios en un **conjunto de registros** guardados en el búfer de copia hasta el servidor, para actualizar el origen de datos. En la sección siguiente, abriremos un **conjunto de registros** en modo de proceso por lotes, realizaremos cambios en el búfer de copia y a continuación, enviaremos nuestros cambios al origen de datos mediante una llamada a **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="393ca-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="393ca-111">Esta sección incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="393ca-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="393ca-112">Envío de actualizaciones: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="393ca-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="393ca-113">Filtro de registros actualizados</span><span class="sxs-lookup"><span data-stu-id="393ca-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="393ca-114">Tratamiento de las actualizaciones con errores</span><span class="sxs-lookup"><span data-stu-id="393ca-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="393ca-115">Detección y resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="393ca-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="393ca-116">Desconexión y reconexión del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="393ca-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="393ca-117">Actualizar los resultados de JOIN: tabla única</span><span class="sxs-lookup"><span data-stu-id="393ca-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

