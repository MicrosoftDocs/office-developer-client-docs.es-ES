---
title: Métodos MoveFirst, MoveLast, MoveNext y MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288689"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="5ba8f-102">Métodos MoveFirst, MoveLast, MoveNext y MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="5ba8f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ba8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ba8f-104">Se desplaza al primer, último, siguiente o anterior registro de un objeto [Recordset](recordset-object-ado.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ba8f-105">Syntax</span></span>

<span data-ttu-id="5ba8f-106">*DataControl*. Recordset. {</span><span class="sxs-lookup"><span data-stu-id="5ba8f-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="5ba8f-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="5ba8f-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="5ba8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ba8f-108">Parameters</span></span>

|<span data-ttu-id="5ba8f-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5ba8f-109">Parameter</span></span>|<span data-ttu-id="5ba8f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ba8f-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5ba8f-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5ba8f-111">*DataControl*</span></span> |<span data-ttu-id="5ba8f-112">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5ba8f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ba8f-113">Remarks</span></span>

<span data-ttu-id="5ba8f-114">Puede usar los métodos **Move** con **RDS. Objeto DataControl** para navegar por los registros de datos de los controles enlazados a datos de una página web.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="5ba8f-115">Por ejemplo, supongamos que muestra un objeto **Recordset** en una cuadrícula enlazando a un objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="5ba8f-116">A continuación, podrá incluir los botones Primero, Último, Siguiente y Anterior, en los que los usuarios pueden hacer clic para moverse hacia el registro primero, último, siguiente o anterior del objeto **Recordset** mostrado.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="5ba8f-117">Para ello, debe llamar a los métodos **MoveFirst**, **MoveLast**, **MoveNext** y **MovePrevious** del objeto **RDS.DataControl** en los procedimientos onClick de los botones Primero, Último, Siguiente y Anterior, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="5ba8f-118">En el [Ejemplo de la Libreta de direcciones](address-book-navigation-buttons.md) se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

