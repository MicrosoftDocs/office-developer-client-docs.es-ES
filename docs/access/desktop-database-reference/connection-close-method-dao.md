---
title: Método Connection.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717219"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="cfe81-102">Método Connection.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfe81-102">Connection.Close method (DAO)</span></span>


<span data-ttu-id="cfe81-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfe81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfe81-104">Cierra un objeto **Connection** abierto.</span><span class="sxs-lookup"><span data-stu-id="cfe81-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe81-105">Syntax</span></span>

<span data-ttu-id="cfe81-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="cfe81-106">*expression* .Close</span></span>

<span data-ttu-id="cfe81-107">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="cfe81-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe81-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfe81-108">Remarks</span></span>

<span data-ttu-id="cfe81-109">Si el objeto **Recordset** ya está cerrado cuando usa **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cfe81-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="cfe81-p101">Si intenta cerrar un objeto **Connection** mientras éste tiene objetos **Recordset** abiertos, los objetos **Recordset** se cerrarán y se cancelará cualquier actualización o modificación pendiente. De igual manera, si intenta cerrar un objeto **Workspace** mientras éste tiene objetos **Connection** abiertos, se cerrarán estos objetos **Connection**, que cerrarán a su vez sus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cfe81-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="cfe81-112">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="cfe81-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

