---
title: Método Recordset. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300815"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="727a3-102">Método Recordset. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="727a3-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="727a3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="727a3-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="727a3-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="727a3-104">Syntax</span></span>

<span data-ttu-id="727a3-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="727a3-105">*expression* .Cancel</span></span>

<span data-ttu-id="727a3-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="727a3-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="727a3-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="727a3-107">Remarks</span></span>

<span data-ttu-id="727a3-108">Utilice el método **Cancel** para terminar la ejecución de una llamada al método **Execute** o **OpenConnection** asincrónica (es decir, el método se ha invocado con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="727a3-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="727a3-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="727a3-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

