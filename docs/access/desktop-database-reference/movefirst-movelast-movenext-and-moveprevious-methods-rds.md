---
title: MoveFirst, MoveLast, MoveNext y MovePrevious (métodos, RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c78e6aaca31201e076dffb55b19be638a337dd19
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944931"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="82211-102">MoveFirst, MoveLast, MoveNext y MovePrevious (métodos, RDS)</span><span class="sxs-lookup"><span data-stu-id="82211-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>


<span data-ttu-id="82211-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82211-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82211-104">Se desplaza al primer, último, siguiente o anterior registro de un objeto [Recordset](recordset-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="82211-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="82211-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82211-105">Syntax</span></span>

<span data-ttu-id="82211-106">*DataControl*. Conjunto de registros. {</span><span class="sxs-lookup"><span data-stu-id="82211-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="82211-107">Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="82211-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="82211-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82211-108">Parameters</span></span>

  - <span data-ttu-id="82211-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="82211-109">*DataControl*</span></span>

  - <span data-ttu-id="82211-110">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="82211-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="82211-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82211-111">Remarks</span></span>

<span data-ttu-id="82211-112">Puede utilizar los métodos **Move** con el **RDS. DataControl** objeto para navegar por los registros de datos en los controles enlazados a datos en una página Web.</span><span class="sxs-lookup"><span data-stu-id="82211-112">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> <span data-ttu-id="82211-113">Por ejemplo, supongamos que muestra un objeto **Recordset** en una cuadrícula enlazando a un objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="82211-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="82211-114">A continuación, podrá incluir los botones Primero, Último, Siguiente y Anterior, en los que los usuarios pueden hacer clic para moverse hacia el registro primero, último, siguiente o anterior del objeto **Recordset** mostrado.</span><span class="sxs-lookup"><span data-stu-id="82211-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="82211-115">Para ello, debe llamar a los métodos **MoveFirst**, **MoveLast**, **MoveNext** y **MovePrevious** del objeto **RDS.DataControl** en los procedimientos onClick de los botones Primero, Último, Siguiente y Anterior, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="82211-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="82211-116">En el [Ejemplo de la Libreta de direcciones](address-book-navigation-buttons.md) se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="82211-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

