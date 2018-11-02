---
title: Recordset2.MoveFirst (método) (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 74b186d0-8f6a-d136-a563-04f58d67b122
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195879(v=office.15)
ms:contentKeyID: 48545667
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd5225e2fdbf662180b3cb11f48c8e7ba65b706a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921372"
---
# <a name="recordset2movefirst-method-dao"></a><span data-ttu-id="b3573-102">Recordset2.MoveFirst (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3573-102">Recordset2.MoveFirst method (DAO)</span></span>


<span data-ttu-id="b3573-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3573-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3573-104">Se desplaza al primer registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="b3573-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3573-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3573-105">Syntax</span></span>

<span data-ttu-id="b3573-106">*expresión* . Métodos MoveFirst</span><span class="sxs-lookup"><span data-stu-id="b3573-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="b3573-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b3573-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3573-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3573-108">Remarks</span></span>

<span data-ttu-id="b3573-109">Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="b3573-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="b3573-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="b3573-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="b3573-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="b3573-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="b3573-114">Si el primer o el último registro ya está activo cuando utiliza **MoveFirst** o **MoveLast**, el registro activo no cambia.</span><span class="sxs-lookup"><span data-stu-id="b3573-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="b3573-115">Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="b3573-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="b3573-116">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="b3573-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="b3573-117">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="b3573-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="b3573-118">No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="b3573-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="b3573-119">Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="b3573-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

