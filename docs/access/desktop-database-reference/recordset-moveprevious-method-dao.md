---
title: Recordset.MovePrevious (método) (DAO)
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
ms.openlocfilehash: 2ee7bff8a5b7d17b714c4a52eff2eca5906c7135
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919874"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="c6ef3-102">Recordset.MovePrevious (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6ef3-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="c6ef3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6ef3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6ef3-104">Se desplaza al registro anterior de un objeto **Recordset** especificado y convierte ese registro en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ef3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6ef3-105">Syntax</span></span>

<span data-ttu-id="c6ef3-106">*expresión* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="c6ef3-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="c6ef3-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c6ef3-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ef3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6ef3-108">Remarks</span></span>

<span data-ttu-id="c6ef3-109">Utilice los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="c6ef3-p101">Si edita el registro activo, asegúrese de que utiliza el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-p101">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record. If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="c6ef3-p102">Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-p102">When you open a **Recordset**, the first record is current and the **BOF** property is **False**. If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="c6ef3-p103">Si utiliza **MovePrevious** cuando el primer registro está activo, la propiedad **BOF** es **True** y no hay registro activo. Si utiliza **MovePrevious** de nuevo, se produce un error y **BOF** sigue siendo **True**.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-p103">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record. If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="c6ef3-116">Si el objeto recordset hace referencia a un **objeto Recordset** de tipo tabla (sólo áreas de trabajo de Microsoft Access), el desplazamiento sigue el índice actual.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="c6ef3-117">Puede definir el índice actual mediante la propiedad **Index**.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="c6ef3-118">Si no define el índice actual, el orden de los registros devueltos queda sin definir.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="c6ef3-119">No puede usar los métodos **MoveFirst**, **MoveLast**ni **MovePrevious** en un objeto **Recordset** de tipo forward – only.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="c6ef3-120">Para mover hacia delante o hacia atrás la posición del registro actual en un objeto **Recordset** un número determinado de registros, use el método **Move**.</span><span class="sxs-lookup"><span data-stu-id="c6ef3-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

