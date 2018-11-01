---
title: Recordset2.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5df46c36ff28bae1e48dfc8dc77443f707fc3e0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877537"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="d2f00-102">Recordset2.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="d2f00-102">Recordset2.Cancel Method (DAO)</span></span>


<span data-ttu-id="d2f00-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2f00-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f00-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2f00-104">Syntax</span></span>

<span data-ttu-id="d2f00-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="d2f00-105">*expression* .Cancel</span></span>

<span data-ttu-id="d2f00-106">*expresión* Expresión que devuelve un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d2f00-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f00-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2f00-107">Remarks</span></span>

<span data-ttu-id="d2f00-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="d2f00-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="d2f00-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="d2f00-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

