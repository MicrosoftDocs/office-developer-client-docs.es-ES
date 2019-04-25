---
title: Método Recordset.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300241"
---
# <a name="recordsetmovefirst-method-dao"></a><span data-ttu-id="bb469-102">Método Recordset.MoveFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb469-102">Recordset.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="bb469-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb469-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb469-104">Se desplaza al primer registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="bb469-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb469-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb469-105">Syntax</span></span>

<span data-ttu-id="bb469-106">*expression* .MoveFirst</span><span class="sxs-lookup"><span data-stu-id="bb469-106">expression  . MoveFirst</span></span>

<span data-ttu-id="bb469-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="bb469-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb469-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb469-108">Remarks</span></span>

<span data-ttu-id="bb469-109">Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="bb469-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="bb469-p101">Si edita el registro activo, asegúrese de que usa el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="bb469-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="bb469-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="bb469-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="bb469-114">Si el primer o el último registro ya está activo cuando usa **MoveFirst** o **MoveLast**, el registro actual no cambia.</span><span class="sxs-lookup"><span data-stu-id="bb469-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="bb469-115">Si recordset hace referencia a un objeto **Recordset** de tipo de tabla (solo en áreas de trabajo de Microsoft Access), el movimiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="bb469-115">If  recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="bb469-116">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="bb469-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="bb469-117">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="bb469-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="bb469-118">No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.</span><span class="sxs-lookup"><span data-stu-id="bb469-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="bb469-119">Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="bb469-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

