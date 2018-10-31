---
title: Modo de proceso por lotes (referencia de escritorio de la base de datos de Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37f66f6ef6c4ed63b106584a6ac5118cddf20526
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861207"
---
# <a name="batch-mode"></a><span data-ttu-id="401d6-102">Modo por lotes</span><span class="sxs-lookup"><span data-stu-id="401d6-102">Batch Mode</span></span>


<span data-ttu-id="401d6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="401d6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="401d6-p101">El modo de proceso por lotes está activo cuando la propiedad **LockType** se ha establecido en **adLockBatchOptimistic** y el proveedor admite la actualización por lotes. Algunas opciones de configuración del tipo de bloqueo no están disponibles según cuál sea la ubicación del cursor. Por ejemplo, un tipo de bloqueo pesimista no está disponible cuando **CursorLocation** está establecido en **adUseClient**. A la inversa, es posible que un proveedor no admita un bloqueo optimista por lotes cuando la ubicación del cursor esté en el servidor. La actualización por lotes se debe utilizar únicamente con un conjunto de claves o con un cursor estático.</span><span class="sxs-lookup"><span data-stu-id="401d6-p101">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider. Certain lock type settings are not available depending on cursor location. For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**. Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server. You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="401d6-p102">El método **UpdateBatch** se utiliza para enviar cambios en un **conjunto de registros** guardados en el búfer de copia hasta el servidor, para actualizar el origen de datos. En la sección siguiente, abriremos un **conjunto de registros** en modo de proceso por lotes, realizaremos cambios en el búfer de copia y a continuación, enviaremos nuestros cambios al origen de datos mediante una llamada a **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="401d6-p102">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source. In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="401d6-111">Esta sección incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="401d6-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="401d6-112">Envío de actualizaciones: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="401d6-112">Sending the Updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)

- [<span data-ttu-id="401d6-113">Filtro de registros actualizados</span><span class="sxs-lookup"><span data-stu-id="401d6-113">Filtering for Updated Records</span></span>](filtering-for-updated-records.md)

- [<span data-ttu-id="401d6-114">Tratamiento de las actualizaciones con errores</span><span class="sxs-lookup"><span data-stu-id="401d6-114">Dealing with Failed Updates</span></span>](dealing-with-failed-updates.md)

- [<span data-ttu-id="401d6-115">Detección y resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="401d6-115">Detecting and Resolving Conflicts</span></span>](detecting-and-resolving-conflicts.md)

- [<span data-ttu-id="401d6-116">Desconexión y reconexión del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="401d6-116">Disconnecting and Reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)

- [<span data-ttu-id="401d6-117">Actualizar los resultados de una operación JOIN: Tabla única</span><span class="sxs-lookup"><span data-stu-id="401d6-117">Updating JOINed Results: Unique Table</span></span>](updating-joined-results-unique-table.md)

