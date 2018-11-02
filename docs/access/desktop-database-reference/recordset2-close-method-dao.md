---
title: Recordset2.Close (método) (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e0ad367ce37a33bb90eb193266d203450fa9d543
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924697"
---
# <a name="recordset2close-method-dao"></a><span data-ttu-id="b068b-102">Recordset2.Close (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="b068b-102">Recordset2.Close method (DAO)</span></span>


<span data-ttu-id="b068b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b068b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b068b-104">Cierra un objeto **Recordset** abierto.</span><span class="sxs-lookup"><span data-stu-id="b068b-104">Closes an open **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b068b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b068b-105">Syntax</span></span>

<span data-ttu-id="b068b-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="b068b-106">*expression* .Close</span></span>

<span data-ttu-id="b068b-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b068b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b068b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b068b-108">Remarks</span></span>

<span data-ttu-id="b068b-109">Si el objeto **Recordset** ya está cerrado cuando usa **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b068b-109">If the **Recordset** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="b068b-p101">Si intenta cerrar un objeto **Connection** mientras éste tiene objetos **Recordset** abiertos, los objetos **Recordset** se cerrarán y se cancelará cualquier actualización o modificación pendiente. De igual manera, si intenta cerrar un objeto **Workspace** mientras éste tiene objetos **Connection** abiertos, se cerrarán estos objetos **Connection**, que cerrarán a su vez sus objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b068b-p101">If you try to close a **Connection** object while it has any open **Recordset** objects, the **Recordset** objects will be closed and any pending updates or edits will be canceled. Similarly, if you try to close a **Workspace** object while it has any open **Connection** objects, those **Connection** objects will be closed, which will close their **Recordset** objects.</span></span>

<span data-ttu-id="b068b-112">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="b068b-112">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

