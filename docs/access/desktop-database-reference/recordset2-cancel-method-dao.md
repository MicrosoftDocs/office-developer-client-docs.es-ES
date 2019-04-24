---
title: Método Recordset2. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307416"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="bc28c-102">Método Recordset2. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc28c-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="bc28c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc28c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="bc28c-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc28c-104">Syntax</span></span>

<span data-ttu-id="bc28c-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="bc28c-105">*expression* .Cancel</span></span>

<span data-ttu-id="bc28c-106">*expresión* Expresión que devuelve un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="bc28c-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc28c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc28c-107">Remarks</span></span>

<span data-ttu-id="bc28c-108">Utilice el método **Cancel** para terminar la ejecución de una llamada al método **Execute** o **OpenConnection** asincrónica (es decir, el método se ha invocado con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="bc28c-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="bc28c-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="bc28c-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

