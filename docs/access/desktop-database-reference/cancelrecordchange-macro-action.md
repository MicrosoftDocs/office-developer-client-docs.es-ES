---
title: CancelarCambioDeRegistro (acción de macro)
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1e0cf06436293cbd0c0326a91bd38dcdce5f16a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869102"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="8da5d-102">CancelarCambioDeRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="8da5d-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="8da5d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8da5d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8da5d-104">Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)** antes de que se confirmen los cambios.</span><span class="sxs-lookup"><span data-stu-id="8da5d-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="8da5d-105">[!NOTA] La acción **CancelarCambioDeRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="8da5d-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="8da5d-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8da5d-106">Remarks</span></span>

<span data-ttu-id="8da5d-107">Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="8da5d-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

