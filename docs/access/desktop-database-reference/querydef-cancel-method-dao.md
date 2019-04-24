---
title: Método QueryDef. Cancel (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301123"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="dd399-102">Método QueryDef. Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd399-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="dd399-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd399-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="dd399-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd399-104">Syntax</span></span>

<span data-ttu-id="dd399-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="dd399-105">*expression* .Cancel</span></span>

<span data-ttu-id="dd399-106">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="dd399-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd399-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd399-107">Remarks</span></span>

<span data-ttu-id="dd399-108">Utilice el método **Cancel** para terminar la ejecución de una llamada al método **Execute** o **OpenConnection** asincrónica (es decir, el método se ha invocado con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="dd399-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="dd399-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="dd399-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

