---
title: Método Recordset.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 1b0ebe0edcfcbfac5942fc83a3ff1f99eddfea7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300346"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="4e685-102">Método Recordset.MoveNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e685-102">Recordset.MoveNext method (DAO)</span></span>


<span data-ttu-id="4e685-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e685-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e685-104">Se desplaza al siguiente registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="4e685-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e685-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e685-105">Syntax</span></span>

<span data-ttu-id="4e685-106">*expression* .MoveNext</span><span class="sxs-lookup"><span data-stu-id="4e685-106">expression  . MoveNext</span></span>

<span data-ttu-id="4e685-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="4e685-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e685-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e685-108">Remarks</span></span>

<span data-ttu-id="4e685-109">Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="4e685-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="4e685-p101">Si edita el registro activo, asegúrese de que usa el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="4e685-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="4e685-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="4e685-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="4e685-p103">Si utiliza **MoveNext** cuando el último registro está activo, la propiedad **EOF** es **True** y no hay registro activo. Si utiliza **MoveNext** de nuevo, se produce un error y **EOF** sigue siendo **True**.</span><span class="sxs-lookup"><span data-stu-id="4e685-p103">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record. If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="4e685-116">Si recordset hace referencia a un objeto **Recordset** de tipo de tabla (solo en áreas de trabajo de Microsoft Access), el movimiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="4e685-116">If  recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="4e685-117">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="4e685-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="4e685-118">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="4e685-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="4e685-119">No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.</span><span class="sxs-lookup"><span data-stu-id="4e685-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="4e685-120">Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="4e685-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

