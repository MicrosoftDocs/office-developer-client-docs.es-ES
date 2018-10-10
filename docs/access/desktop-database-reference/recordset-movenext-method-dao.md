---
title: Recordset.MoveNext Method (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7675da7016044836bd2c8bf723ab6e1bc9a65b1b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484356"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="a8a5e-102">Recordset.MoveNext Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a8a5e-102">Recordset.MoveNext Method (DAO)</span></span>


<span data-ttu-id="a8a5e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8a5e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8a5e-104">Se desplaza al siguiente registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8a5e-105">Syntax</span></span>

<span data-ttu-id="a8a5e-106">*expresión* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="a8a5e-106">*expression* .MoveNext</span></span>

<span data-ttu-id="a8a5e-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a8a5e-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8a5e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8a5e-108">Remarks</span></span>

<span data-ttu-id="a8a5e-109">Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="a8a5e-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="a8a5e-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="a8a5e-p103">Si utiliza **MoveNext** cuando el último registro está activo, la propiedad **EOF** es **True** y no hay registro activo. Si utiliza **MoveNext** de nuevo, se produce un error y **EOF** sigue siendo **True**.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="a8a5e-116">Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="a8a5e-117">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="a8a5e-118">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="a8a5e-119">No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="a8a5e-120">Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="a8a5e-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

