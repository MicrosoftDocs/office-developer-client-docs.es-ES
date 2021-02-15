---
title: Método Recordset.Cancel (DAO)
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
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="21ce1-102">Método Recordset.Cancel (DAO)</span><span class="sxs-lookup"><span data-stu-id="21ce1-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="21ce1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21ce1-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="21ce1-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21ce1-104">Syntax</span></span>

<span data-ttu-id="21ce1-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="21ce1-105">*expression* .Cancel</span></span>

<span data-ttu-id="21ce1-106">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="21ce1-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ce1-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21ce1-107">Remarks</span></span>

<span data-ttu-id="21ce1-108">Use el **método Cancel** para finalizar la ejecución de una llamada asincrónica al método **Execute** o **OpenConnection** (es decir, el método se invocó con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="21ce1-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="21ce1-109">**Cancel** devolverá un error en tiempo de ejecución si dbRunAsync no se usó en el método que está intentando finalizar.</span><span class="sxs-lookup"><span data-stu-id="21ce1-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

