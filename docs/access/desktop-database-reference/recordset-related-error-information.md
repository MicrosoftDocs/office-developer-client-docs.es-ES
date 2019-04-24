---
title: Información de errores relacionados con conjuntos de registros
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307619"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="42f1c-102">Información de errores relacionados con conjuntos de registros</span><span class="sxs-lookup"><span data-stu-id="42f1c-102">Recordset-related error information</span></span>

<span data-ttu-id="42f1c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42f1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42f1c-104">Durante un proceso por lotes, la propiedad **Status** del objeto **Recordset** proporciona información sobre cada registro del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="42f1c-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="42f1c-105">Antes de que se realice una actualización por lotes, la propiedad **Status** del **conjunto de registros** refleja información sobre los registros que se van a agregar, cambiar y eliminar.</span><span class="sxs-lookup"><span data-stu-id="42f1c-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="42f1c-106">Después de haber llamado a **UpdateBatch**, la propiedad **Status** indica si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="42f1c-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="42f1c-107">A medida que se mueve por los registros del **conjunto de registros**, el valor de la propiedad **Status** cambia para describir el estado del registro activo.</span><span class="sxs-lookup"><span data-stu-id="42f1c-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

