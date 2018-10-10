---
title: CancelarCambioDeRegistro (acción de macro)
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fe474f9ba7250e3225bc73460c6d192800c861b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484857"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="de680-102">CancelarCambioDeRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="de680-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="de680-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de680-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de680-104">Puede utilizar la acción **CancelarCambioDeRegistro** para cancelar los cambios aplicados a un registro en un bloque de datos **[CrearRegistro](createrecord-data-block.md)** o **[EditarRegistro](editrecord-data-block.md)** antes de que se confirmen los cambios.</span><span class="sxs-lookup"><span data-stu-id="de680-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <P><span data-ttu-id="de680-105">[!NOTA] La acción <STRONG>CancelarCambioDeRegistro</STRONG> solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="de680-105">The <STRONG>CancelRecordChange</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="de680-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de680-106">Remarks</span></span>

<span data-ttu-id="de680-107">Cuando se llama a la acción **CancelarCambioDeRegistro**, se sale inmediatamente del bloque de datos **CrearRegistro** o **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="de680-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

