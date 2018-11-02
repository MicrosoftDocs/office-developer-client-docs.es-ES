---
title: Database.Close (método) (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920686"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="dcd1e-102">Database.Close (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="dcd1e-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="dcd1e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcd1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcd1e-104">Cierra un objeto **Database** abierto.</span><span class="sxs-lookup"><span data-stu-id="dcd1e-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcd1e-105">Syntax</span></span>

<span data-ttu-id="dcd1e-106">*expresión* . Cerrar</span><span class="sxs-lookup"><span data-stu-id="dcd1e-106">*expression* .Close</span></span>

<span data-ttu-id="dcd1e-107">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="dcd1e-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd1e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcd1e-108">Remarks</span></span>

<span data-ttu-id="dcd1e-109">Si el objeto **Database** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="dcd1e-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="dcd1e-110">Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="dcd1e-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

