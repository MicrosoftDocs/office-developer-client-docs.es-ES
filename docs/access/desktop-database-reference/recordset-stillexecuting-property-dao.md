---
title: Propiedad Recordset.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1195a45c3846cf79a45c16cda8e23bc95ef8156d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307570"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="1d131-102">Propiedad Recordset.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="1d131-102">Recordset.StillExecuting property (DAO)</span></span>

<span data-ttu-id="1d131-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d131-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1d131-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d131-104">Syntax</span></span>

<span data-ttu-id="1d131-105">*expresión* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="1d131-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="1d131-106">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1d131-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d131-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d131-107">Remarks</span></span>

<span data-ttu-id="1d131-p101">Utilice la propiedad **StillExecuting** para determinar si el método asincrónico **Execute** o **OpenConnection** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se ha completado. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d131-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="1d131-p102">Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **Connection**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="1d131-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="1d131-112">Utilice el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea que se esté realizando.</span><span class="sxs-lookup"><span data-stu-id="1d131-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

