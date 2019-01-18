---
title: Actualización de datos (referencia de escritorio de la base de datos de Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726340"
---
# <a name="updating-data"></a><span data-ttu-id="a8591-102">Actualización de datos</span><span class="sxs-lookup"><span data-stu-id="a8591-102">Updating data</span></span>


<span data-ttu-id="a8591-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8591-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8591-104">El comportamiento y la funcionalidad de las operaciones de actualización dependen en gran medida del modo de actualización (tipo de bloqueo), del tipo de cursor y de su ubicación.</span><span class="sxs-lookup"><span data-stu-id="a8591-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="a8591-p101">Use el método **Update** para guardar los cambios efectuados en el registro actual de un objeto **Recordset** desde la llamada al método **AddNew** o desde el cambio de alguno de los valores de campo de un registro existente. El objeto **Recordset** debe ser compatible con actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="a8591-p101">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="a8591-p102">Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llame al método **UpdateBatch**. Si modifica el registro actual o agrega un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir los cambios por lotes al proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8591-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="a8591-109">El registro actual sigue siendo el actual después de la llamada a los métodos **Update** o **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="a8591-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="a8591-110">Esta sección incluye los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a8591-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="a8591-111">Modo Inmediato</span><span class="sxs-lookup"><span data-stu-id="a8591-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="a8591-112">Procesamiento de transacciones</span><span class="sxs-lookup"><span data-stu-id="a8591-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="a8591-113">Modo de proceso por lotes (ADO)</span><span class="sxs-lookup"><span data-stu-id="a8591-113">Batch mode (ADO)</span></span>](batch-mode.md)

