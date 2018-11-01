---
title: Recordset2.MovePrevious Method (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cdc6173a419881b64b89b8fd898f1c11a4b2f64b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875661"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="de2c6-102">Recordset2.MovePrevious Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="de2c6-102">Recordset2.MovePrevious Method (DAO)</span></span>


<span data-ttu-id="de2c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de2c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de2c6-104">Se desplaza al registro anterior de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="de2c6-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de2c6-105">Syntax</span></span>

<span data-ttu-id="de2c6-106">*expresión* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="de2c6-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="de2c6-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="de2c6-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de2c6-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de2c6-108">Remarks</span></span>

<span data-ttu-id="de2c6-109">Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="de2c6-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="de2c6-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="de2c6-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="de2c6-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="de2c6-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="de2c6-p103">Si utiliza **MovePrevious** cuando el primer registro está activo, la propiedad **BOF** es **True** y no hay registro activo. Si utiliza **MovePrevious** de nuevo, se produce un error y **BOF** sigue siendo **True**.</span><span class="sxs-lookup"><span data-stu-id="de2c6-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="de2c6-116">Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="de2c6-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="de2c6-117">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="de2c6-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="de2c6-118">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="de2c6-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="de2c6-119">No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="de2c6-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="de2c6-120">Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="de2c6-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

