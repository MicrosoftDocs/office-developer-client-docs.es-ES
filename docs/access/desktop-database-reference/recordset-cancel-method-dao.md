---
title: Recordset.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d7e77bd844385b9400449027312dacc02940e58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484041"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="0de1e-102">Recordset.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0de1e-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="0de1e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0de1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="0de1e-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0de1e-104">Syntax</span></span>

<span data-ttu-id="0de1e-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="0de1e-105">*expression* .Cancel</span></span>

<span data-ttu-id="0de1e-106">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0de1e-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de1e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0de1e-107">Remarks</span></span>

<span data-ttu-id="0de1e-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="0de1e-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="0de1e-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="0de1e-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

