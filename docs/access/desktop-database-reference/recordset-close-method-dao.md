---
title: Recordset.Close (método) (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5eaa2153e2c420fb91518a47509abec8059d87a0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922849"
---
# <a name="recordsetclose-method-dao"></a><span data-ttu-id="6e61e-102">Recordset.Close (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e61e-102">Recordset.Close method (DAO)</span></span>


<span data-ttu-id="6e61e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e61e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e61e-104">Cierra un objeto **Recordset** abierto.</span><span class="sxs-lookup"><span data-stu-id="6e61e-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e61e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e61e-105">Syntax</span></span>

<span data-ttu-id="6e61e-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="6e61e-106">*expression* .Close</span></span>

<span data-ttu-id="6e61e-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="6e61e-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e61e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e61e-108">Remarks</span></span>

<span data-ttu-id="6e61e-109">Si el objeto **Recordset** ya está cerrado cuando usa **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6e61e-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="6e61e-p101">Si intenta cerrar un objeto **Connection** mientras éste tiene objetos **Recordset** abiertos, los objetos **Recordset** se cerrarán y se cancelará cualquier actualización o modificación pendiente. De igual manera, si intenta cerrar un objeto **Workspace** mientras éste tiene objetos **Connection** abiertos, se cerrarán estos objetos **Connection**, que cerrarán a su vez sus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6e61e-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="6e61e-112">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="6e61e-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

