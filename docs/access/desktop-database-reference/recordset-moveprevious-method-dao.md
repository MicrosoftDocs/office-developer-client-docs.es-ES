---
title: Método Recordset.MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 95cf5daa9eac6644b17f47b09ebc749bd9ed928e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284514"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="86e28-102">Método Recordset.MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="86e28-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="86e28-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86e28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86e28-104">Se desplaza al registro anterior de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="86e28-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86e28-105">Syntax</span></span>

<span data-ttu-id="86e28-106">*expresión* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="86e28-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="86e28-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="86e28-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e28-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86e28-108">Remarks</span></span>

<span data-ttu-id="86e28-109">Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="86e28-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="86e28-p101">Si edita el registro activo, asegúrese de que usa el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="86e28-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="86e28-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="86e28-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="86e28-p103">Si utiliza **MovePrevious** cuando el primer registro está activo, la propiedad **BOF** es **True** y no hay registro activo. Si utiliza **MovePrevious** de nuevo, se produce un error y **BOF** sigue siendo **True**.</span><span class="sxs-lookup"><span data-stu-id="86e28-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="86e28-116">Si recordset hace referencia a un objeto **Recordset** de tipo de tabla (solo en áreas de trabajo de Microsoft Access), el movimiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="86e28-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="86e28-117">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="86e28-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="86e28-118">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="86e28-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="86e28-119">No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.</span><span class="sxs-lookup"><span data-stu-id="86e28-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="86e28-120">Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="86e28-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

