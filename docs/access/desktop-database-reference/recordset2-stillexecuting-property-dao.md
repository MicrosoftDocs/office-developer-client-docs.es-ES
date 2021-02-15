---
title: Propiedad Recordset2.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307220"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="1a0ee-102">Propiedad Recordset2.StillExecuting (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a0ee-102">Recordset2.StillExecuting property (DAO)</span></span>


<span data-ttu-id="1a0ee-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a0ee-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0ee-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a0ee-104">Syntax</span></span>

<span data-ttu-id="1a0ee-105">*expresión* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="1a0ee-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="1a0ee-106">*expresión* Variable que representa un objeto **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="1a0ee-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a0ee-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a0ee-107">Remarks</span></span>

<span data-ttu-id="1a0ee-p101">Utilice la propiedad **StillExecuting** para determinar si el método asincrónico **Execute** o **OpenConnection** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se ha completado. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="1a0ee-p102">Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **Connection**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="1a0ee-112">Utilice el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea que se esté realizando.</span><span class="sxs-lookup"><span data-stu-id="1a0ee-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

