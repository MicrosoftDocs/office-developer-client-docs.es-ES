---
title: CancelarCambioDeRegistro (acción de macro)
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296657"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="e2647-102">CancelarCambioDeRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e2647-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="e2647-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2647-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2647-104">Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)** antes de que se confirmen los cambios.</span><span class="sxs-lookup"><span data-stu-id="e2647-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="e2647-105">[!NOTA] La acción **CancelarCambioDeRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="e2647-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="e2647-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2647-106">Remarks</span></span>

<span data-ttu-id="e2647-107">Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="e2647-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

