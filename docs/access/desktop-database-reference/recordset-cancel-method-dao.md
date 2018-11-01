---
title: Recordset.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cde31424f409f3b3d152189e3964bc3447cfd53c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871489"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="21834-102">Recordset.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="21834-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="21834-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21834-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="21834-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21834-104">Syntax</span></span>

<span data-ttu-id="21834-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="21834-105">*expression* .Cancel</span></span>

<span data-ttu-id="21834-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="21834-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21834-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21834-107">Remarks</span></span>

<span data-ttu-id="21834-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="21834-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="21834-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="21834-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

