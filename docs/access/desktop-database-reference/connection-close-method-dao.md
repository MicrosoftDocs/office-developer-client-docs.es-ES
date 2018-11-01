---
title: Connection.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4cc4230c7d647d58c0f30bd8351118e6c44198a8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879702"
---
# <a name="connectionclose-method-dao"></a><span data-ttu-id="0896b-102">Connection.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0896b-102">Connection.Close Method (DAO)</span></span>


<span data-ttu-id="0896b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0896b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0896b-104">Cierra un objeto **Connection** abierto.</span><span class="sxs-lookup"><span data-stu-id="0896b-104">Closes an open **Connection**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0896b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0896b-105">Syntax</span></span>

<span data-ttu-id="0896b-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="0896b-106">*expression* .Close</span></span>

<span data-ttu-id="0896b-107">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="0896b-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0896b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0896b-108">Remarks</span></span>

<span data-ttu-id="0896b-109">Si el objeto **Recordset** ya está cerrado cuando usa **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0896b-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="0896b-p101">Si intenta cerrar un objeto **Connection** mientras éste tiene objetos **Recordset** abiertos, los objetos **Recordset** se cerrarán y se cancelará cualquier actualización o modificación pendiente. De igual manera, si intenta cerrar un objeto **Workspace** mientras éste tiene objetos **Connection** abiertos, se cerrarán estos objetos **Connection**, que cerrarán a su vez sus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0896b-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="0896b-112">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="0896b-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

