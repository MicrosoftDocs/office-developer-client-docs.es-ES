---
title: Recordset2.Cancel (método) (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708427"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="7e8da-102">Recordset2.Cancel (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e8da-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="7e8da-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e8da-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8da-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e8da-104">Syntax</span></span>

<span data-ttu-id="7e8da-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="7e8da-105">*expression* .Cancel</span></span>

<span data-ttu-id="7e8da-106">*expresión* Expresión que devuelve un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7e8da-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e8da-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e8da-107">Remarks</span></span>

<span data-ttu-id="7e8da-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="7e8da-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="7e8da-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="7e8da-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

