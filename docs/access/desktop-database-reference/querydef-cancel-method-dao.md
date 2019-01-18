---
title: QueryDef.Cancel (método) (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720558"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="d0586-102">QueryDef.Cancel (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="d0586-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="d0586-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0586-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d0586-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0586-104">Syntax</span></span>

<span data-ttu-id="d0586-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="d0586-105">*expression* .Cancel</span></span>

<span data-ttu-id="d0586-106">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="d0586-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0586-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0586-107">Remarks</span></span>

<span data-ttu-id="d0586-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="d0586-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="d0586-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="d0586-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

